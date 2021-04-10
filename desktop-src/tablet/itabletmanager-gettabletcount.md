---
description: Récupère le nombre de tablettes attachées au système.
ms.assetid: b2027336-611b-4d17-8943-f16770effaf8
title: 'ITabletManager :: GetTabletCount, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletManager.GetTabletCount
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: fbdd485c44bc67b3ecaec5aa279d4bc20e18d167
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210614"
---
# <a name="itabletmanagergettabletcount-method"></a>ITabletManager :: GetTabletCount, méthode

Récupère le nombre de tablettes attachées au système.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetTabletCount(
  [out] ULONG *pcTablets
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pcTablets* \[ à\]
</dt> <dd>

Nombre de tablettes attachées au système.

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

[**Interface ITabletManager**](itabletmanager.md)
</dt> </dl>

 

 




