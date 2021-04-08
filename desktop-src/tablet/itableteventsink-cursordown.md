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
ms.openlocfilehash: 1f0ffbe8c300e3c227cd59d8ff391b8990873c56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757054"
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

 

 




