---
title: IUniversalOrchestrator::WorkCompleted
description: Appelle Universal Orchestrator pour indiquer que le travail est terminé
ms.topic: reference
ms.date: 01/14/2021
ms.openlocfilehash: 5094ae864b4df9a3dd53b90c3b7d099a206a0ad8db1d1176b603b5ba45ca8194
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966072"
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



 

 



