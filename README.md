# OTT-Analysis-on-Spotify-Dataset

LINK:- https://www.kaggle.com/code/jyotimanojmandal/ott-analysis-spotify-dataset


About the project: This project is a part of course Data Analysis with Python: Zero to Pandas provided by Jovian. Jovian is an online platform for data science and machine learning. It is designed to provide the best hands-on learning experience.

About Dataset: This dataset is retrieved from kaggle. Kaggle is a online platform especially for data science and machine learning which provide resources and tools for achieving higher in the domain. The link for this url is Spotify data and you can visit Kaggle datasets for various interesting datasets around the world.

Our dataset contains informations like tracks, artists, popularity, duration and many more.

Objective of the analysis
To extract more and more information from the data.
To provide better insights. So that it will help in future decisions that can be taken by the company.

corr_df = df_tracks.drop(["key", "mode", "explicit"], axis = 1).corr(method = "pearson", numeric_only = True)
plt.figure(figsize = (10,6))
ax = sns.heatmap(corr_df, annot = True, fmt = ".1g", linecolor = 'k', linewidths = '5', cmap = 'Reds')
plt.title("Correlation Between Variables")
sample_df = df_tracks.sample(int(0.004*len(df_tracks)))
print(len(sample_df))

plt.figure(figsize = (10,6))
sns.regplot(data = sample_df, y = "loudness", x = "energy", color = "c")
plt.title("Loudness vs Energy Correlation")

plt.figure(figsize = (10,8))
sns.regplot(data = sample_df, y = "popularity", x = "acousticness", color = "red")
plt.title("Popularity vs Acoustiness Correlation")

df_tracks['dates'] = df_tracks.index.get_level_values('release_date')
df_tracks.dates = pd.to_datetime(df_tracks.dates)
years = df_tracks.dates.dt.year
sns.displot(years, discrete = True, aspect = 2, height = 5, kind = "hist")
plt.title("Number of Songs per Year")


![__results___27_1](https://github.com/HOSHANGI/OTT-Analysis-on-Spotify-Dataset/assets/118753140/b2373b12-4fc4-4d62-a494-d285a709a508)
![__results___26_1](https://github.com/HOSHANGI/OTT-Analysis-on-Spotify-Dataset/assets/118753140/b32e3b1f-708d-4863-af4c-c5dd358b559e)
![__results___21_1](https://github.com/HOSHANGI/OTT-Analysis-on-Spotify-Dataset/assets/118753140/880d4bc1-e258-4b78-bb8b-e6a75c5a99a2)
![__results___20_1](https://github.com/HOSHANGI/OTT-Analysis-on-Spotify-Dataset/assets/118753140/076cdd46-a281-4833-b499-50983e5095f6)
![__results___19_1](https://github.com/HOSHANGI/OTT-Analysis-on-Spotify-Dataset/assets/118753140/3eab2fac-3f8b-4bd8-8a79-3c43d52fe1bf)
![__results___17_1](https://github.com/HOSHANGI/OTT-Analysis-on-Spotify-Dataset/assets/118753140/4ef86a7d-51bc-412e-b7bd-036680b3c089)
![__results___16_2](https://github.com/HOSHANGI/OTT-Analysis-on-Spotify-Dataset/assets/118753140/ff3a787c-5aca-486c-8755-58c083674778)
![__results___15_1](https://github.com/HOSHANGI/OTT-Analysis-on-Spotify-Dataset/assets/118753140/8c0e66cb-c8c5-4406-bf71-63f98f8e5939)
![Spotify](https://github.com/HOSHANGI/OTT-Analysis-on-Spotify-Dataset/assets/118753140/c66d0213-90d4-4e85-919a-6bc850238b43)
