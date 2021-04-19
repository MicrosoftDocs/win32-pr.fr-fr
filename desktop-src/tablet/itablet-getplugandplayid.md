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
ms.openlocfilehash: 3fb6ce7d59cb29aac4b06b7245bc6246b0688a7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529268"
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
| <dl> <dt>**\_OK**</dt> </dl>   | Opération réussie.<br/>                       |
| <dl> <dt>**E \_ échec**</dt> </dl> | Une erreur non spécifiée s'est produite.<br/> |



 

## <a name="remarks"></a>Notes

Il incombe à l’appelant de libérer la mémoire retournée à partir de cette méthode à l’aide de [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Bibliothèque<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface ITablet**](itablet.md)
</dt> </dl>

 

