---
description: Cette méthode retourne une interface qui fournit l’accès aux données vidéo.
ms.assetid: 084F020F-A6F5-4982-BA4B-A8F8D6182868
title: 'IVideoFrameNative :: GetData, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVideoFrameNative.GetData
api_type:
- COM
api_location:
- windows.media.core.interop.h
ms.openlocfilehash: 832b2e300887699b926362ce9cbfc6f334c181805bacb3546532920c684251d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993769"
---
# <a name="ivideoframenativegetdata-method"></a>IVideoFrameNative :: GetData, méthode

Cette méthode retourne une interface qui fournit l’accès aux données vidéo.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetData(
  [in]  REFIID riid,
  [out] LPVOID *ppv
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*riid* \[ dans\]
</dt> <dd>

IID de l’interface à récupérer.

</dd> <dt>

*PPV* \[ à\]
</dt> <dd>

Lorsque cette méthode est retournée avec succès, contient le pointeur d’interface demandé dans le paramètre *riid* .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK en cas de réussite. Retourne E \_ nointerface si l’interface demandée est introuvable.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVideoFrameNative**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative)
</dt> </dl>

 

 



