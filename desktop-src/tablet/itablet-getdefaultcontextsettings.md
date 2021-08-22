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
ms.openlocfilehash: 646756a924bd9b848f2141b796205f2cf2374140811b7dd87f8ffd64c69ee8d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119336259"
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

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                            | Description                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Réussite.<br/>                       |
| <dl> <dt>**E \_ échec**</dt> </dl> | Une erreur non spécifiée s'est produite.<br/> |



 

## <a name="remarks"></a>Remarques

Il incombe à l’appelant de libérer la mémoire retournée à partir de cette méthode à l’aide de [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Bibliothèque<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface ITablet**](itablet.md)
</dt> </dl>

 

