---
title: VariantNotInt (CheckState)
description: VariantNotInt (CheckState)
ms.assetid: 77140193-22E8-427D-AE9C-FEC6B93483DD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d951a51ae6aa3f4d9454fc95a56c76cfe30500c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196785"
---
# <a name="variantnotint-checkstate"></a>VariantNotInt (CheckState)

## <a name="text"></a>Texte

La variante retournée par {0} doit être un {1} , mais est un {2} .

## <a name="type"></a>Type

Error

## <a name="description"></a>Description

Un élément signale un État MSAA non valide. Par exemple, la méthode [**obtenir \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) utilisée pour récupérer l’État MSAA d’un élément doit retourner une valeur entière qui représente l’une des constantes d’État MSAA, mais qui retourne une autre variante à la place.

Ce problème provoque des problèmes pour les personnes qui reposent sur un lecteur d’écran et un clavier pour la navigation, car un état d’élément incorrect peut être signalé à l’utilisateur.

## <a name="possible-causes"></a>Causes possibles

L’État MSAA de l’élément ou de son parent est incorrect.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IAccessible :: \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)
</dt> <dt>

[**Constantes d’état d’objet**](object-state-constants.md)
</dt> </dl>

 

 




