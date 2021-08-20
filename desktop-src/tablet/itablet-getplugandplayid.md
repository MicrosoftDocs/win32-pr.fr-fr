---
description: Retourne une chaîne contenant l’ID de Plug-and-Play pour le périphérique tablette.
ms.assetid: a0b6619b-f80c-470b-aa3f-f0b30a9dbda8
title: 'ITablet :: GetPlugAndPlayId, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetPlugAndPlayId
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 2c7028e11a7a8ec6d1e6c79c461ce05f50dfe0b4b69108f0f1527b4fbd9ba3fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118041909"
---
# <a name="itabletgetplugandplayid-method"></a>ITablet :: GetPlugAndPlayId, méthode

Retourne une chaîne contenant l’ID de Plug-and-Play pour le périphérique tablette.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetPlugAndPlayId(
  [out] LPWSTR *ppwszPPId
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppwszPPId* \[ à\]
</dt> <dd>

Pointeur vers une chaîne contenant l’ID de Plug-and-Play pour le périphérique tablette.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                            | Description                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Réussite.<br/>                       |
| <dl> <dt>**E \_ échec**</dt> </dl> | Une erreur non spécifiée s'est produite.<br/> |



 

## <a name="remarks"></a>Remarques

Il incombe à l’appelant de libérer la mémoire retournée à partir de cette méthode à l’aide de [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Bibliothèque<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface ITablet**](itablet.md)
</dt> </dl>

 

