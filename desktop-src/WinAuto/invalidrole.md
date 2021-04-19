---
title: InvalidRole
description: InvalidRole
ms.assetid: B0707B90-59D6-4F86-8CBB-1DF57FDBEE31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 531aa9917bd68b615c2cd2457d7a24bfc4af336c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510602"
---
# <a name="invalidrole"></a>InvalidRole

## <a name="text"></a>Texte

Le entier retourné par la fonction obtenir \_ accRole n’est pas une constante Role valide, système de rôle IE \_\_\*

## <a name="type"></a>Type

Error

## <a name="description"></a>Description

Un élément signale un rôle MSAA non valide. Par exemple, la méthode [**obtenir \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) retourne une valeur entière qui n’est pas mappée à une constante de rôle d’objet valide (par exemple, ListItem de système de rôle \_ \_ ).

Ce problème entraîne des problèmes pour les personnes qui reposent sur un lecteur d’écran et un clavier pour la navigation, car les éléments peuvent être identifiés incorrectement à l’utilisateur.

## <a name="possible-causes"></a>Causes possibles

Un rôle MSAA est défini de manière inappropriée pour l’élément ou son parent.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IAccessible :: \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[**Rôles d’objet**](object-roles.md)
</dt> </dl>

 

 




