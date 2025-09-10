# Docker Hello World Examples

Exemplos simples de apps rodando em Docker, com `HEALTHCHECK`.

---

## 🟢 Node.js App

### Build
```bash
docker build --build-arg VERSION=1.1.0 -t nodeapp:0.1 -f Dockerfile .
```

### Run
```bash
docker run --name nodeapp   -e PORT=3000   -p 3000:3000   nodeapp:0.1
```

Acesse em: [http://localhost:3000](http://localhost:3000)

---

## 🐍 Python Flask App

### Build
```bash
docker build -t python-healthcheck -f Dockerfile.python .
```

### Run
```bash
docker run -p 5000:5000 python-healthcheck:latest
```

Acesse em:  
- Página principal → [http://localhost:5000](http://localhost:5000)  
- Healthcheck → [http://localhost:5000/health](http://localhost:5000/health)  