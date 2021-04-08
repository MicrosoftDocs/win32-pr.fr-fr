---
description: Fonction proxy pour la méthode InitializeFromPalette.
ms.assetid: e7156cae-8d59-4dbd-8845-0e892e10107b
title: IWICPalette_InitializeFromPalette_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_InitializeFromPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 130c135d3c32135aeefd25fe8799e50c0b5ec855
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868009"
---
# <a name="iwicpalette_initializefrompalette_proxy-function"></a>IWICPalette \_ \_ fonction proxy InitializeFromPalette

Fonction proxy pour la méthode [**InitializeFromPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializefrompalette) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IWICPalette_InitializeFromPalette_Proxy(
  _In_ IWICPalette *THIS_PTR,
  _In_ IWICPalette *pIMILPalette
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Ce \_ PTR* \[ dans\]
</dt> <dd>

Tapez : **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _

Pointeur vers cet objet [_ *IWICPalette* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .

</dd> <dt>

*pIMILPalette* \[ dans\]
</dt> <dd>

Tapez : **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _

Pointeur désignant la palette source.

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



 

 




