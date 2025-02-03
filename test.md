#  UTK EEB Resources 

## Facts 
The Ecology & Evolutionary Biology Department: 
- is a top 10% program in the field 
- offers both Masters and PhD degrees
- has 62 graduate students

## Links
[EEB-website](https://eeb.utk.edu/)

## Outreach
![EEB_people](https://eeb.utk.edu/wp-content/uploads/2023/12/graduate-students.webp)

## EEB Analysis Example
```
set.seed(123)

habitat <- rep(c("Forest", "Grassland", "Wetland"), each = 20)  # 3 habitat types, 20 samples each
biomass <- c(rnorm(20, mean = 50, sd = 10),  # Forest: Mean = 50, SD = 10
             rnorm(20, mean = 30, sd = 8),   # Grassland: Mean = 30, SD = 8
             rnorm(20, mean = 40, sd = 9))   # Wetland: Mean = 40, SD = 9

ecology_data <- data.frame(Habitat = habitat, Biomass = biomass)

anova_result <- aov(Biomass ~ Habitat, data = ecology_data)

summary(anova_result)

boxplot(Biomass ~ Habitat, data = ecology_data, col = c("lightgreen", "gold", "lightblue"),
        main = "Plant Biomass Across Different Habitats", ylab = "Biomass (g/m²)", xlab = "Habitat Type")

```