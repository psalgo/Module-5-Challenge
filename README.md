# Module-5-Challenge
paul salgo module 5 challenge

Citations:
####
drug_regimen_counts.plot(kind='bar', color='purple', alpha=0.7, figsize=(10, 6))
plt.title('Total Number of Rows for Each Drug Regimen')
plt.xlabel('Drug Regimen')
plt.ylabel('Number of Rows')

plt.show()
-- chatgpt

####
gender_distribution.plot.pie(autopct='%1.1f%%', colors=['blue', 'red'], startangle=90)
plt.title('Distribution of Female versus Male Mice (Pandas)')
plt.axis('equal')  # pie is drawn as a circle

plt.show()
-- chatgpt

####
plt.figure(figsize=(8, 8))
plt.pie(gender_distribution, labels=gender_distribution.index, autopct='%1.1f%%', colors=['blue', 'red'], startangle=90)
plt.title('Distribution of Female versus Male Mice (Matplotlib)')
plt.axis('equal')  # pie is drawn as a circle

plt.show()
-- chatgpt

from scipy.stats import linregress
correlation_coefficient = capomulin_data['Weight (g)'].corr(capomulin_data.groupby('Mouse ID')['Tumor Volume (mm3)'].mean())

slope, intercept, rvalue, pvalue, stderr = linregress(mouse_weight, avg_tumor_volume)

regression_line = slope * mouse_weight + intercept

# Plot
plt.figure(figsize=(10, 6))
plt.scatter(mouse_weight, avg_tumor_volume, color='green', edgecolors='black')
plt.plot(mouse_weight, regression_line, color='red', label=f'Linear Regression\nCorrelation: {correlation_coefficient:.2f}')
plt.title('Mouse Weight vs. Average Tumor Volume (Capomulin) with Linear Regression')
plt.xlabel('Mouse Weight (g)')
plt.ylabel('Average Tumor Volume (mm3)')
plt.legend()
plt.grid(True)
plt.show()
-- chatgpt
