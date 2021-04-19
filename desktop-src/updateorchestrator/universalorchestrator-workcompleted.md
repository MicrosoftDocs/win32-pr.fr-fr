---
title: IUniversalOrchestrator::WorkCompleted
description: Appelle Universal Orchestrator pour indiquer que le travail est terminé
ms.topic: method
ms.date: 01/14/2021
ms.openlocfilehash: 8d4a08e7f021811e59a182a8b726397476b78433
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/21/2021
ms.locfileid: "106542069"
---
# <a name="iuniversalorchestratorworkcompleted-method"></a>IUniversalOrchestrator :: WorkCompleted, méthode

> [!NOTE] 
> Cette API appartient à l’API Universal Orchestrator.

Permet aux clients d’informer Universal Orchestrator que le travail précédemment planifié a été effectué et d’arrêter les rappels pour effectuer le travail jusqu’au prochain appel ScheduleWork réussi.

## <a name="syntax"></a>Syntaxe

```C++
HRESULT WorkCompleted(
  LPCWSTR callerIdentifier,
  BOOL    workCompleted);
```

## <a name="parameters"></a>Paramètres

`callerIdentifier`

Chaîne unique qui identifie tous les appels de ce client spécifique.

`workCompleted`

**True** si le travail s’est terminé avec succès. Sinon, **false** si la tentative de travail a échoué et doit être retentée à l’avenir. 

## <a name="return-value"></a>Valeur retournée
Si cette méthode est réussie, elle retourne **S_OK**.  Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise

| Condition requise | Version |
|---|---|
| Client minimal pris en charge | Windows 10 1903 |
|   |   |



 

 



