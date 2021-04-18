---
description: Identifie si le style de non-couleur spécifié est souligné.
ms.assetid: 72056bf7-0a18-4ad3-a8c4-d2335a7218ae
title: IdUlIMEStyle fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IdUlIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 262f726e8b2201b809a9416a67c2af860acee65e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526377"
---
# <a name="idulimestyle-function"></a>IdUlIMEStyle fonction)

Identifie si le style de non-couleur spécifié est souligné.

## <a name="syntax"></a>Syntaxe


```C++
UINT __cdecl IdUlIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pimestyle* \[ dans\]
</dt> <dd>

Une structure **IMESTYLE** retournée par la fonction [**PIMEStyleFromAttr**](pimestylefromattr.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette fonction peut retourner l’une des valeurs suivantes.

<dl> <dt>

**IMESTY \_ UL \_ min** (2002)
</dt> <dt>

**IMESTY \_ UL \_ None** (2002)
</dt> <dt>

**IMESTY \_ UL \_ simple** (2003)
</dt> <dt>

**IMESTY \_ UL \_ pointé** (2005)
</dt> <dt>

**IMESTY \_ UL \_ épais** (2006)
</dt> <dt>

**IMESTY \_ UL en \_ minuscule** (2011)
</dt> <dt>

**IMESTY \_ UL \_ THICKLOWER** (2012)
</dt> <dt>

**IMESTY \_ UL \_ THICKDITHLOWER** (2013)
</dt> <dt>

**IMESTY \_ UL \_ DITHLOWER** (2014)
</dt> <dt>

**IMESTY \_ UL \_ Max** (2014)
</dt> </dl>

## <a name="remarks"></a>Notes

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PIMEStyleFromAttr**](pimestylefromattr.md)
</dt> </dl>

 

 
