---
description: Récupère les paramètres de contexte par défaut pour la tablette.
ms.assetid: 59d1bab0-a8b8-4e23-9311-2921f9035dc4
title: 'ITablet :: GetDefaultContextSettings, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetDefaultContextSettings
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 7e2f0977257553d8405b337dcc1f22d8b0fdff5a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521224"
---
# <a name="itabletgetdefaultcontextsettings-method"></a>ITablet :: GetDefaultContextSettings, méthode

Récupère les paramètres de contexte par défaut pour la tablette.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetDefaultContextSettings(
  [out] TABLET_CONTEXT_SETTINGS **ppTCS
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppTCS* \[ à\]
</dt> <dd>

Paramètres de contexte par défaut pour la tablette.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                            | Description                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Réussite.<br/>                       |
| <dl> <dt>**E \_ échec**</dt> </dl> | Une erreur non spécifiée s'est produite.<br/> |



 

## <a name="remarks"></a>Notes

Il incombe à l’appelant de libérer la mémoire retournée à partir de cette méthode à l’aide de [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Bibliothèque<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface ITablet**](itablet.md)
</dt> </dl>

 

