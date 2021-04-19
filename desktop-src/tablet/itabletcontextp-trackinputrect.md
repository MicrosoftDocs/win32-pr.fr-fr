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
ms.openlocfilehash: 4529263b81933651db35b88262b11e979d39e6f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528335"
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
| <dl> <dt>**\_OK**</dt> </dl>   | Opération réussie.<br/>                       |
| <dl> <dt>**E \_ échec**</dt> </dl> | Une erreur non spécifiée s'est produite.<br/> |



 

## <a name="remarks"></a>Notes

Appelez cette méthode chaque fois que l’emplacement de la fenêtre à l’écran change.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Bibliothèque<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface ITabletContextP**](itabletcontextp.md)
</dt> </dl>

 

 




