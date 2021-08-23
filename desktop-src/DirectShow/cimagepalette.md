---
description: La classe CImagePalette gère les palettes pour les convertisseurs vidéo. Il peut être utilisé pour créer une palette logique à partir d’un format vidéo. Cette classe est destinée à être utilisée avec les classes CBaseWindow et CDrawImage. elle est donc un peu spécialisée.
ms.assetid: dcbe5049-0e8c-4221-825a-0fd8e6efd2a5
title: CImagePalette, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette
api_type:
- COM
api_location: ''
ms.openlocfilehash: 390bd4fc60e7d20264ae3a9238699108e7778524b73c6af22038197260da4463
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074063"
---
# <a name="cimagepalette-class"></a>CImagePalette, classe

La `CImagePalette` classe gère les palettes pour les convertisseurs vidéo. Il peut être utilisé pour créer une palette logique à partir d’un format vidéo. Cette classe est destinée à être utilisée avec les classes [**CBaseWindow**](cbasewindow.md) et [**CDrawImage**](cdrawimage.md) . elle est donc un peu spécialisée.



| Variables membres protégées                                       | Description                                                                                    |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**m \_ HPALETTE**](cimagepalette-m-hpalette.md)                  | Handle vers la palette logique gérée par cet objet.                                        |
| [**m \_ pBaseWindow**](cimagepalette-m-pbasewindow.md)            | Pointeur vers l’objet **CBaseWindow** qui gère la fenêtre.                                 |
| [**m \_ pDrawImage**](cimagepalette-m-pdrawimage.md)              | Pointeur vers l’objet **CDrawImage** qui dessine l’image vidéo.                               |
| [**m \_ pFilter**](cimagepalette-m-pfilter.md)                    | Pointeur désignant le filtre propriétaire.                                                                  |
| M&#233;thodes publiques                                                   | Description                                                                                    |
| [**CImagePalette**](cimagepalette-cimagepalette.md)             | Méthode de constructeur.                                                                            |
| [**CopyPalette**](cimagepalette-copypalette.md)                 | Copie la palette de toute structure **VIDEOINFO** vers toute structure en palette **VIDEOINFO** . |
| [**MakeIdentityPalette**](cimagepalette-makeidentitypalette.md) | Tente de créer une palette qui correspond directement à la palette sélectionnée dans le périphérique d’affichage.   |
| [**MakePalette**](cimagepalette-makepalette.md)                 | Crée une palette logique à partir de la table des couleurs dans un format vidéo.                              |
| [**PreparePalette**](cimagepalette-preparepalette.md)           | Configure une palette en fonction d’un type de média à partir du filtre propriétaire.                               |
| [**RemovePalette**](cimagepalette-removepalette.md)             | Supprime la palette logique existante.                                                          |



 

 

 



