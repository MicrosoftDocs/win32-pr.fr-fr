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
ms.openlocfilehash: b009bc08dddb15bc7aa5b12c8846ea66c4a52e56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534707"
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
| <dl> <dt>**\_OK**</dt> </dl>   | Opération réussie.<br/>                       |
| <dl> <dt>**E \_ échec**</dt> </dl> | Une erreur non spécifiée s'est produite.<br/> |



 

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

 

 




