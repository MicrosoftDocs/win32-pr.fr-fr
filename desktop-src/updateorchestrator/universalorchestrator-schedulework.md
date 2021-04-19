---
title: IUniversalOrchestrator::ScheduleWork
description: Appelle Universal Orchestrator pour planifier le travail
ms.topic: method
ms.date: 01/14/2021
ms.openlocfilehash: 456df8f975114f7bdf750a0449f3bd98efcc3b2e
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/21/2021
ms.locfileid: "106525764"
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



 

 



