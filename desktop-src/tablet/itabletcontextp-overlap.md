---
description: Déplace un contexte de tablette vers l’avant ou l’arrière de la file d’attente d’entrée.
ms.assetid: ef4521b5-776b-46dc-864a-625bc221054a
title: 'ITabletContextP :: superposition, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.Overlap
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: ec8b462f2d06e1613c32b795af1793776cafddd6a3531ac6a0b5385f3d3e5128
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712239"
---
# <a name="itabletcontextpoverlap-method"></a>ITabletContextP :: superposition, méthode

Déplace un contexte de tablette vers l’avant ou l’arrière de la file d’attente d’entrée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Overlap(
  [in]  BOOL  bTop,
  [out] DWORD *pdwtcid
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bTop* \[ dans\]
</dt> <dd>

Indique si le contexte de tablette doit être déplacé vers le haut ou le bas de la file d’attente d’entrée.

</dd> <dt>

*pdwtcid* \[ à\]
</dt> <dd>

Identificateur du contexte de tablette.

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

[**Interface ITabletContextP**](itabletcontextp.md)
</dt> </dl>

 

 




