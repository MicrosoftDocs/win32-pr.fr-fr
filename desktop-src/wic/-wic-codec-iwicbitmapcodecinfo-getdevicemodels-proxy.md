---
description: Fonction proxy pour la méthode GetDeviceModels.
ms.assetid: de8f91f7-fef7-48bc-94fc-34c43175248b
title: IWICBitmapCodecInfo_GetDeviceModels_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetDeviceModels_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 659ca401384f907e0bad1a86dd79e61bad55cf2612bb45713246b26711e57d9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118711985"
---
# <a name="iwicbitmapcodecinfo_getdevicemodels_proxy-function"></a>IWICBitmapCodecInfo \_ \_ fonction proxy GetDeviceModels

Fonction proxy pour la méthode [**GetDeviceModels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getdevicemodels) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IWICBitmapCodecInfo_GetDeviceModels_Proxy(
  _In_    IWICBitmapCodecInfo *THIS_PTR,
  _In_    UINT                cchDeviceModels,
  _Inout_ WCHAR               *wzDeviceModels,
  _Inout_ UINT                *pcchActual
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Ce \_ PTR* \[ dans\]
</dt> <dd>

Type : **[ **IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\***

Pointeur vers cet objet [**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .

</dd> <dt>

*cchDeviceModels* \[ dans\]
</dt> <dd>

Type : **uint**

Taille de la mémoire tampon des modèles d’appareil.

</dd> <dt>

*wzDeviceModels* \[ in, out\]
</dt> <dd>

Type : **WCHAR \***

Pointeur qui reçoit une liste séparée par des virgules des noms de modèles d’appareil associés au codec.

</dd> <dt>

*pcchActual* \[ in, out\]
</dt> <dd>

Type : **uint \***

Taille réelle de la mémoire tampon nécessaire pour récupérer tous les noms de modèle d’appareil.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec SP2, Windows les \[ applications de bureau Vista uniquement\]<br/>                                                                                              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 




