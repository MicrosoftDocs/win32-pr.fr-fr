---
description: respectez les consignes suivantes lors de la création d’un correctif pour une Windows Installer petite mise à jour.
ms.assetid: 0e57c2aa-e86a-4161-9749-c7963182a6d5
title: Création d’un correctif de mise à jour de petite taille
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b2c3dffac099358b924914b5dbd86871ba370241c42a2e3fd5caef2d8f12ff4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118379394"
---
# <a name="creating-a-small-update-patch"></a>Création d’un correctif de mise à jour de petite taille

Lors de la création d’un correctif pour les [petites mises à jour](small-updates.md), les auteurs doivent respecter les instructions suivantes :

-   Les correctifs de petite mise à jour doivent être conçus pour une installation cible unique.
-   Les correctifs de petite mise à jour doivent utiliser la version la plus ancienne comme installation cible.
-   Un correctif logiciel de petite mise à jour doit remplacer et rendre obsolète les correctifs de mise à jour antérieurs.

Le scénario suivant illustre le meilleur choix d’un correctif de mise à jour de petite taille.

Votre société livre la version 1,0 de Myproduct.msi. Nous vous fournissons bientôt un correctif de [mise à jour de petite taille](small-updates.md) pour Myproduct.msi appelé qfe1. Cela ne modifie pas la propriété [**ProductCode**](productcode.md) ou [**ProductVersion**](productversion.md) .

Plus tard, vous créerez un deuxième correctif de [mise à jour](small-updates.md) pour Myproduct.msi appelé QFE2. Ce deuxième correctif doit cibler la version 1,0 de Myproduct.msi. Ce deuxième correctif ne doit pas cibler à la fois Myproduct.msi version 1,0 et Myproduct.msi version 1,0 + QFE1. Lorsque QFE2 est appliqué, il doit supprimer QFE1.

 

 



