---
description: Fonction proxy pour la méthode GetVersion.
ms.assetid: b064b065-bc02-4943-b208-ce5e40c12aa2
title: IWICComponentInfo_GetVersion_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetVersion_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: bad3677068802861bce9c0c7d0c1b03e5d06d0db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538948"
---
# <a name="iwiccomponentinfo_getversion_proxy-function"></a>IWICComponentInfo \_ GetVersion \_ proxy, fonction

Fonction proxy pour la méthode [**GetVersion**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getversion) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IWICComponentInfo_GetVersion_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchVersion,
  _Inout_ WCHAR             *wzVersion,
  _Out_   UINT              *pcchActual
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Ce \_ PTR* \[ dans\]
</dt> <dd>

Tapez : **[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) \** _

Pointeur vers cet objet [_ *IWICComponentInfo* *](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) .

</dd> <dt>

*cchVersion* \[ dans\]
</dt> <dd>

Type : **uint**

Taille de la mémoire tampon *wzVersion* .

</dd> <dt>

*wzVersion* \[ in, out\]
</dt> <dd>

Type : **WCHAR \** _

Pointeur qui reçoit une chaîne indifférente de culture de la version du composant.

</dd> <dt>

_pcchActual * \[ out\]
</dt> <dd>

Type : **uint \** _

Pointeur qui reçoit la longueur réelle de la version du composant.

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



 

 




