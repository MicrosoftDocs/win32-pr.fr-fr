---
description: La fonction CreateNPPInterface utilise l’objet BLOB retourné par le Finder pour créer un NPP que l’application peut utiliser.
ms.assetid: 41f48c72-3284-4ebc-baff-63553c8971e6
title: CreateNPPInterface, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateNPPInterface
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 03c2bb7fae0f68e6d38016df353266cfc9ec11757eeb98f6a5e41ab4316e63c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744539"
---
# <a name="createnppinterface-function"></a>CreateNPPInterface fonction)

La fonction **CreateNPPInterface** utilise l’objet BLOB retourné par le Finder pour créer un NPP que l’application peut utiliser.

## <a name="syntax"></a>Syntaxe


```C++
DWORD CreateNPPInterface(
  _In_  HBLOB  hBlob,
  _In_  REFIID iid,
  _Out_ void   **ppvObject
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hBlob* \[ dans\]
</dt> <dd>

Handle vers l’objet BLOB retourné par le Finder.

</dd> <dt>

*IID* \[ dans\]
</dt> <dd>

Identificateur de l’interface que vous appelez à partir de NPP (**IRTC** ou **IDelaydC**, par exemple).

</dd> <dt>

*ppvObject* \[ à\]
</dt> <dd>

Pointeur vers le pointeur retourné vers l’interface demandée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est NMERR \_ Success.

Si la fonction échoue, la valeur de retour est une valeur NMERR qui décrit l’erreur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Bibliothèque<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




