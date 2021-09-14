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
ms.openlocfilehash: d0efa1c33dd5e0778f13ddd59290de324c92e813
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127222676"
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

## <a name="return-value"></a>Valeur de retour

Si la fonction réussit, la valeur de retour est NMERR \_ Success.

Si la fonction échoue, la valeur de retour est une valeur NMERR qui décrit l’erreur.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Bibliothèque<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




