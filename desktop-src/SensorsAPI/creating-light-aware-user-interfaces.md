---
description: Cette section traite de l’utilisation des données de capteur d’éclairage ambiant et de la façon dont les fonctionnalités et le contenu de programme de l’interface utilisateur peuvent être optimisés pour de nombreuses conditions d’éclairage.
ms.assetid: c84075b2-ae41-4915-a0f6-3a9c017ae0b8
title: Création d' Light-Aware interfaces utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bd97bb304c3a8718ae4b32d8b9100a1e7eb7a18240b9089c112272f588ee209
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118890283"
---
# <a name="creating-light-aware-user-interfaces"></a>Création d' Light-Aware interfaces utilisateur

Cette section traite de l’utilisation des données de capteur d’éclairage ambiant et de la façon dont les fonctionnalités et le contenu de programme de l’interface utilisateur peuvent être optimisés pour de nombreuses conditions d’éclairage.

Les capteurs de lumière ambiante exposent des données qui peuvent être utilisées pour déterminer divers aspects des conditions d’éclairage où se trouve le capteur. Les capteurs de lumière ambiante peuvent exposer la luminosité globale d’un environnement (éclairage) et d’autres aspects de la lumière environnante, tels que la chromatique ou la température de couleur.

Les ordinateurs peuvent être plus utiles à plusieurs égards lorsque le système répond à des conditions d’éclairage. cela inclut le contrôle de la luminosité de l’écran de l’ordinateur (une nouvelle fonctionnalité entièrement prise en charge dans Windows 7), l’ajustement automatique du niveau d’éclairage des claviers allumés et le contrôle de la luminosité pour d’autres lumières (telles que l’éclairage du bouton, les indicateurs d’activité, etc.).

Les programmes de l’utilisateur final peuvent également bénéficier de capteurs légers. Les programmes peuvent appliquer un thème adapté à une condition d’éclairage particulière, par exemple un thème d’extérieur spécifique et un thème d’intérieur. L’aspect le plus important de l’intégration de capteur de lumière avec les programmes est peut-être l’optimisation de lisibilité et de lisibilité basée sur des conditions d’éclairage.

L’API de capteur vous permet de créer des programmes de ce type. Considérons le scénario suivant.

## <a name="scenario-using-your-laptop-to-navigate-to-a-restaurant"></a>Scénario : utilisation de votre ordinateur portable pour accéder à un restaurant

Supposons que vous souhaitiez utiliser votre ordinateur pour vous aider à accéder à un nouveau restaurant. Vous commencez dans votre maison, en recherchant l’adresse du restaurant et en planifiant votre itinéraire. La capture d’écran suivante montre comment votre programme de navigation peut optimiser son interface utilisateur pour afficher des informations détaillées dans des conditions d’éclairage intérieurs.

![interface utilisateur conçue pour l’éclairage intérieur.](images/nav-normal.png)

Lorsque vous êtes en dehors de votre voiture, vous rencontrez un soleil direct, ce qui rend l’écran de l’ordinateur portable difficile à lire. La capture d’écran suivante montre comment votre programme peut modifier son interface utilisateur pour optimiser la lisibilité et la lisibilité en clair. Dans cette vue, la plupart des détails ont été omis et le contraste est agrandi.

![interface utilisateur conçue pour les conditions d’éclairage direct.](images/nav-contrast.png)

À mesure que vous vous rapprochez du restaurant, les approches de la soirée se déplacent à l’extérieur. Dans la capture d’écran suivante, l’interface utilisateur du programme de navigation a été optimisée pour un affichage de faible luminosité. En utilisant les couleurs plus sombres, cette interface utilisateur est facile à visualiser dans la voiture sombre.

![interface utilisateur conçue pour un affichage de faible luminosité.](images/nav-lowlight.png)

Dans la suite de cette section, vous allez découvrir quelques opérations que vous pouvez effectuer pour optimiser vos programmes en fonction des conditions d’éclairage et de la façon dont vous pouvez utiliser l’API de capteur pour faciliter l’utilisation de l’interface utilisateur.

## <a name="in-this-section"></a>Dans cette section

-   [Notions de base des interfaces utilisateur Light-Aware](fundamentals-of-light-aware-user-interfaces.md)
-   [Exemples d’interfaces utilisateur Light-Aware](examples-of-light-aware-user-interfaces.md)
-   [Optimisation de l’expérience utilisateur](optimizing-the-user-experience.md)
-   [Compréhension et interprétation des valeurs LX](understanding-and-interpreting-lux-values.md)
-   [Utilisation des données de capteur de lumière](handling-data-from-multiple-light-sensors.md)

 

 



