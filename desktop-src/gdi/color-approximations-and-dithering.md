---
description: Bien qu’une application puisse utiliser la couleur sans tenir compte des capacités de couleur de l’appareil, le résultat obtenu peut ne pas être aussi instructif et agréable que la sortie pour laquelle la couleur est choisie soigneusement.
ms.assetid: 008c8a8e-3456-4727-9b27-00b20ae880a2
title: Approximations de couleurs et tramage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a72e28dbc3ce20a42b53b5ff060d950719e2d861
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127520072"
---
# <a name="color-approximations-and-dithering"></a>Approximations de couleurs et tramage

Bien qu’une application puisse utiliser la couleur sans tenir compte des capacités de couleur de l’appareil, le résultat obtenu peut ne pas être aussi instructif et agréable que la sortie pour laquelle la couleur est choisie soigneusement. Peu, le cas échéant, les appareils garantissent une correspondance exacte pour chaque valeur de couleur possible ; par conséquent, si une application demande une couleur que l’appareil ne peut pas générer, le système se rapproche de cette couleur à l’aide d’une couleur que l’appareil peut générer. Par exemple, si une application tente de créer un stylet rouge pour une imprimante noir et blanc, elle reçoit un stylet noir. le système utilise alors le noir comme approximation pour le rouge.

Une application peut déterminer si le système doit arrondir une couleur donnée à l’aide de la fonction [**GetNearestColor**](/windows/desktop/api/Wingdi/nf-wingdi-getnearestcolor) . La fonction prend une valeur de couleur et retourne la valeur de couleur de la couleur de correspondance la plus proche que l’appareil peut générer. La méthode utilisée par le système pour déterminer cette approximation dépend du pilote de périphérique et de ses fonctionnalités de couleur. Dans la plupart des cas, l’intensité globale de la couleur approximative est la plus proche de celle de la couleur demandée.

Quand une application crée un stylet ou définit la couleur du texte, le système se rapproche toujours d’une couleur si aucune correspondance exacte n’existe. Quand une application crée un pinceau plein, le système peut tenter de simuler la couleur demandée par le biais du tramage. Le *tramage* simule une couleur en alternant au moins deux couleurs dans un modèle. Par exemple, différentes nuances de rose peuvent être simulées en alternant différentes combinaisons de rouge et de blanc. Selon les couleurs et le modèle, le tramage peut produire des simulations raisonnables. Elle est particulièrement utile pour les appareils monochromes, car elle augmente le nombre de « couleurs » disponibles au-delà du noir et du blanc simples.

La méthode utilisée pour créer des couleurs dépendantes dépend du pilote de périphérique. La plupart des pilotes de périphérique utilisent un algorithme de tramage standard, qui génère un modèle en fonction des valeurs d’intensité des couleurs rouge, vert et bleu demandées. En général, toute couleur demandée qui ne peut pas être générée par l’appareil est sujette à la simulation, mais une application n’est pas avertie lorsque le système simule une couleur. En outre, une application ne peut pas modifier ou modifier l’algorithme de tramage du pilote de périphérique. Toutefois, une application peut contourner l’algorithme en créant et en utilisant des pinceaux de modèle. De cette façon, l’application crée ses propres couleurs en combinant des couleurs unies dans le bitmap qu’elle utilise pour créer le pinceau.

 

 



