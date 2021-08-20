---
title: AccessibleObjectFromPointReturnedNullChildId
description: AccessibleObjectFromPointReturnedNullChildId
ms.assetid: 20511B76-736B-4B43-8DC3-4306DF74CF73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fb6ebf33cdfdef7b6e32ec4b9943accc06551d5f37f625fa77cb22e01b913df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994359"
---
# <a name="accessibleobjectfrompointreturnednullchildid"></a>AccessibleObjectFromPointReturnedNullChildId

## <a name="text"></a>Texte

AccessibleObjectFromPoint ( {0} , {1} ) a retourné un childID null

## <a name="type"></a>Type

Erreur

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

 

 




