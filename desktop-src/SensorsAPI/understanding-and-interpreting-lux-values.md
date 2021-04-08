---
description: Le type de données de capteur principal pour les capteurs de lumière ambiante est l’éclairage en lux (lumens par mètre carré). Les principes énoncés dans cette rubrique sont basés sur l’utilisation de valeurs en Lux comme entrée et la réaction à ces données dans un programme.
ms.assetid: 29855779-7c27-4cfe-b8af-b33bc86a1f62
title: Compréhension et interprétation des valeurs LX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8012f983eeac29cc07b18ac2d27918d2df6ed52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034850"
---
# <a name="understanding-and-interpreting-lux-values"></a><span data-ttu-id="5be8f-104">Compréhension et interprétation des valeurs LX</span><span class="sxs-lookup"><span data-stu-id="5be8f-104">Understanding and Interpreting Lux Values</span></span>

<span data-ttu-id="5be8f-105">Le type de données de capteur principal pour les capteurs de lumière ambiante est l’éclairage en lux (lumens par mètre carré).</span><span class="sxs-lookup"><span data-stu-id="5be8f-105">The primary sensor data type for ambient light sensors is illuminance in lux (lumens per square meter).</span></span> <span data-ttu-id="5be8f-106">Les principes énoncés dans cette rubrique sont basés sur l’utilisation de valeurs en Lux comme entrée et la réaction à ces données dans un programme.</span><span class="sxs-lookup"><span data-stu-id="5be8f-106">The principles outlined in this topic are based on taking lux values as input and reacting to that data in a program.</span></span>

<span data-ttu-id="5be8f-107">Les lectures en Lux sont directement proportionnelles à l’énergie par mètre carré absorbée par seconde.</span><span class="sxs-lookup"><span data-stu-id="5be8f-107">Lux readings are directly proportional to the energy per square meter that is absorbed per second.</span></span> <span data-ttu-id="5be8f-108">La perception humaine des niveaux de lumière n’est pas si simple.</span><span class="sxs-lookup"><span data-stu-id="5be8f-108">Human perception of light levels is not so straightforward.</span></span> <span data-ttu-id="5be8f-109">La perception humaine de la lumière est compliquée, car nos yeux évoluent constamment et d’autres processus biologiques affectent notre perception.</span><span class="sxs-lookup"><span data-stu-id="5be8f-109">Human perception of light is complicated because our eyes are constantly adjusting and other biological processes are affecting our perception.</span></span> <span data-ttu-id="5be8f-110">Toutefois, nous pouvons considérer cette perception d’un point de vue simplifié en créant plusieurs plages d’intérêt avec des seuils supérieurs et inférieurs connus.</span><span class="sxs-lookup"><span data-stu-id="5be8f-110">However, we can think of this perception from a simplified perspective by creating several ranges of interest with known upper and lower thresholds.</span></span>

<span data-ttu-id="5be8f-111">L’exemple de jeu de données suivant représente des seuils approximatifs pour les conditions d’éclairage courantes et l’étape d’éclairage correspondante.</span><span class="sxs-lookup"><span data-stu-id="5be8f-111">The following example data set represents rough thresholds for common lighting conditions, and the corresponding lighting step.</span></span> <span data-ttu-id="5be8f-112">Ici, chaque étape d’éclairage représente une modification de l’environnement d’éclairage.</span><span class="sxs-lookup"><span data-stu-id="5be8f-112">Here, each lighting step represents a change in lighting environment.</span></span>

> [!Note]  
> <span data-ttu-id="5be8f-113">Ce jeu de données est à titre d’illustration et peut ne pas être complètement précis pour tous les utilisateurs ou situations.</span><span class="sxs-lookup"><span data-stu-id="5be8f-113">This data set is for illustration and may not be completely accurate for all users or situations.</span></span>

 



