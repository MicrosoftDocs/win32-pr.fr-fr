---
description: Fonction de rappel utilisée pour informer l’hôte de résultats d’une action (par exemple, capturer un frame) qu’elle a demandée.
MS-HAID: vspixengine.IRunActionCallback\_RequestResult\_IUnknown\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IRunActionCallback :: RequestResult, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5D6B1599-2CF4-46E7-92DB-5D93DD5AD0EE
api_name:
- IRunActionCallback.RequestResult
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9f7647daf828bb5d6ecc6f8200a24f9b02d70ae1933cdf7eb00162f24e80320a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892349"
---
# <a name="span-idvspixengineirunactioncallback_requestresult_iunknown_ptrspanirunactioncallbackrequestresult-method"></a><span id="vspixengine.irunactioncallback_requestresult_iunknown_ptr"></span>IRunActionCallback :: RequestResult, méthode

Fonction de rappel utilisée pour informer l’hôte de résultats d’une action (par exemple, capturer un frame) qu’elle a demandée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RequestResult(
   IUnknown * actionResult
);
```

## <a name="parameters"></a>Paramètres

*actionResult*   
Résultat de l’action.

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Voir aussi

[**IRunActionCallback**](/windows/desktop/direct3dtools/irunactioncallback)

 

 
