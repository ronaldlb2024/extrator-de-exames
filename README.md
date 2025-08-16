# Extrator de Exames – Caixa de Texto (Versão Estendida)

## Descrição
Ferramenta em JavaScript que pode ser colada diretamente no **Console do navegador (F12)** para extrair exames laboratoriais de laudos em PDF/HTML (completo ou evolutivo, como Dasa, Rede D’Or, Afip). A saída é simplificada em uma única linha pronta para evolução ou prontuário.

A interface aparece como um painel no canto da tela, com caixas de texto para **entrada**, **saída** e um **compilado persistente** (armazenado em `localStorage`).

## Fluxo de Uso
1. Abra o laudo no navegador (modo leitura ou PDF aberto em HTML).
2. Pressione **F12** → guia **Console**.
3. Cole o código completo do script e pressione **ENTER**.
4. No painel que abrirá:
   - **Cole** o laudo bruto na caixa superior.
   - Clique **Extrair** para gerar a linha formatada.
   - Use **Adicionar ao compilado** para salvar como “Leito 1…N”.
   - Opcional: digite o nome do paciente para vincular.
   - Ao finalizar, clique em **Exportar .txt** para baixar todos os resultados.

## Recursos
- Suporte a **laudos completos** e **evolutivos**.
- Extrai automaticamente valores de:
  - Hemograma: Hb, Ht, Leucócitos (ajustado para Dasa – valor absoluto), Plaquetas (ajuste para milhares), RDW, Neutrófilos, Segmentados, Linfócitos, Monócitos, Eosinófilos, Basófilos.
  - Bioquímica: Uréia, Creatinina, Sódio, Potássio, Magnésio, Cálcio iônico, Glicose, Lactato, PCR, Troponina.
  - Gasometrias: Arterial e Venosa (pH, pO2, pCO2, HCO3, BE, SatO2).
  - Coagulação: RNI/INR, Relação TTPA.
- **Persistência local**: mantém o compilado no navegador até ser limpo.
- **Exportação**: gera `.txt` com todos os pacientes/leitos.
- **Atalhos**: botão para copiar saída, limpar entrada, limpar compilado.

## Observações
- Não envia dados para nenhum servidor, todo processamento ocorre **localmente no navegador**.
- Funciona em Chrome/Edge/Firefox (preferência para Chromium).
- Recomenda-se usar em computadores pessoais ou ambientes controlados, devido a dados sensíveis.

## Exemplo de Linha Gerada
```
Hb 10.9; Ht 32.9; Leuco 5820; Plaq 91000; URE 146; CRE 2.2; NA 140; K 3.5; pH(a) 7.33; pO2(a) 35; ...
```

