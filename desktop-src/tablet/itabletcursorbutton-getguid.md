---
description: Récupère l’identificateur unique du bouton du stylet.
ms.assetid: 06bd6a84-46cd-4c62-92d6-50caae359e43
title: 'ITabletCursorButton :: GetGuid, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursorButton.GetGuid
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: f4492aa98630491730435080981172bc60a1eeccfe0c84ed76e3b4d504a79ad1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119844279"
---
# <a name="itabletcursorbuttongetguid-method"></a>ITabletCursorButton :: GetGuid, méthode

Récupère l’identificateur unique du bouton du stylet.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetGuid(
  [out] GUID *pguidBtn
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pguidBtn* \[ à\]
</dt> <dd>

Valeur unique qui identifie le bouton du stylet.

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

[**Interface ITabletCursorButton**](itabletcursorbutton.md)
</dt> </dl>

 

 