| <span data-ttu-id="5be8f-114">Condition d’éclairage</span><span class="sxs-lookup"><span data-stu-id="5be8f-114">Lighting condition</span></span> | <span data-ttu-id="5be8f-115">De (Lux)</span><span class="sxs-lookup"><span data-stu-id="5be8f-115">From (lux)</span></span> | <span data-ttu-id="5be8f-116">À (Lux)</span><span class="sxs-lookup"><span data-stu-id="5be8f-116">To (lux)</span></span> | <span data-ttu-id="5be8f-117">Valeur moyenne (Lux)</span><span class="sxs-lookup"><span data-stu-id="5be8f-117">Mean value (lux)</span></span> | <span data-ttu-id="5be8f-118">Étape d’éclairage</span><span class="sxs-lookup"><span data-stu-id="5be8f-118">Lighting step</span></span> |
|--------------------|------------|----------|------------------|---------------|
| <span data-ttu-id="5be8f-119">Noir tonal</span><span class="sxs-lookup"><span data-stu-id="5be8f-119">Pitch Black</span></span>        | <span data-ttu-id="5be8f-120">0</span><span class="sxs-lookup"><span data-stu-id="5be8f-120">0</span></span>          | <span data-ttu-id="5be8f-121">10</span><span class="sxs-lookup"><span data-stu-id="5be8f-121">10</span></span>       | <span data-ttu-id="5be8f-122">5</span><span class="sxs-lookup"><span data-stu-id="5be8f-122">5</span></span>                | <span data-ttu-id="5be8f-123">1</span><span class="sxs-lookup"><span data-stu-id="5be8f-123">1</span></span>             |
| <span data-ttu-id="5be8f-124">Très sombre</span><span class="sxs-lookup"><span data-stu-id="5be8f-124">Very Dark</span></span>          | <span data-ttu-id="5be8f-125">11</span><span class="sxs-lookup"><span data-stu-id="5be8f-125">11</span></span>         | <span data-ttu-id="5be8f-126">50</span><span class="sxs-lookup"><span data-stu-id="5be8f-126">50</span></span>       | <span data-ttu-id="5be8f-127">30</span><span class="sxs-lookup"><span data-stu-id="5be8f-127">30</span></span>               | <span data-ttu-id="5be8f-128">2</span><span class="sxs-lookup"><span data-stu-id="5be8f-128">2</span></span>             |
| <span data-ttu-id="5be8f-129">Inportes sombres</span><span class="sxs-lookup"><span data-stu-id="5be8f-129">Dark Indoors</span></span>       | <span data-ttu-id="5be8f-130">51</span><span class="sxs-lookup"><span data-stu-id="5be8f-130">51</span></span>         | <span data-ttu-id="5be8f-131">200</span><span class="sxs-lookup"><span data-stu-id="5be8f-131">200</span></span>      | <span data-ttu-id="5be8f-132">125</span><span class="sxs-lookup"><span data-stu-id="5be8f-132">125</span></span>              | <span data-ttu-id="5be8f-133">3</span><span class="sxs-lookup"><span data-stu-id="5be8f-133">3</span></span>             |
| <span data-ttu-id="5be8f-134">Dimensions de l’intérieur</span><span class="sxs-lookup"><span data-stu-id="5be8f-134">Dim Indoors</span></span>        | <span data-ttu-id="5be8f-135">201</span><span class="sxs-lookup"><span data-stu-id="5be8f-135">201</span></span>        | <span data-ttu-id="5be8f-136">400</span><span class="sxs-lookup"><span data-stu-id="5be8f-136">400</span></span>      | <span data-ttu-id="5be8f-137">300</span><span class="sxs-lookup"><span data-stu-id="5be8f-137">300</span></span>              | <span data-ttu-id="5be8f-138">4</span><span class="sxs-lookup"><span data-stu-id="5be8f-138">4</span></span>             |
| <span data-ttu-id="5be8f-139">Inportes normales</span><span class="sxs-lookup"><span data-stu-id="5be8f-139">Normal Indoors</span></span>     | <span data-ttu-id="5be8f-140">401</span><span class="sxs-lookup"><span data-stu-id="5be8f-140">401</span></span>        | <span data-ttu-id="5be8f-141">1 000</span><span class="sxs-lookup"><span data-stu-id="5be8f-141">1000</span></span>     | <span data-ttu-id="5be8f-142">700</span><span class="sxs-lookup"><span data-stu-id="5be8f-142">700</span></span>              | <span data-ttu-id="5be8f-143">5</span><span class="sxs-lookup"><span data-stu-id="5be8f-143">5</span></span>             |
| <span data-ttu-id="5be8f-144">Portes lumineuses</span><span class="sxs-lookup"><span data-stu-id="5be8f-144">Bright Indoors</span></span>     | <span data-ttu-id="5be8f-145">1001</span><span class="sxs-lookup"><span data-stu-id="5be8f-145">1001</span></span>       | <span data-ttu-id="5be8f-146">5 000</span><span class="sxs-lookup"><span data-stu-id="5be8f-146">5000</span></span>     | <span data-ttu-id="5be8f-147">3000</span><span class="sxs-lookup"><span data-stu-id="5be8f-147">3000</span></span>             | <span data-ttu-id="5be8f-148">6</span><span class="sxs-lookup"><span data-stu-id="5be8f-148">6</span></span>             |
| <span data-ttu-id="5be8f-149">Dim Outdoors</span><span class="sxs-lookup"><span data-stu-id="5be8f-149">Dim Outdoors</span></span>       | <span data-ttu-id="5be8f-150">5001</span><span class="sxs-lookup"><span data-stu-id="5be8f-150">5001</span></span>       | <span data-ttu-id="5be8f-151">10 000</span><span class="sxs-lookup"><span data-stu-id="5be8f-151">10,000</span></span>   | <span data-ttu-id="5be8f-152">7500</span><span class="sxs-lookup"><span data-stu-id="5be8f-152">7500</span></span>             | <span data-ttu-id="5be8f-153">7</span><span class="sxs-lookup"><span data-stu-id="5be8f-153">7</span></span>             |
| <span data-ttu-id="5be8f-154">Cloud Outdoors</span><span class="sxs-lookup"><span data-stu-id="5be8f-154">Cloudy Outdoors</span></span>    | <span data-ttu-id="5be8f-155">10 001</span><span class="sxs-lookup"><span data-stu-id="5be8f-155">10,001</span></span>     | <span data-ttu-id="5be8f-156">30,000</span><span class="sxs-lookup"><span data-stu-id="5be8f-156">30,000</span></span>   | <span data-ttu-id="5be8f-157">20 000</span><span class="sxs-lookup"><span data-stu-id="5be8f-157">20,000</span></span>           | <span data-ttu-id="5be8f-158">8</span><span class="sxs-lookup"><span data-stu-id="5be8f-158">8</span></span>             |
| <span data-ttu-id="5be8f-159">Soleil direct</span><span class="sxs-lookup"><span data-stu-id="5be8f-159">Direct Sunlight</span></span>    | <span data-ttu-id="5be8f-160">30 001</span><span class="sxs-lookup"><span data-stu-id="5be8f-160">30,001</span></span>     | <span data-ttu-id="5be8f-161">100 000</span><span class="sxs-lookup"><span data-stu-id="5be8f-161">100,000</span></span>  | <span data-ttu-id="5be8f-162">65 000</span><span class="sxs-lookup"><span data-stu-id="5be8f-162">65,000</span></span>           | <span data-ttu-id="5be8f-163">9</span><span class="sxs-lookup"><span data-stu-id="5be8f-163">9</span></span>             |



 

