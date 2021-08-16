---
title: Méthode IBackgroundCopyError GetError (Deliveryoptimization. h)
description: Récupère le code d’erreur et identifie le contexte dans lequel l’erreur s’est produite.
ms.assetid: C87897CD-9648-4CEF-B963-68EE35356929
keywords:
- Méthode GetError
- Méthode GetError, interface IBackgroundCopyError
- Interface IBackgroundCopyError, méthode GetError
topic_type:
- apiref
api_name:
- IBackgroundCopyError.GetError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d147bc877f9694617ec94651f53f4cf438c00de8d752710c3659f24ba4ffe21c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118810324"
---
# <a name="ibackgroundcopyerrorgeterror-method"></a>IBackgroundCopyError :: GetError, méthode

Récupère le code d’erreur et identifie le contexte dans lequel l’erreur s’est produite.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetError(
  [out] BG_ERROR_CONTEXT *pContext,
  [out] HRESULT          *pErrorCode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pContext* \[ à\]
</dt> <dd>

Contexte dans lequel l’erreur s’est produite. Pour obtenir la liste des valeurs de contexte, consultez l’énumération [**BG_ERROR_CONTEXT**](bg-error-context.md) .

</dd> <dt>

*pErrorCode* \[ à\]
</dt> <dd>

Code d’erreur de l’erreur qui s’est produite.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne **S_OK** en cas de réussite ou une des valeurs com HRESULT standard en cas d’erreur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1709 \[ uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur, version 1709 \[ applications de bureau uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyError est défini en tant que 19C613A0-FCB8-4F28-81AE-897C3D078F81<br/>             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IBackgroundCopyError**](ibackgroundcopyerror.md)
</dt> <dt>

[**IBackgroundCopyError :: GetFile**](ibackgroundcopyerror-getfile-method.md)
</dt> </dl>

 

 





