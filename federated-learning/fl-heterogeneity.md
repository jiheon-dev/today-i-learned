# Federated Learning Heterogeneity

In federated learning, data heterogeneity and statistical heterogeneity are different concepts.

Data heterogeneity refers to cases where the characteristics of the data collected by the various organizations participating in federated learning differ. This can happen because the characteristics of the data vary depending on the organization, location, and method of collection. For example, in federated learning, patients' medical history data collected from various healthcare institutions may have different formats and structures. This data heterogeneity is one of the factors that is degrading the performance of the model.

Statistical heterogeneity, on the other hand, is when the data sets of participating institutions in federated learning differ in size, distribution, variance, and label ratio. This can happen depending on the size, environment, and demographic characteristics of the institution from which the data was collected. For example, temperature data collected from various regions in federated learning may have different distributions and variances. This statistical heterogeneity can act as a factor for models to learn unsuitable data or to degrade their ability to generalize.

Thus, data heterogeneity and statistical heterogeneity are other factors to consider in federated learning. Data heterogeneity represents the characteristics of the data itself, and statistical heterogeneity represents the characteristics of the data set. To reduce this heterogeneity, the performance of the model can be improved using methods such as preprocessing data, leveling data sets, and appropriate weighting.
