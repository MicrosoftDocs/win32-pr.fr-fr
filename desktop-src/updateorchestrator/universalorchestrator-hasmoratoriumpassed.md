---
title: IUniversalOrchestrator::HasMoratoriumPassed
description: Interroge Universal Orchestrator pour déterminer si la période postérieure à OOBE a été dépassée.
ms.topic: reference
ms.date: 01/14/2021
ms.openlocfilehash: 61870e1bd57f54afded3f905da34ddc9198bcdb555c42adc4c799e08f2acf392
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966126"
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



 

 



