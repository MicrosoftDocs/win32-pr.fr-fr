---
description: Cette section traite de l’utilisation des données de capteur d’éclairage ambiant et de la façon dont les fonctionnalités et le contenu de programme de l’interface utilisateur peuvent être optimisés pour de nombreuses conditions d’éclairage.
ms.assetid: c84075b2-ae41-4915-a0f6-3a9c017ae0b8
title: Création d' Light-Aware interfaces utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a4b6d404e366cb898114fe61729ab1ad722feb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952501"
---
# <a name="creating-light-aware-user-interfaces"></a><span data-ttu-id="2ac8c-103">Création d' Light-Aware interfaces utilisateur</span><span class="sxs-lookup"><span data-stu-id="2ac8c-103">Creating Light-Aware User Interfaces</span></span>

<span data-ttu-id="2ac8c-104">Cette section traite de l’utilisation des données de capteur d’éclairage ambiant et de la façon dont les fonctionnalités et le contenu de programme de l’interface utilisateur peuvent être optimisés pour de nombreuses conditions d’éclairage.</span><span class="sxs-lookup"><span data-stu-id="2ac8c-104">This section covers the use of ambient light sensor data, and how user interface features and program content can be optimized for many lighting conditions.</span></span>

<span data-ttu-id="2ac8c-105">Les capteurs de lumière ambiante exposent des données qui peuvent être utilisées pour déterminer divers aspects des conditions d’éclairage où se trouve le capteur.</span><span class="sxs-lookup"><span data-stu-id="2ac8c-105">Ambient light sensors expose data that can be used to determine various aspects of the lighting conditions where the sensor is located.</span></span> <span data-ttu-id="2ac8c-106">Les capteurs de lumière ambiante peuvent exposer la luminosité globale d’un environnement (éclairage) et d’autres aspects de la lumière environnante, tels que la chromatique ou la température de couleur.</span><span class="sxs-lookup"><span data-stu-id="2ac8c-106">Ambient light sensors can expose the overall brightness of an environment (illuminance) and other aspects of the surrounding light, such as chromaticity or color temperature.</span></span>

<span data-ttu-id="2ac8c-107">Les ordinateurs peuvent être plus utiles à plusieurs égards lorsque le système répond à des conditions d’éclairage.</span><span class="sxs-lookup"><span data-stu-id="2ac8c-107">Computers can be more useful in several ways when the system is responsive to lighting conditions.</span></span> <span data-ttu-id="2ac8c-108">Cela inclut le contrôle de la luminosité de l’écran de l’ordinateur (une nouvelle fonctionnalité entièrement prise en charge dans Windows 7), l’ajustement automatique du niveau d’éclairage des claviers allumés et même la luminosité pour d’autres lumières (comme l’éclairage du bouton, les indicateurs d’activité, etc.).</span><span class="sxs-lookup"><span data-stu-id="2ac8c-108">These include controlling the brightness of the computer display (a new, fully supported feature in Windows 7), automatically adjusting the lighting level of illuminated keyboards, and even brightness control for other lights (such as button illumination, activity lights, and so on).</span></span>

<span data-ttu-id="2ac8c-109">Les programmes de l’utilisateur final peuvent également bénéficier de capteurs légers.</span><span class="sxs-lookup"><span data-stu-id="2ac8c-109">End-user programs can also benefit from light sensors.</span></span> <span data-ttu-id="2ac8c-110">Les programmes peuvent appliquer un thème adapté à une condition d’éclairage particulière, par exemple un thème d’extérieur spécifique et un thème d’intérieur.</span><span class="sxs-lookup"><span data-stu-id="2ac8c-110">Programs can apply a theme that is appropriate for a particular lighting condition, such as a specific outdoor theme and indoor theme.</span></span> <span data-ttu-id="2ac8c-111">L’aspect le plus important de l’intégration de capteur de lumière avec les programmes est peut-être l’optimisation de lisibilité et de lisibilité basée sur des conditions d’éclairage.</span><span class="sxs-lookup"><span data-stu-id="2ac8c-111">Perhaps the most important aspect of light sensor integration with programs is readability and legibility optimizations that are based on lighting conditions.</span></span>

<span data-ttu-id="2ac8c-112">L’API de capteur vous permet de créer des programmes de ce type.</span><span class="sxs-lookup"><span data-stu-id="2ac8c-112">The Sensor API enables you to create such programs.</span></span> <span data-ttu-id="2ac8c-113">Considérons le scénario suivant.</span><span class="sxs-lookup"><span data-stu-id="2ac8c-113">Consider the following scenario.</span></span>

## <a name="scenario-using-your-laptop-to-navigate-to-a-restaurant"></a><span data-ttu-id="2ac8c-114">Scénario : utilisation de votre ordinateur portable pour accéder à un restaurant</span><span class="sxs-lookup"><span data-stu-id="2ac8c-114">Scenario: Using your Laptop to Navigate to a Restaurant</span></span>

