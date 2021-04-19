---
title: IUniversalOrchestrator::HasMoratoriumPassed
description: Interroge Universal Orchestrator pour déterminer si la période postérieure à OOBE a été dépassée.
ms.topic: method
ms.date: 01/14/2021
ms.openlocfilehash: 2ed354d365b795a0c959396e6b26d6bc73baad97
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/21/2021
ms.locfileid: "106527717"
---
# <a name="iuniversalorchestratorhasmoratoriumpassed-method"></a>IUniversalOrchestrator :: HasMoratoriumPassed, méthode

> [!NOTE] 
> Cette API appartient à l’API Universal Orchestrator.

Permet aux clients de déterminer si Universal Orchestrator fonctionne immédiatement après le nouvel appareil, ce qui limite les tentatives de travail visant à minimiser l’interruption de l’utilisateur. 

## <a name="syntax"></a>Syntaxe

```C++
HRESULT HasMoratoriumPassed(
  LPCWSTR callerIdentifier,
  BOOL*   moratoriumPassed);
```

## <a name="parameters"></a>Paramètres

`callerIdentifier`

Chaîne unique qui identifie tous les appels de ce client spécifique.

`hasMoratoriumPassed`

Paramètre de sortie qui stocke le résultat de la requête.

## <a name="return-value"></a>Valeur retournée
Si cette méthode est réussie, elle retourne **S_OK**.  Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise

| Condition requise | Version |
|---|---|
| Client minimal pris en charge | Windows 10 1903 |
|   |   |



 

 



