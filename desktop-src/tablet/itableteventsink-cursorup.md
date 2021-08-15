---
description: Se produit lorsque l’utilisateur a relâché le stylet à partir de la surface du digitaliseur de tablette.
ms.assetid: 34dc7e6b-101a-4edd-8c3c-9aafb85cf58b
title: 'ITabletEventSink :: CursorUp, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorUp
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 586f18750e832bad653a3df92d14efb41b39547ee532913ac52c986a9b5e137c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712129"
---
# <a name="itableteventsinkcursorup-method"></a>ITabletEventSink :: CursorUp, méthode

Se produit lorsque l’utilisateur a relâché le stylet à partir de la surface du digitaliseur de tablette.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CursorUp(
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

Données du stylet indiquant l’emplacement où le stylet a été levé de la tablette.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Bibliothèque<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface ITabletEventSink**](itableteventsink.md)
</dt> </dl>

 

 