<span data-ttu-id="5be8f-164">Si nous affichons ces données à l’aide des valeurs moyennes de ce tableau, nous voyons que la relation de l’étape Lux-à-éclairage n’est pas linéaire, comme indiqué dans le graphique suivant.</span><span class="sxs-lookup"><span data-stu-id="5be8f-164">If we visualize this data by using the mean values from this table, we see that the lux-to-lighting-step relationship is not linear, as show in the following graph.</span></span>

![graphique d’éclairage linéaire](images/luxtostep.png)

<span data-ttu-id="5be8f-166">Toutefois, si vous affichez ces données à l’aide d’une échelle logarithmique sur l’axe des x, nous voyons qu’une relation à peu près linéaire émerge.</span><span class="sxs-lookup"><span data-stu-id="5be8f-166">However, if we view this data by using a logarithmic scale on the x-axis, we can see that a roughly linear relationship emerges.</span></span>

![graphique d’éclairage logarithmique](images/luxlogtostep.png)

### <a name="an-example-transform"></a><span data-ttu-id="5be8f-168">Exemple de transformation</span><span class="sxs-lookup"><span data-stu-id="5be8f-168">An Example Transform</span></span>

<span data-ttu-id="5be8f-169">Sur la base de l’exemple de jeu de données pour les capteurs de lumière ambiante précédemment fournis, vous pouvez obtenir l’équation suivante pour mapper les valeurs Lux à la perception humaine.</span><span class="sxs-lookup"><span data-stu-id="5be8f-169">Based on the sample data set for ambient light sensors previously provided, you could arrive at the following equation to map lux values to human perception.</span></span> <span data-ttu-id="5be8f-170">Dans cet exemple, la plage de valeurs attendue est comprise entre 0 Lux et 1 million Lux.</span><span class="sxs-lookup"><span data-stu-id="5be8f-170">In this example, the expected values range from 0 lux to 1,000,000 lux.</span></span>

![équation de valeur Lux](images/sensor-lux-equation.jpg)

<span data-ttu-id="5be8f-172">Cette équation donne des valeurs qui varient à peu près de manière linéaire entre 0,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="5be8f-172">This equation results in values that vary in a roughly linear fashion between 0.0 and 1.0.</span></span> <span data-ttu-id="5be8f-173">Ce résultat indique comment l’éclairage perçu par l’homme a été modifié en fonction de l’exemple de jeu de données indiqué précédemment.</span><span class="sxs-lookup"><span data-stu-id="5be8f-173">This result indicates how human-perceived lighting changed based on the example data set that was shown previously.</span></span>

 

 



