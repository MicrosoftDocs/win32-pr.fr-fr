---
description: Fonction proxy pour la méthode CreateDecoderFromStream.
ms.assetid: 8395d647-c8c9-4715-b15d-a30755ae0a98
title: IWICImagingFactory_CreateDecoderFromStream_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateDecoderFromStream_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 1f6f84c9c29d10243f1b3bcb2cad43967547eeae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760191"
---
# <a name="iwicimagingfactory_createdecoderfromstream_proxy-function"></a>IWICImagingFactory \_ \_ fonction proxy CreateDecoderFromStream

Fonction proxy pour la méthode [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IWICImagingFactory_CreateDecoderFromStream_Proxy(
  _In_        IWICImagingFactory *pFactory,
  _In_        IStream            *pIStream,
  _In_  const GUID               *pguidVendor,
  _In_        WICDecodeOptions   metadataOptions,
  _Out_       IWICBitmapDecoder  **ppIDecoder
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFactory* \[ dans\]
</dt> <dd>

Tapez : **[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _

</dd> <dt>

_pIStream * \[ dans\]
</dt> <dd>

Type : **[IStream](/windows/desktop/api/objidl/nn-objidl-istream) \** _

Flux à partir duquel créer le décodeur.

</dd> <dt>

_pguidVendor * \[ dans\]
</dt> <dd>

Type : * #*const \* GUID* _

GUID du fournisseur pour le décodeur.

</dd> <dt>

_metadataOptions * \[ dans\]
</dt> <dd>

Type : **[ **WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**

[**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) à utiliser lors de la création du décodeur.

</dd> <dt>

*ppIDecoder* \[ à\]
</dt> <dd>

Tapez : **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***

Pointeur qui reçoit un pointeur vers un nouveau [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).

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



 

