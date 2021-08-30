---
title: VariantNotInt (CheckRole)
description: VariantNotInt (CheckRole)
ms.assetid: 24A9E91D-92E6-492B-B5CE-DF42E5923F60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66b5d06c42668e600b15019277ac7bacb3a07b2058e083b5de4964d1d6c46052
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098019"
---
# <a name="variantnotint-checkrole"></a>VariantNotInt (CheckRole)

## <a name="text"></a>Texte

La variante retournée par {0} doit être un {1} , mais est un {2} .

## <a name="type"></a>Type

Erreur

## <a name="description"></a>Description

Un élément signale un rôle MSAA non valide. Par exemple, la méthode [**obtenir \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) utilisée pour récupérer le rôle MSAA d’un élément doit retourner une valeur entière qui représente l’une des constantes de rôle MSAA, mais qui retourne une autre variante à la place.

Ce problème entraîne des problèmes pour les personnes qui reposent sur un lecteur d’écran et un clavier pour la navigation, car les éléments peuvent être identifiés incorrectement à l’utilisateur.

## <a name="possible-causes"></a>Causes possibles

Un rôle MSAA est défini de manière inappropriée pour l’élément ou son parent.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IAccessible :: \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[**Rôles d’objet**](object-roles.md)
</dt> </dl>

 

 




