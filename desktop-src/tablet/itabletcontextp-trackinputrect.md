---
description: Met à jour les coordonnées du mappage de l’emplacement des fenêtres dans le digitaliseur de tablette.
ms.assetid: 2984b87b-620e-4e5d-a3cc-4c3f4c89bae3
title: 'ITabletContextP :: TrackInputRect, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.TrackInputRect
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: 400055247583ec0bd2095d5d6f68d8481c69fd6bb4e7f7730344120203655ce2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350569"
---
# <a name="itabletcontextptrackinputrect-method"></a>ITabletContextP :: TrackInputRect, méthode

Met à jour les coordonnées du mappage de l’emplacement des fenêtres dans le digitaliseur de tablette.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT TrackInputRect(
  [out] RECT *prcInput
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*prcInput* \[ à\]
</dt> <dd>

Nouveau rectangle de la fenêtre d’entrée après la mise à jour du mappage entre les coordonnées de la fenêtre et du digitaliseur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                            | Description                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Réussite.<br/>                       |
| <dl> <dt>**E \_ échec**</dt> </dl> | Une erreur non spécifiée s'est produite.<br/> |



 

## <a name="remarks"></a>Remarques

Appelez cette méthode chaque fois que l’emplacement de la fenêtre à l’écran change.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Bibliothèque<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface ITabletContextP**](itabletcontextp.md)
</dt> </dl>

 

 