<span data-ttu-id="2ac8c-115">Supposons que vous souhaitiez utiliser votre ordinateur pour vous aider à accéder à un nouveau restaurant.</span><span class="sxs-lookup"><span data-stu-id="2ac8c-115">Suppose you want to use your computer to help you navigate to a new restaurant.</span></span> <span data-ttu-id="2ac8c-116">Vous commencez dans votre maison, en recherchant l’adresse du restaurant et en planifiant votre itinéraire.</span><span class="sxs-lookup"><span data-stu-id="2ac8c-116">You start out in your house, looking up the address of the restaurant and planning your route.</span></span> <span data-ttu-id="2ac8c-117">La capture d’écran suivante montre comment votre programme de navigation peut optimiser son interface utilisateur pour afficher des informations détaillées dans des conditions d’éclairage intérieurs.</span><span class="sxs-lookup"><span data-stu-id="2ac8c-117">The following screen shot shows how your navigation program could optimize its UI to show detailed information in indoor lighting conditions.</span></span>

![interface utilisateur conçue pour l’éclairage intérieur.](images/nav-normal.png)

<span data-ttu-id="2ac8c-119">Lorsque vous êtes en dehors de votre voiture, vous rencontrez un soleil direct, ce qui rend l’écran de l’ordinateur portable difficile à lire.</span><span class="sxs-lookup"><span data-stu-id="2ac8c-119">When you go outside to your car, you encounter direct sunlight, which makes the laptop's screen difficult to read.</span></span> <span data-ttu-id="2ac8c-120">La capture d’écran suivante montre comment votre programme peut modifier son interface utilisateur pour optimiser la lisibilité et la lisibilité en clair.</span><span class="sxs-lookup"><span data-stu-id="2ac8c-120">The following screen shot shows how your program could alter its UI to maximize legibility/readability in direct light.</span></span> <span data-ttu-id="2ac8c-121">Dans cette vue, la plupart des détails ont été omis et le contraste est agrandi.</span><span class="sxs-lookup"><span data-stu-id="2ac8c-121">In this view, much of the detail has been omitted and contrast is maximized.</span></span>

![interface utilisateur conçue pour les conditions d’éclairage direct.](images/nav-contrast.png)

<span data-ttu-id="2ac8c-123">À mesure que vous vous rapprochez du restaurant, les approches de la soirée se déplacent à l’extérieur.</span><span class="sxs-lookup"><span data-stu-id="2ac8c-123">As you get closer to the restaurant, evening approaches and it gets dark outside.</span></span> <span data-ttu-id="2ac8c-124">Dans la capture d’écran suivante, l’interface utilisateur du programme de navigation a été optimisée pour un affichage de faible luminosité.</span><span class="sxs-lookup"><span data-stu-id="2ac8c-124">In the following screen shot, the UI for the navigation program has been optimized for low-light viewing.</span></span> <span data-ttu-id="2ac8c-125">En utilisant les couleurs plus sombres, cette interface utilisateur est facile à visualiser dans la voiture sombre.</span><span class="sxs-lookup"><span data-stu-id="2ac8c-125">By using darker colors overall, this UI is easy to glance at in the dark car.</span></span>

![interface utilisateur conçue pour un affichage de faible luminosité.](images/nav-lowlight.png)

<span data-ttu-id="2ac8c-127">Dans la suite de cette section, vous allez découvrir quelques opérations que vous pouvez effectuer pour optimiser vos programmes en fonction des conditions d’éclairage et de la façon dont vous pouvez utiliser l’API de capteur pour faciliter l’utilisation de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2ac8c-127">In the remainder of this section, you will explore some things that you can do to optimize your programs for various lighting conditions and how you can use the Sensor API to help enable light-aware UI.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2ac8c-128">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="2ac8c-128">In This Section</span></span>

-   [<span data-ttu-id="2ac8c-129">Notions de base des interfaces utilisateur Light-Aware</span><span class="sxs-lookup"><span data-stu-id="2ac8c-129">Fundamentals of Light-Aware User Interfaces</span></span>](fundamentals-of-light-aware-user-interfaces.md)
-   [<span data-ttu-id="2ac8c-130">Exemples d’interfaces utilisateur Light-Aware</span><span class="sxs-lookup"><span data-stu-id="2ac8c-130">Examples of Light-Aware User Interfaces</span></span>](examples-of-light-aware-user-interfaces.md)
-   [<span data-ttu-id="2ac8c-131">Optimisation de l’expérience utilisateur</span><span class="sxs-lookup"><span data-stu-id="2ac8c-131">Optimizing the User Experience</span></span>](optimizing-the-user-experience.md)
-   [<span data-ttu-id="2ac8c-132">Compréhension et interprétation des valeurs LX</span><span class="sxs-lookup"><span data-stu-id="2ac8c-132">Understanding and Interpreting Lux Values</span></span>](understanding-and-interpreting-lux-values.md)
-   [<span data-ttu-id="2ac8c-133">Utilisation des données de capteur de lumière</span><span class="sxs-lookup"><span data-stu-id="2ac8c-133">Using Light Sensor Data</span></span>](handling-data-from-multiple-light-sensors.md)

 

 



