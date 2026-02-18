# Diagrama de Arquitectura del Sistema

## Componentes
+-------------+
¦ Cliente ¦ (App Móvil / Navegador)
¦ (Frontend) ¦
+-------------+
¦
+-----------------+
¦ ¦
? ?
+-------------+ +-------------+
¦ API REST ¦ ¦ GraphQL ¦
¦ (PokéAPI) ¦ ¦ Playground¦
+-------------+ +-------------+
¦ ¦
+-----------------+
¦
?
+-----------------+
¦ Base de Datos ¦
¦ Pokémon API ¦
+-----------------+
## Flujo de Peticiones

### REST (Over-fetching)
1. Cliente solicita `/pokemon/1`
2. Servidor responde con TODO el objeto Pokémon
3. Cliente recibe muchos datos innecesarios

### GraphQL (Eficiente)
1. Cliente envía consulta con campos específicos
2. Servidor devuelve SOLO los campos solicitados
3. Incluye datos relacionados (evoluciones) en una sola petición

## Decisión Arquitectónica
Para aplicaciones móviles con datos limitados, **GraphQL** es superior por:
- Menor consumo de datos
- Menos peticiones HTTP
- Control total del cliente sobre la respuesta