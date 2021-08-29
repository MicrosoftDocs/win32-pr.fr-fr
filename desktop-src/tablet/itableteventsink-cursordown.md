---
description: Se produit lorsque l’info-bulle du stylet contacte la surface de tablette numérique.
ms.assetid: 7f4a441d-00d2-4120-8a8d-d3496cdc7e58
title: 'ITabletEventSink :: CursorDown, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorDown
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 242e9ebdf2999c342e6ae7f4711a9f142b38a23e977e7dc9a44b906e0062bc2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119820639"
---
# <a name="itableteventsinkcursordown-method"></a>ITabletEventSink :: CursorDown, méthode

Se produit lorsque l’info-bulle du stylet contacte la surface de tablette numérique.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CursorDown(
  [in] TABLET_CONTEXT_ID tcid,
  [in] CURSOR_ID         cid,
  [in] ULONG             nSerialNumber,
  [in] ULONG             cbPkt,
  [in] BYTE              *pbPkt
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*TCID* \[ dans\]
</dt> <dd>

Identificateur de la tablette.

</dd> <dt>

*CID* \[ dans\]
</dt> <dd>

Identificateur du stylet.

</dd> <dt>

*nSerialNumber* \[ dans\]
</dt> <dd>

Numéro de série du stylet.

</dd> <dt>

*cbPkt* \[ dans\]
</dt> <dd>

Nombre d’octets dans un paquet de données de stylet.

</dd> <dt>

*pbPkt* \[ dans\]
</dt> <dd>

Données du stylet indiquant l’emplacement où le stylet touche la tablette.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                            | Description                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Réussite.<br/>                       |
| <dl> <dt>**E \_ échec**</dt> </dl> | Une erreur non spécifiée s'est produite.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Bibliothèque<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface ITabletEventSink**](itableteventsink.md)
</dt> </dl>

 

 




