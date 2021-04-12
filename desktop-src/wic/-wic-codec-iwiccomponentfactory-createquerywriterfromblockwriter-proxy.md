---
description: Fonction proxy pour la méthode CreateQueryWriterFromBlockWriter.
ms.assetid: f941e3b1-1645-4ed6-b2c5-180cb4c43fca
title: IWICComponentFactory_CreateQueryWriterFromBlockWriter_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentFactory_CreateQueryWriterFromBlockWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c8c94b351e72fd7de367e5dd74a0c7ed62ce84f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204225"
---
# <a name="iwiccomponentfactory_createquerywriterfromblockwriter_proxy-function"></a>IWICComponentFactory \_ \_ fonction proxy CreateQueryWriterFromBlockWriter

Fonction proxy pour la méthode [**CreateQueryWriterFromBlockWriter**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createquerywriterfromblockwriter) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IWICComponentFactory_CreateQueryWriterFromBlockWriter_Proxy(
  _In_  IWICComponentFactory    *THIS_PTR,
  _In_  IWICMetadataBlockWriter *pIBlockWriter,
  _Out_ IWICMetadataQueryWriter **ppIQueryWriter
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Ce \_ PTR* \[ dans\]
</dt> <dd>

Tapez : **[**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) \** _

Pointeur vers cet objet [_ *IWICComponentFactory* *](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) .

</dd> <dt>

*pIBlockWriter* \[ dans\]
</dt> <dd>

Tapez : **[**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) \** _

</dd> <dt>

_ppIQueryWriter * \[ out\]
</dt> <dd>

Type : **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***

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



 

 




