---
description: Fonction proxy pour la méthode CreateMetadataWriterFromReader.
ms.assetid: da9e80d3-3265-428d-987e-8b344472527a
title: IWICComponentFactory_CreateMetadataWriterFromReader_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentFactory_CreateMetadataWriterFromReader_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e08ca8b42a0ddf0997ee5945c11fa75257d82f1b3655969f3f29a50264b561fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118206660"
---
# <a name="iwiccomponentfactory_createmetadatawriterfromreader_proxy-function"></a>IWICComponentFactory \_ \_ fonction proxy CreateMetadataWriterFromReader

Fonction proxy pour la méthode [**CreateMetadataWriterFromReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatawriterfromreader) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IWICComponentFactory_CreateMetadataWriterFromReader_Proxy(
  _In_        IWICComponentFactory *THIS_PTR,
  _In_        IWICMetadataReader   *pIReader,
  _In_  const GUID                 *pguidVendor,
  _Out_       IWICMetadataWriter   **ppIWriter
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Ce \_ PTR* \[ dans\]
</dt> <dd>

Type : **[ **IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)\***

Pointeur vers cet objet [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) .

</dd> <dt>

*pIReader* \[ dans\]
</dt> <dd>

Type : **[ **IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)\***

</dd> <dt>

*pGuidVendor* \[ dans\]
</dt> <dd>

Type : **const GUID \***

</dd> <dt>

*ppIWriter* \[ à\]
</dt> <dd>

Type : **[ **IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)\*\***

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



 

 




