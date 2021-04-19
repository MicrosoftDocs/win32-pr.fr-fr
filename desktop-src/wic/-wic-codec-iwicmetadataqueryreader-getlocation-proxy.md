---
description: Fonction proxy pour la méthode GetLocation.
ms.assetid: 2dc4767b-9992-4e5a-a171-2de19178d912
title: IWICMetadataQueryReader_GetLocation_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetLocation_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 40dd23df0e1004687a945889d2598d41ca0e2e72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522452"
---
# <a name="iwicmetadataqueryreader_getlocation_proxy-function"></a>IWICMetadataQueryReader \_ \_ fonction proxy GetLocation

Fonction proxy pour la méthode [**GetLocation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getlocation) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IWICMetadataQueryReader_GetLocation_Proxy(
  _In_    IWICMetadataQueryReader *THIS_PTR,
  _In_    UINT                    cchMaxLength,
  _Inout_ WCHAR                   *wzNamespace,
  _Out_   UINT                    *pcchActualLength
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Ce \_ PTR* \[ dans\]
</dt> <dd>

Tapez : **[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) \** _

Pointeur vers cet objet [_ *IWICMetadataQueryReader* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) .

</dd> <dt>

*cchMaxLength* \[ dans\]
</dt> <dd>

Type : **uint**

Longueur de la mémoire tampon *wzNamespace* .

</dd> <dt>

*wzNamespace* \[ in, out\]
</dt> <dd>

Type : **WCHAR \** _

Pointeur qui reçoit l’emplacement actuel de l’espace de noms.

</dd> <dt>

_pcchActualLength * \[ out\]
</dt> <dd>

Type : **uint \** _

Longueur réelle de la mémoire tampon nécessaire pour récupérer l’emplacement actuel de l’espace de noms.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : _ *HRESULT**

Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]<br/>                                                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 




