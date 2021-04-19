---
description: Fonction proxy pour la méthode Initialize.
ms.assetid: 47a717d2-9aac-4230-bdb3-093212eb5448
title: IWICBitmapScaler_Initialize_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapScaler_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: cc317adc831b0cf0759580d5c6924fb3f0997524
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531206"
---
# <a name="iwicbitmapscaler_initialize_proxy-function"></a>IWICBitmapScaler \_ Initialise la \_ fonction proxy

Fonction proxy pour la méthode [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapscaler-initialize) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IWICBitmapScaler_Initialize_Proxy(
  _In_ IWICBitmapScaler           *THIS_PTR,
  _In_ IWICBitmapSource           *pISource,
  _In_ UINT                       uiWidth,
  _In_ UINT                       uiHeight,
  _In_ WICBitmapInterpolationMode mode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Ce \_ PTR* \[ dans\]
</dt> <dd>

Tapez : **[**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) \** _

Pointeur vers cet objet [_ *IWICBitmapScaler* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) .

</dd> <dt>

*pISource* \[ dans\]
</dt> <dd>

Tapez : **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _

Source de l’image bitmap d’entrée.

</dd> <dt>

_uiWidth * \[ dans\]
</dt> <dd>

Type : **uint**

Largeur de destination.

</dd> <dt>

*uiHeight* \[ dans\]
</dt> <dd>

Type : **uint**

Hauteur de destination.

</dd> <dt>

*mode* \[ dans\]
</dt> <dd>

Type : **[ **WICBitmapInterpolationMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapinterpolationmode)**

Mode d’interpolation à utiliser lors de la mise à l’échelle.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]<br/>                                                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 




