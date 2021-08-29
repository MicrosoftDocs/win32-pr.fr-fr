---
description: Cette méthode retourne une interface qui fournit l’accès aux données audio.
ms.assetid: 4FA7CC9D-D379-4C08-8D4F-5301ECCDF372
title: 'IAudioFrameNative :: GetData, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAudioFrameNative.GetData
api_type:
- COM
api_location:
- windows.media.core.interop.h
ms.openlocfilehash: 3d845cef0a4a9f6ee9d19b35705b20bd7e6bf2862a84ce4118acb92a5c66f37d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642119"
---
# <a name="iaudioframenativegetdata-method"></a>IAudioFrameNative :: GetData, méthode

Cette méthode retourne une interface qui fournit l’accès aux données audio.

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

Type : **REFIID**

IID de l’interface à récupérer.

</dd> <dt>

*PPV* \[ à\]
</dt> <dd>

Type : **LPVOID \***

Lorsque cette méthode est retournée avec succès, contient le pointeur d’interface demandé dans le paramètre *riid* .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retourne S \_ OK en cas de réussite. Retourne E \_ nointerface si l’interface demandée est introuvable.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IAudioFrameNative**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-iaudioframenative)
</dt> </dl>

 

 



