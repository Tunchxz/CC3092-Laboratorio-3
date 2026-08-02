# Laboratorio 3: Seq2Seq Inglés-Español

Implementación desde cero, **usando únicamente PyTorch** (sin `nn.LSTM`, `nn.Embedding`, `nn.Linear`, sin `loss.backward()`), de un modelo Seq2Seq Encoder-Decoder con celdas LSTM para traducción inglés-español sobre un corpus con traducciones naturales en español (elisión de sujeto, perífrasis verbales, mismo largo).

Se implementan tanto el **forward pass** como el **backward pass** (backpropagation manual):

```
oración_EN → [E_enc] → [Encoder LSTM] → c = h_T^enc
                                          |
<SOS>+oración_ES → [E_dec] → [Decoder LSTM] → [W_out+softmax] → predicción
```

## Cómo ejecutar el notebook

Requiere Python 3.

1. (Recomendado) Crear un entorno virtual e instalar dependencias:

   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   pip install -r requirements.txt
   ```

2. Abrir el notebook y ejecutar las celdas **en orden**:

   ```bash
   jupyter notebook Laboratorio-3.ipynb
   ```

   O ejecutarlo completo sin interfaz gráfica:

   ```bash
   jupyter nbconvert --to notebook --execute --inplace Laboratorio-3.ipynb
   ```
