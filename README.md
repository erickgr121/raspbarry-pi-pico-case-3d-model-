# raspbarry-pi-pico-case-3d-model-
uma case 3d para a comunidade do raspbarry pi pico usb c 
# 

Este é um projeto de case mecânico totalmente paramétrico desenvolvido em **OpenSCAD** para a placa de desenvolvimento **YD-RP2040** (fabricada pela *VCC-GND Studio*). O design foi projetado do zero para manufatura aditiva (impressão 3D FDM), dividindo-se em duas partes funcionais (Base e Tampa) com encaixe por pressão (*snap-fit*) e botões flexíveis integrados (*living hinge*), dispensando o uso de parafusos ou suportes de impressão.

---

## 📐 Características do Projeto e Hardware Real

Diferente de cases comuns para a Raspberry Pi Pico padrão, este modelo foi mapeado milimetricamente usando como referência a geometria real e exclusiva da **YD-RP2040**, corrigindo os eixos e posições dos seguintes componentes:
* **Conector USB-C:** Abertura frontal expandida para cabos modernos de alta qualidade.
* **Botão BOOT:** Posicionado no quadrante superior esquerdo da placa.
* **Janela do LED RGB:** Abertura centralizada na extremidade oposta.
* **Botão RESET (RST):** Botão mecânico flexível integrado à direita do LED RGB.
* **Botão USER (USR):** Botão mecânico flexível integrado à esquerda do LED RGB.
* **Ventilação Ativa:** 6 furos inferiores e 4 aberturas horizontais nas paredes maiores para dissipação térmica natural do chip RP2040.

---

## 🔧 Configurações e Variáveis Globais (OpenSCAD)

O arquivo `YD-RP2040_Case.scad` é 100% editável. Você pode alterar as tolerâncias estruturais modificando as variáveis no início do script:

| Parâmetro | Valor Padrão | Descrição |
| :--- | :--- | :--- |
| `wall_thick` | `2.00 mm` | Espessura das paredes perimetrais externas |
| `floor_thick` | `1.60 mm` | Espessura do piso da base |
| `lid_thick` | `1.80 mm` | Espessura do topo da tampa |
| `clearance_side`| `0.20 mm` | Folga interna nas laterais da PCB |
| `clearance_lid` | `0.25 mm` | Folga perimetral de acoplamento da tampa |
| `btn_hinge_thick`| `0.80 mm`| Espessura da membrana flexível dos botões |

---


## 🖨️ Parâmetros Recomendados de Fatiamento (3D Printing)

O design foi otimizado para ser impresso **sem suportes**. As pontes internas e furos utilizam chanfros geométricos autoportantes.

* **Material:** PLA, PETG ou ABS.
* **Altura de Camada:** `0.20 mm` (essencial para a espessura calibrada das travas e botões flexíveis).
* **Perímetros/Paredes:** `3` ou `4` (garante resistência mecânica elástica nas presilhas).
* **Preenchimento (Infill):** `15%` a `20%` (Padrões *Giroide* ou *Grade* são recomendados).
* **Suporte:** **Desativado (NÃO UTILIZAR)**.
* **Orientação na Mesa:**
  * A **Base** deve ser impressa com o fundo apoiado diretamente na mesa.
  * A **Tampa** é exportada invertida automaticamente pelo código, garantindo que o teto plano externo fique colado na mesa de impressão para melhor acabamento superficial.

---

## 🛠️ Montagem e Uso

1. Espere a mesa da impressora esfriar completamente antes de retirar as peças para evitar empenamento térmico nas áreas finas.
2. Com o dedo, pressione levemente os três botões da tampa algumas vezes para amaciar as membranas de plástico (*living hinge*).
3. Insira a placa YD-RP2040 dentro da base, encaixando-a nos 4 pinos guias e passando o conector USB-C pelo rasgo frontal.
4. Alinhe a tampa sobre a base e aplique uma leve pressão nas laterais até escutar o estalo (*snap*) dos quatro clipes de fixação.

---

## 📄 Licença

Este projeto está licenciado sob a licença **MIT** - consulte o arquivo [LICENSE](LICENSE) para obter mais detalhes.
