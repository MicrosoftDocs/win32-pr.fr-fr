---
description: Se produit lors de la création d’un nouveau contexte de tablette.
ms.assetid: 64e1f778-90c1-417d-a80b-37aeecffd411
title: 'ITabletEventSink :: ContextCreate, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.ContextCreate
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: e622a246c7c317cf9e3373cbd3791108ed071e71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320741"
---
# <a name="itableteventsinkcontextcreate-method"></a>ITabletEventSink :: ContextCreate, méthode

Se produit lors de la création d’un nouveau contexte de tablette.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ContextCreate(
  [in] TABLET_CONTEXT_ID tcid
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*TCID* \[ dans\]
</dt> <dd>

Identificateur du contexte de tablette en cours de création.

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

[**Interface ITabletEventSink**](itableteventsink.md)
</dt> </dl>

 

 




