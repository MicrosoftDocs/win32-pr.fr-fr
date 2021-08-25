---
title: InvalidRole
description: InvalidRole
ms.assetid: B0707B90-59D6-4F86-8CBB-1DF57FDBEE31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1acecf91e90f93ccb1d220e9b2d91cbaa012b8d436b18a910daa73bf6ca3f1fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859999"
---
# <a name="invalidrole"></a>InvalidRole

## <a name="text"></a>Texte

Le entier retourné par la fonction obtenir \_ accRole n’est pas une constante Role valide, système de rôle IE \_\_\*

## <a name="type"></a>Type

Erreur

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

 

 




