---
title: ElementIsNotChildOfElementsParent
description: ElementIsNotChildOfElementsParent
ms.assetid: DFD5CC2A-B5F4-49F2-B3EF-2CD447A575E2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c5a3d62a6ae656bffffca442ed3cbb9b85be8dc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380428"
---
# <a name="elementisnotchildofelementsparent"></a>ElementIsNotChildOfElementsParent

## <a name="text"></a>Texte

L’élément n’est pas un enfant de son parent

## <a name="type"></a>Type

Error

## <a name="description"></a>Description

Lorsque la méthode [**\_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) est appelée sur l’élément enfant retourné par [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) (à l’aide des \_ constantes de navigation NAVDIR firstChild ou NAVDIR \_ LastChild), l’élément parent retourné ne correspond pas à l’élément parent spécifié dans l’appel **accNavigate** .

Ce problème peut entraîner des problèmes de navigation pour les outils automatisés, car le parcours des éléments peut être erratique et imprévisible.

## <a name="possible-causes"></a>Causes possibles

Implémentation MSAA incorrecte ou non valide.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IAccessible :: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> <dt>

[**IAccessible :: \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




