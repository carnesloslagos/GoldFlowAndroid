# Gold Flow Android — V0.1

Primera versión de una app Android para visualizar order flow de XAUUSDT de Binance y usarlo como referencia para operar XAUUSD en Exness.

## Qué hace esta V0.1

- Conecta al WebSocket público de Binance USDⓈ-M Futures.
- Consume `XAUUSDT@aggTrade` en tiempo real.
- Calcula Delta por trade.
- Calcula CVD acumulado.
- Consume `XAUUSDT@depth20@100ms`.
- Muestra volumen agregado de bids/asks y su proporción.
- Muestra una curva CVD.
- Muestra una lectura sencilla LONG / SHORT / ESPERAR.

## Qué NO hace todavía

- No ejecuta operaciones.
- No conecta con Exness.
- No intenta igualar exactamente los precios Binance/Exness.
- No implementa todavía FVG, heatmap histórico, absorción, footprint ni divergencia automática.
- La señal V0.1 es deliberadamente simple y NO debe usarse sola para operar dinero real.

## Cómo abrirla

1. Instala Android Studio.
2. Abre la carpeta `GoldFlowAndroid`.
3. Espera a que Gradle sincronice.
4. Conecta un Android o crea un emulador.
5. Ejecuta la configuración `app`.

## Próxima V0.2

La siguiente etapa debería añadir:
- gráfico de precio + CVD juntos;
- detección de divergencia precio/CVD;
- grandes operaciones ("burbujas");
- FVG;
- absorción;
- heatmap de liquidez;
- comparación de precio Binance vs Exness mediante una fuente de cotización de Exness;
- puntuación de confluencia.

La app usa datos públicos de mercado. Binance documenta streams WebSocket para `aggTrade` y `depth`; las conexiones públicas no requieren credenciales de cuenta. Revisar la documentación oficial antes de una versión de producción.
