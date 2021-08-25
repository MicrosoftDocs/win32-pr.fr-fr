---
description: Commence l’achèvement de la tâche.
ms.assetid: 75C84DD9-D815-45C2-A28E-EAE437EAFF89
title: 'TaskCompletionClient :: ApplyTaskCompletion, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TaskCompletionClient.ApplyTaskCompletion
api_type:
- COM
api_location:
- ExecModelClient.dll
ms.openlocfilehash: 58c95144077697f1655547a58571ce3475355aa96040ce1815bd3178bc9a1290
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773669"
---
# <a name="taskcompletionclientapplytaskcompletion-method"></a>TaskCompletionClient :: ApplyTaskCompletion, méthode

Commence l’achèvement de la tâche.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ApplyTaskCompletion(
    UINT32   ptcfCategory
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ptcfCategory* 
</dt> <dd>

Valeur qui indique la catégorie de la tâche.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

La seule valeur prise en charge pour *ptcfCategory* est 0x08000000.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Windows Server 2016 \[ applications de bureau uniquement\]<br/>                                           |
| DLL<br/>                      | <dl> <dt>ExecModelClient.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TaskCompletionClient**](taskcompletionclient.md)
</dt> </dl>

 

 




