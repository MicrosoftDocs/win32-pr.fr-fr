---
description: Se produit lorsque le stylet quitte la plage de détection physique (proximité) de la tablette.
ms.assetid: ded01278-126d-415d-9a7b-1e6fe3650a37
title: 'ITabletEventSink :: CursorOutOfRange, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorOutOfRange
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: e2250401f3888bd07ff250549c11c34e6a54576d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868678"
---
# <a name="itableteventsinkcursoroutofrange-method"></a>ITabletEventSink :: CursorOutOfRange, méthode

Se produit lorsque le stylet quitte la plage de détection physique (proximité) de la tablette.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CursorOutOfRange(
  [in] TABLET_CONTEXT_ID tcid,
       t                 cid
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*TCID* \[ dans\]
</dt> <dd>

Identificateur de la tablette.

</dd> <dt>

*confirmation* 
</dt> <dd>

Identificateur du stylet.

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

 

 




