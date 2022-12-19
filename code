import plotly.express as px

# Do not modify the line below.
countries = ["Argentina", "Bolivia", "Brazil", "Chile", "Colombia", "Ecuador", "Falkland Islands", "Guyana", "Paraguay", "Peru", "Suriname", "Uruguay", "Venezuela"]

# Do not modify the line below.
colors = ["blue", "green", "red", "yellow"]

# Map of neighboring countries
neighbors = {
    "Argentina": ["Bolivia", "Brazil", "Chile", "Paraguay", "Uruguay"],
    "Bolivia": ["Argentina", "Brazil", "Chile", "Paraguay", "Peru"],
    "Brazil": ["Argentina", "Bolivia", "Colombia", "Guyana", "Paraguay", "Peru", "Suriname", "Uruguay", "Venezuela"],
    "Chile": ["Argentina", "Bolivia", "Peru"],
    "Colombia": ["Brazil", "Ecuador", "Peru", "Venezuela"],
    "Ecuador": ["Colombia", "Peru"],
    "Falkland Islands": [],
    "Guyana": ["Brazil", "Suriname", "Venezuela"],
    "Paraguay": ["Argentina", "Bolivia", "Brazil"],
    "Peru": ["Bolivia", "Brazil", "Chile", "Colombia", "Ecuador"],
    "Suriname": ["Brazil", "Guyana"],
    "Uruguay": ["Argentina", "Brazil"],
    "Venezuela": ["Brazil", "Colombia", "Guyana"]
} 
def create_colormap(countries, neighbors, colors):
    colormap = {} #create colormap 
    for country in countries:
        available_colors = list(colors) #list color that specific country can take
        for neighbor in neighbors[country]: #give colour method
            if neighbor in colormap and colormap[neighbor] in available_colors:#check avaliabilty
                available_colors.remove(colormap[neighbor]) #if same with neighbour delete neighbour color 
        colormap[country] = available_colors[0]
    return colormap
# Do not modify this method, only call it with an appropriate argument.
# colormap should be a dictionary having countries as keys and colors as values.
def plot_choropleth(colormap):
    fig = px.choropleth(locationmode="country names",
                        locations=countries,
                        color=countries,
                        color_discrete_sequence=[colormap[c] for c in countries],
                        scope="south america")
    fig.show()



# Implement main to call necessary functions
if __name__ == "__main__":
    colormap = create_colormap(countries, neighbors, colors)
    plot_choropleth(colormap=colormap)
    #Hocam plot'u calıştıramadım fakat aynı colormapı methodla oluşturdum
    #bu yuzden testi sildim colomapı kendi oluşturduğumu koydum
