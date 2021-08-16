---
title: WMCreateStreamForURL fonction)
description: La fonction WMCreateStreamForURL est implémentée par l’application pour créer un objet COM IStream pour une URL donnée.
ms.assetid: df8d0e57-9f71-4be3-a0b0-cf61b68611bc
keywords:
- WMCreateStreamForURL fonction Windows Media format
topic_type:
- apiref
api_name:
- WMCreateStreamForURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9c32302147eeb814c211a77555ab1c9bb3614eddf3d8001015479461e05d40ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117653452"
---
# <a name="wmcreatestreamforurl-function"></a>WMCreateStreamForURL fonction)

La fonction **WMCreateStreamForURL** est implémentée par l’application pour créer un objet com **ISTREAM** pour une URL donnée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WMCreateStreamForURL(
  _In_  LPCWSTR pwszURL,
  _Out_ BOOL    *pfCorrectSource,
  _Out_ IStream **ppStream
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pwszURL* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne de caractères larges contenant l’URL.

</dd> <dt>

*pfCorrectSource* \[ à\]
</dt> <dd>

Pointeur vers un indicateur, true empêchera le kit de développement logiciel (SDK) d’essayer d’autres plug-ins sources pour cette URL.

</dd> <dt>

*PPStream* \[ à\]
</dt> <dd>

Pointeur vers un pointeur vers l’objet **IStream** créé par la méthode.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, elle doit retourner S \_ OK. En cas d’échec, il doit retourner un code d’erreur **HRESULT** approprié, et \* *PPStream* doit avoir la valeur **null**.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Plug-ins sources**](source-plug-ins.md)
</dt> </dl>

 

 




