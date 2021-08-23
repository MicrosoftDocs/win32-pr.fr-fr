---
title: VariantNotInt (CheckState)
description: VariantNotInt (CheckState)
ms.assetid: 77140193-22E8-427D-AE9C-FEC6B93483DD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a3334a3609e9d64c1bb7109cc6f5bb52a2d09f9f9ac18cc41abf5d761f8e939
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052167"
---
# <a name="variantnotint-checkstate"></a>VariantNotInt (CheckState)

## <a name="text"></a>Texte

La variante retournée par {0} doit être un {1} , mais est un {2} .

## <a name="type"></a>Type

Erreur

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

 

 




