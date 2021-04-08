---
title: AccessibleObjectFromPointReturnedNullChildId
description: AccessibleObjectFromPointReturnedNullChildId
ms.assetid: 20511B76-736B-4B43-8DC3-4306DF74CF73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e03c708d13bd8abfe642b99310c8b5bea176e11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675665"
---
# <a name="accessibleobjectfrompointreturnednullchildid"></a>AccessibleObjectFromPointReturnedNullChildId

## <a name="text"></a>Texte

AccessibleObjectFromPoint ( {0} , {1} ) a retourné un childID null

## <a name="type"></a>Type

Error

## <a name="description"></a>Description

Le ChildId de l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de l’objet obtenu pour les coordonnées données a la valeur null.

## <a name="possible-causes"></a>Causes possibles

L’interaction de l’utilisateur pendant la vérification, telle que le déplacement du focus vers un HWND non cible, interfère avec le processus de vérification.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Navigation via le test de positionnement et l’emplacement à l’écran](navigation-through-hit-testing-and-screen-location.md)
</dt> <dt>

[**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
</dt> </dl>

 

 




