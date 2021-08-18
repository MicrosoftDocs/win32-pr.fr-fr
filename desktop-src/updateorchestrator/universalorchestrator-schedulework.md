---
title: IUniversalOrchestrator::ScheduleWork
description: Appelle Universal Orchestrator pour planifier le travail
ms.topic: reference
ms.date: 01/14/2021
ms.openlocfilehash: bb2ecc67167e0651663856354a07ec86f985c664f1d2bccff98917adf72f054d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966081"
---
# <a name="iuniversalorchestratorschedulework-method"></a>IUniversalOrchestrator :: ScheduleWork, méthode

> [!NOTE] 
> Cette API appartient à l’API Universal Orchestrator.

Permet aux clients d’informer Universal Orchestrator que le travail est en attente et de fournir un fichier binaire qui sera appelé par Universal Orchestrator pour effectuer la mise à jour ultérieurement.

Le binaire de rappel doit être signé avec un certificat Microsoft valide, et l’appelant doit appeler l’appel ScheduleWork à partir du contexte système.

## <a name="syntax"></a>Syntaxe

```C++
HRESULT ScheduleWork(
  LPCWSTR callerIdentifier,
  LPCWSTR cmdLine
  LPCWSTR startArg,
  LPCWSTR pauseArg);
```

## <a name="parameters"></a>Paramètres

`callerIdentifier`

Chaîne unique qui identifie tous les appels de ce client spécifique.

`cmdLine`

Chemin d’accès complet au fichier binaire de rappel qui sera appelé par Universal Orchestrator pour effectuer le travail.

`startArg`

Paramètres à passer au binaire de rappel pour indiquer que Start est demandé.

`pauseArg`

*(facultatif)* Paramètres à passer au binaire de rappel pour indiquer qu’une pause est demandée.

## <a name="return-value"></a>Valeur retournée
Si cette méthode est réussie, elle retourne **S_OK**.  Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise

| Condition requise | Version |
|---|---|
| Client minimal pris en charge | Windows 10 1903 |
|   |   |



 

 



