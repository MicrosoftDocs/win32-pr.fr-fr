---
title: AccessibleObjectFromPointReturnedNullIAccessible
description: AccessibleObjectFromPointReturnedNullIAccessible
ms.assetid: DF786659-8ADC-4EB0-A606-8B80C139691A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71963ad564454dcb90266b4fe4c63ba7282dbc514ab286629798420ff1db9f6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118327695"
---
# <a name="accessibleobjectfrompointreturnednulliaccessible"></a>AccessibleObjectFromPointReturnedNullIAccessible

## <a name="text"></a>Texte

AccessibleObjectFromPoint ( {0} , {1} ) a retourné la valeur null

## <a name="type"></a>Type

Erreur

## <a name="description"></a>Description

L’adresse de l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de l’élément d’interface utilisateur obtenue pour les coordonnées données est null.

## <a name="possible-causes"></a>Causes possibles

-   L’interaction de l’utilisateur pendant la vérification, telle que le déplacement du focus vers un HWND non cible, interfère avec le processus de vérification.
-   Implémentation MSAA incorrecte ou non valide.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Navigation via le test de positionnement et l’emplacement à l’écran](navigation-through-hit-testing-and-screen-location.md)
</dt> <dt>

[**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
</dt> </dl>

 

 




