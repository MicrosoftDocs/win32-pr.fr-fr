---
title: Durée de vie du contexte de l’opération et Threading
description: La durée de vie du contexte d’opération, représentée par \_ un \_ handle de contexte de l’opération WS, détermine la durée de vie des propriétés qu’il contient.
ms.assetid: 37caf382-2b33-464d-b6c1-e4bd3271a5aa
keywords:
- Durée de vie du contexte de l’opération et services Web de Threading pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ea27b0b1dc41ccd029df7d726fe92631adc1ee4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522841"
---
# <a name="operation-context-lifetime-and-threading"></a>Durée de vie du contexte de l’opération et Threading

La durée de vie du contexte d’opération, représentée par un handle de [ \_ \_ contexte de l’opération WS](ws-operation-context.md) , détermine la durée de vie des propriétés qu’il contient. Par conséquent, un contexte ne doit être utilisé qu’au cours de la durée de vie de l' [opération de service](service-operation.md) ou du rappel auquel son fourni. La durée de vie d’un appel synchrone est l’exécution de la fonction elle-même. Pour un appel asynchrone, la durée de vie se termine une fois l’appel asynchrone terminé. Le modèle de service ne fournit aucune garantie sur le contexte une fois l’appel terminé. Le comportement de la confiance sur le contexte de l’opération ou sur l’une de ses propriétés au-delà de sa durée de vie n’est pas défini.


Voir aussi la calculatrice basée sur la session exemple, [SessionfullCalculatorServiceExample](sessionfullcalculatorserviceexample.md).

## <a name="threading-model"></a>Modèle de thread

Le contexte d’opération prend en charge le Threading libre, mais cela est vrai pour le contexte d’opération lui-même et ne s’applique à aucune des propriétés qu’il contient.

Lorsque vous inscrivez un rappel d’annulation pour une opération de service à l’aide de la fonction [**WsRegisterOperationForCancel**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) , Notez que la première inscription réussira. Toutefois, la définition du rappel d’annulation à plusieurs moments échoue.

 

 




