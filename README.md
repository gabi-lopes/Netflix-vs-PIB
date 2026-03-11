# 🚴 Part II – Trip Duration Analysis
**Autora:** Gabriela Lopes

---

## 📖 Overview
Esta investigação explora padrões de uso de bicicletas compartilhadas em uma cidade específica.  
O foco principal é analisar:
- Duração das viagens
- Tipos de usuários
- Estações mais utilizadas  

O objetivo é identificar tendências de comportamento, otimizar serviços e fornecer insights estratégicos para crescimento do sistema de compartilhamento de bicicletas.

---

## 🗂 Dataset Overview
**Arquivo:** `cleaned_data.csv`  
**Linhas:** 183.412  
**Colunas:** 16  

Inclui:
- `duration_sec` – duração da viagem em segundos  
- `start_time` / `end_time` – horário de início e fim da viagem  
- `start_station_name` / `end_station_name` – nomes das estações  
- `start_station_latitude` / `start_station_longitude` – localização geográfica  
- `user_type` – Subscriber ou Customer  
- `member_birth_year` / `member_gender` – dados demográficos  
- `bike_share_for_all_trip` – participação no programa Bike Share for All  

**Limpeza de dados:**  
- Remoção de outliers em `duration_sec`  
- Exclusão de valores ausentes  
- Dataset final contém **175.147 linhas limpas**  

---

## 📊 Key Insights

### ⏱ Trip Duration Patterns
- A maioria das viagens dura menos de 15 minutos (~800 segundos).  
- Indica popularidade para deslocamentos rápidos.  
- Outliers com durações muito longas foram filtrados.

### 👥 User Type Trends
- **Subscribers** dominam a base e apresentam viagens mais consistentes.  
- **Customers** têm mais variabilidade, sugerindo uso recreativo ou ocasional.

### 📍 Station Popularity
- Algumas estações são consistentemente mais populares como ponto de partida.  
- Estas estações estão próximas a hubs de transporte e áreas movimentadas.  

---

## 📈 Visualizations

### 1️⃣ Trip Duration Distribution (Histogram)
Mostra a distribuição das durações, destacando a maioria das viagens curtas e a presença de outliers.

```python
plt.figure(figsize=(10, 6))
sns.histplot(df['duration_sec'], kde=True, bins=300)
plt.title('Distribution of Trip Durations')
plt.xlabel('Duration (seconds)')
plt.ylabel('Frequency')
plt.xlim(0, 8000)
plt.show()
