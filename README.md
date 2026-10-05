# QAcove Upload Results (GitHub Action)

Sube reportes JUnit XML o Playwright JSON a QAcove. Cada resultado se asocia a un caso por código (ej. `TC-12` en el nombre del test) o por título exacto.

```yaml
- uses: DamianRobdam/qacove-action@v1
  if: always()
  with:
    api-key: ${{ secrets.QACOVE_API_KEY }}
    project-id: 12
    report-path: test-results/junit.xml
```

Requiere una API key con permiso de escritura (Cuenta → Llaves API). Usa `dry-run: true` para probar sin registrar.
