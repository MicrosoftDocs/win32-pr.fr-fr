---
title: VariantNotInt (CheckRole)
description: VariantNotInt (CheckRole)
ms.assetid: 24A9E91D-92E6-492B-B5CE-DF42E5923F60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdca744468d863ff1ab95b66edf5b3ff1f40b48f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310150"
---
# <a name="variantnotint-checkrole"></a>VariantNotInt (CheckRole)

## <a name="text"></a>Texte

La variante retournée par {0} doit être un {1} , mais est un {2} .

## <a name="type"></a>Type

Error

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

 

 




