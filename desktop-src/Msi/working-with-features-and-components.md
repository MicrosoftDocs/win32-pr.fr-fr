---
description: Il existe plusieurs fonctions qui modifient l’installation des composants et fonctionnalités du produit. La rubrique suivante décrit comment modifier des fonctionnalités et des composants.
ms.assetid: 840656f9-ea85-49e7-8842-f779228c30d6
title: Utilisation des fonctionnalités et des composants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18b77fd93a9f2ee8181020f6c436d7e61e09a0f6d7858f0159fb70a7c7d8eeef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145172"
---
# <a name="working-with-features-and-components"></a>Utilisation des fonctionnalités et des composants

Il existe plusieurs fonctions qui modifient l’installation des [composants et fonctionnalités](components-and-features.md)du produit. La rubrique suivante décrit comment modifier des fonctionnalités et des composants.

**Pour modifier l’installation de fonctionnalités et de composants**

1.  Définissez le niveau d’installation d’un composant ou d’une fonctionnalité en appelant la fonction [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel) .

    Chaque fonctionnalité d’un package se voit attribuer un niveau d’installation dans le [tableau des fonctionnalités](feature-table.md). Si le niveau d’installation d’une fonctionnalité est inférieur au niveau défini par [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel), la fonctionnalité est sélectionnée pour l’installation. Une fois **MsiSetInstallLevel** appelé, vous pouvez définir explicitement si une fonctionnalité est installée.

2.  Déterminez les États disponibles pour une fonctionnalité spécifiée en appelant la fonction [**MsiGetFeatureValidStates**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa) .
3.  Obtenez l’espace disque requis pour une fonctionnalité spécifiée et ses fonctionnalités enfants en appelant la fonction [**MsiGetFeatureCost**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta) .
4.  Obtenir l’état actuel d’une fonctionnalité ou d’un composant en appelant la fonction [**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea) ou la fonction [**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea) .
5.  Modifiez l’état de la fonctionnalité ou du composant avec la fonction [**MsiSetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeaturestatea) ou la fonction [**MsiSetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea) .

 

 



