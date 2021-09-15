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
ms.openlocfilehash: 950d96ac46c18d741d5cf2337326f116fb79e36a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522320"
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

## <a name="return-value"></a>Valeur de retour

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

La seule valeur prise en charge pour *ptcfCategory* est 0x08000000.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Windows Server 2016 \[ applications de bureau uniquement\]<br/>                                           |
| DLL<br/>                      | <dl> <dt>ExecModelClient.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TaskCompletionClient**](taskcompletionclient.md)
</dt> </dl>

 

 




