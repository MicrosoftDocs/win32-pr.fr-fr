---
description: L’attribut stretchmode spécifie comment étirer une image qui ne correspond pas aux dimensions de sortie.
ms.assetid: 9a26bb8b-2b1c-424a-ae30-e175c60c76a1
title: Attribut stretchmode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed398fbe193ef262bdfc9a28cf66bef3a5b11f759d90c460cc99342ec7cd66b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903869"
---
# <a name="stretchmode-attribute"></a>Attribut stretchmode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

L' `stretchmode` attribut spécifie comment étirer une image qui ne correspond pas aux dimensions de sortie.

## <a name="possible-values"></a>Valeurs possibles

Doit avoir l’une des valeurs suivantes.

-   « Stretch » : l’image est étirée pour s’ajuster à la taille de l’image de sortie sans conserver les proportions. (Par défaut)
-   « Crop » : l’image est rognée pour s’ajuster à la taille de trame de sortie.
-   « preserveaspectratio » : les proportions d’origine sont conservées, avec une bandes noire le long de la dimension plus petite.
-   « preserveaspectrationoletterbox » : l’image est redimensionnée pour remplir l’intégralité du frame cible tout en préservant les proportions.

## <a name="applies-to"></a>S'applique à

[**capture**](clip-element.md)

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Attributs XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineSrc::SetStretchMode**](iamtimelinesrc-setstretchmode.md)
</dt> </dl>

 

 



