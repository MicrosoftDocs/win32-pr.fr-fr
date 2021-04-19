---
description: Fonction proxy pour la méthode CreateDecoderFromFilename.
ms.assetid: 12c60899-0fe0-47d0-9026-48c74df328ef
title: IWICImagingFactory_CreateDecoderFromFilename_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateDecoderFromFilename_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 3497d71475198d035a496909e65c47df6c5f8b8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545144"
---
# <a name="iwicimagingfactory_createdecoderfromfilename_proxy-function"></a>IWICImagingFactory \_ \_ fonction proxy CreateDecoderFromFilename

Fonction proxy pour la méthode [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IWICImagingFactory_CreateDecoderFromFilename_Proxy(
  _In_        IWICImagingFactory  *pFactory,
  _In_        LPCWSTR             wzFilename,
  _In_  const GUID                *pguidVendor,
  _In_        DWORD               dwDesiredAccess,
  _In_        WICDecodeOptions    metadataOptions,
  _Out_       IWICBitmapDecoder   **ppIDecoder
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFactory* \[ dans\]
</dt> <dd>

Tapez : **IWICImagingFactory \** _

</dd> <dt>

_wzFilename * \[ dans\]
</dt> <dd>

Type : **LPCWSTR**

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom d’un objet à créer ou ouvrir.

</dd> <dt>

*pGuidVendor* \[ dans\]
</dt> <dd>

Type : * #*const \* GUID* _

GUID du fournisseur pour le décodeur.

</dd> <dt>

_dwDesiredAccess * \[ dans\]
</dt> <dd>

Type : **DWORD**

Accès à l’objet, qui peut être en lecture, en écriture ou les deux.

Pour plus d’informations, consultez [ \[ fichiers \] de sécurité de fichiers et de droits d’accès](../fileio/file-security-and-access-rights.md).

</dd> <dt>

*metadataOptions* \[ dans\]
</dt> <dd>

Type : **[ **WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**

[**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) à utiliser lors de la création du décodeur.

</dd> <dt>

*ppIDecoder* \[ à\]
</dt> <dd>

Tapez : **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***

Pointeur qui reçoit un pointeur vers le nouveau [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).

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



 

