---
title: NullParent
description: NullParent
ms.assetid: F9563D73-66EF-4C66-8783-B034AA7A212E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f265f66eb4d0b0985d9f3979fc7ff4b9bb1812df1617cdaa4f6f50d7b357e067
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998149"
---
# <a name="nullparent"></a>NullParent

## <a name="text"></a>Texte

Les éléments parents ont la valeur NULL

## <a name="type"></a>Type

Erreur

## <a name="description"></a>Description

La valeur NULL est retournée lorsque la méthode [**\_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) est appelée sur l’élément. La méthode **obtenir \_ accParent** doit retourner la valeur NULL uniquement lorsqu’elle est appelée sur l’élément racine de la cible de vérification.

Ce problème peut entraîner des problèmes de navigation pour les outils automatisés, car le parcours des éléments peut être erratique et imprévisible.

## <a name="possible-causes"></a>Causes possibles

Implémentation MSAA incorrecte ou non valide.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IAccessible :: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> <dt>

[**IAccessible :: \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




