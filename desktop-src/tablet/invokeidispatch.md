---
description: Appelle la fonctionnalité d’assistance pour l’interface IDispatch.
ms.assetid: ccef47af-d9dd-48c3-93d3-ee997dacf7a8
title: InvokeIDispatch fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InvokeIDispatch
api_type:
- LibDef
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 9708ebc5675d918c959be132d16037ac4e128650280b8243dcfe5c48834b602b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118041869"
---
# <a name="invokeidispatch-function"></a>InvokeIDispatch fonction)

Appelle la fonctionnalité d’assistance pour l’interface IDispatch.

Cette fonction n’est pas destinée à être utilisée par le code d’application.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI InvokeIDispatch(
        IDispatch  *pDispatch,
        DISPID     dispid,
        DISPPARAMS *pDisp,
  _Out_ VARIANT    *pVarResult
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDispatch* 
</dt> <dd>

Instance de l’interface IDispatch.

</dd> <dt>

*égal* 
</dt> <dd>

Méthode, propriété ou argument à passer.

</dd> <dt>

*pDisp* 
</dt> <dd>

Paramètres à passer.

</dd> <dt>

*pVarResult* \[ à\]
</dt> <dd>

Structure qui reçoit les valeurs récupérées.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, elle retourne la valeur \_ OK. En cas d’échec, les codes de retour possibles incluent, sans s’y limiter, les valeurs indiquées dans le tableau suivant.



| Code de retour                                                                                  | Description                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | La valeur de *pDispatch* n’est pas valide.<br/> |



 

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                         |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                             |
| Bibliothèque<br/>                  | <dl> <dt>InkObj.dll</dt> </dl> |



 

 




