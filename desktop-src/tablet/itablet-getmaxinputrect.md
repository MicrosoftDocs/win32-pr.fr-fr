---
description: Récupère un rectangle qui représente la zone d’entrée maximale de la tablette.
ms.assetid: 98facd24-b019-40d1-afe1-28c9a78cae80
title: 'ITablet :: GetMaxInputRect, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetMaxInputRect
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 422c64a8f5f77b354f02ab9601f7a0c888669d61783afb636816efbdc2e13b27
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883539"
---
# <a name="itabletgetmaxinputrect-method"></a>ITablet :: GetMaxInputRect, méthode

Récupère un rectangle qui représente la zone d’entrée maximale de la tablette.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetMaxInputRect(
  [out] RECT *prcInput
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*prcInput* \[ à\]
</dt> <dd>

Pointeur vers le rectangle qui représente la zone d’entrée maximale de la tablette.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                            | Description                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Réussite.<br/>                       |
| <dl> <dt>**E \_ échec**</dt> </dl> | Une erreur non spécifiée s'est produite.<br/> |



 

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

 

 




