import csv
import os

os.chdir(r'C:\Users\xyl19\PycharmProjects\untitled\gpt')

input_file = 'F&Q_default.md'
output_file = 'output.csv'

with open(input_file, 'r',encoding='utf-8') as f:
    lines = f.readlines()

# Extracting headers
headers = lines[0].strip().split('|')
headers = [header.strip() for header in headers if header.strip()]

data = []
for line in lines[2:]:
    row = line.strip().split('|')
    row = [field.strip() for field in row if field.strip()]
    if len(row) == len(headers):
        data.append(row)

# Writing to CSV file
with open(output_file, 'w', newline='',encoding='utf-8') as f:
    writer = csv.writer(f)
    writer.writerow(['index', 'content', 'source'])
    writer.writerows(data)
