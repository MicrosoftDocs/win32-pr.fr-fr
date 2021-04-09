---
description: Fonction proxy pour la méthode RemoveMetadataByName.
ms.assetid: fb86766e-234d-4e39-9d4b-7814d50a3867
title: IWICMetadataQueryWriter_RemoveMetadataByName_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryWriter_RemoveMetadataByName_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 8e4681d3fbb93f176129ce2527356306d4ea02fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866530"
---
# <a name="iwicmetadataquerywriter_removemetadatabyname_proxy-function"></a>IWICMetadataQueryWriter \_ \_ fonction proxy RemoveMetadataByName

Fonction proxy pour la méthode [**RemoveMetadataByName**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataquerywriter-removemetadatabyname) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IWICMetadataQueryWriter_RemoveMetadataByName_Proxy(
  _In_ IWICMetadataQueryWriter *THIS_PTR,
  _In_ LPCWSTR                 wzName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Ce \_ PTR* \[ dans\]
</dt> <dd>

Tapez : **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) \** _

Pointeur vers cet objet [_ *IWICMetadataQueryWriter* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) .

</dd> <dt>

*wzName* \[ dans\]
</dt> <dd>

Type : **LPCWSTR**

Nom de l’élément de métadonnées à supprimer.

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



 

 




