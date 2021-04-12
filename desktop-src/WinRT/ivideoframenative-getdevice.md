---
description: Cette méthode retourne un appareil associé aux données vidéo.
ms.assetid: 9A61159B-C383-4770-AD8F-9F69F720E3E2
title: 'IVideoFrameNative :: GetDevice, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVideoFrameNative.GetDevice
api_type:
- COM
api_location:
- windows.media.core.interop.h
ms.openlocfilehash: d012ae79b1cb2c83e916dc74113cc3d0560da4c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393516"
---
# <a name="ivideoframenativegetdevice-method"></a>IVideoFrameNative :: GetDevice, méthode

Cette méthode retourne un appareil associé aux données vidéo.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetDevice(
  [in]  REFIID riid,
  [out] LPVOID *ppv
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*riid* \[ dans\]
</dt> <dd>

IID de l’appareil à récupérer.

</dd> <dt>

*PPV* \[ à\]
</dt> <dd>

Lorsque cette méthode est retournée avec succès, contient le pointeur d’appareil demandé dans le paramètre *riid* .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK en cas de réussite.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVideoFrameNative**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative)
</dt> </dl>

 

 



