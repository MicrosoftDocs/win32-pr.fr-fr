---
title: InconsistentState, InconsistentProperties
description: InconsistentState, InconsistentProperties
ms.assetid: 82A2ECA8-0155-402A-A745-B97D3F633643
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30533125c342bd80134c9eab45f14917a3b3ad04af9d969140c49502cbfd192a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644839"
---
# <a name="inconsistentstate-inconsistentproperties"></a>InconsistentState, InconsistentProperties

## <a name="text"></a>Texte

Les États/propriétés d’un contrôle sont incohérents {0} et {1}

## <a name="type"></a>Type

Erreur

## <a name="description"></a>Description

Un élément signale des États MSAA incohérents ou incompatibles ou des propriétés UI Automation. Par exemple, lorsque la méthode [**obtenir \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) retourne l’une des combinaisons suivantes.

-   Système d’état \_ \_ développé et \_ système d’état \_ réduit
-   Système d’état \_ \_ sélectionné et non \_ \_ sélectionnable par le système
-   Système d’État axé sur le système d’état \_ \_ et non sur \_ le système d’état \_

Ce problème provoque des problèmes pour les personnes qui reposent sur un lecteur d’écran et un clavier pour la navigation, car un état d’élément incorrect peut être signalé à l’utilisateur.

## <a name="possible-causes"></a>Causes possibles

L’État MSAA de l’élément ou de son parent est incorrect.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IAccessible :: \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)
</dt> <dt>

[**Constantes d’état d’objet**](object-state-constants.md)
</dt> <dt>

[États et propriétés](uiauto-msaa.md)
</dt> </dl>

 

 




