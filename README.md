import pandas as pd  

# 1. DataFrame yaratish  
data = {  
    'Ism': ['Ali', 'Vali', 'Sardor'],  
    'Yoshi': [25, 30, 22],  
    'Shahar': ['Toshkent', 'Samarqand', 'Buxoro']  
}  
df = pd.DataFrame(data)  

# 2. Ma'lumotlarni ko'rish  
print(df)  

# 3. Filtrlash  
young_people = df[df['Yoshi'] < 30]  
print("30 yoshdan kichiklar:\n", young_people)  

# 4. O'zgartirish  
df['Yoshi'] += 1  # Har bir shaxsning yoshini 1 ga oshirish  
print("Yangilangan DataFrame:\n", df)  

# 5. CSV formatda saqlash  
df.to_csv('data.csv', index=False)
