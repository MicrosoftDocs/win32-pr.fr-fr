---
description: Termine une demande asynchrone pour annuler l’inscription d’une file d’attente de travail à l’aide d’une tâche du service Planificateur de classes multimédias (MMCSS).
ms.assetid: 0E8F9BF6-AC1E-4FC0-BFAE-F292C4859F1F
title: RtwqEndUnregisterWorkQueueWithMMCSS fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtwqEndUnregisterWorkQueueWithMMCSS
api_type:
- DllExport
api_location:
- RTWorkQ.dll
ms.openlocfilehash: 083f0ca787bb842850320b9dd1d320ef4d5b172ee0b6d9b117296e58b991bd0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117793399"
---
# <a name="rtwqendunregisterworkqueuewithmmcss-function"></a>RtwqEndUnregisterWorkQueueWithMMCSS fonction)

Termine une demande asynchrone pour annuler l’inscription d’une file d’attente de travail à l’aide d’une tâche du service Planificateur de classes multimédias (MMCSS).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI RtwqEndUnregisterWorkQueueWithMMCSS(
    IMFAsyncResult  *pResult 
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pResult* 
</dt> <dd>

Pointeur vers l’interface [**IMFAsyncResult**](/windows/win32/api/mfobjects/nn-mfobjects-imfasyncresult) . Transmettez le même pointeur que celui reçu dans la méthode [**IRtwqAsyncCallback :: Invoke**](/windows/win32/api/rtworkq/nf-rtworkq-irtwqasynccallback-invoke) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Aucun</dt> </dl>        |
| Bibliothèque<br/>                  | <dl> <dt>Rtworkq. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RTWorkQ.dll</dt> </dl> |



 

 
