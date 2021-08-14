---
title: ElementIsChildOfParentMulipleTimes
description: ElementIsChildOfParentMulipleTimes
ms.assetid: B966ABE0-5109-4DAD-8125-EB4A3B3A5F61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfed0716423d8b1fef182be7cb0cb8ef122cf70cff6a574069fe40b63549f744
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118829548"
---
# <a name="elementischildofparentmulipletimes"></a>ElementIsChildOfParentMulipleTimes

## <a name="text"></a>Texte

Le accParent de l’élément est ( {0} ), mais l’élément d’origine est une {1} heure enfant

## <a name="type"></a>Type

Erreur

## <a name="description"></a>Description

Lorsque la méthode [**\_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) est appelée sur l’élément cible, elle signale qu’elle est un enfant du même parent plusieurs fois.

Ce problème peut entraîner des problèmes de navigation pour les outils automatisés, car le parcours des éléments peut être erratique et imprévisible.

## <a name="possible-causes"></a>Causes possibles

Implémentation MSAA incorrecte ou non valide.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IAccessible :: \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




