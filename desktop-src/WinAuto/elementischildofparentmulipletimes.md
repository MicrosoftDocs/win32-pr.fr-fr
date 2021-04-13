---
title: ElementIsChildOfParentMulipleTimes
description: ElementIsChildOfParentMulipleTimes
ms.assetid: B966ABE0-5109-4DAD-8125-EB4A3B3A5F61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da27c66027f7948dfa794c85dace015565d636c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197467"
---
# <a name="elementischildofparentmulipletimes"></a>ElementIsChildOfParentMulipleTimes

## <a name="text"></a>Texte

Le accParent de l’élément est ( {0} ), mais l’élément d’origine est une {1} heure enfant

## <a name="type"></a>Type

Error

## <a name="description"></a>Description

Lorsque la méthode [**\_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) est appelée sur l’élément cible, elle signale qu’elle est un enfant du même parent plusieurs fois.

Ce problème peut entraîner des problèmes de navigation pour les outils automatisés, car le parcours des éléments peut être erratique et imprévisible.

## <a name="possible-causes"></a>Causes possibles

Implémentation MSAA incorrecte ou non valide.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IAccessible :: \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




