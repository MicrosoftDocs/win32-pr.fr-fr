---
description: Fonction proxy pour la méthode GetSpecVersion.
ms.assetid: 363e55c2-d6e8-4ddc-a063-c5be08232a67
title: IWICComponentInfo_GetSpecVersion_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetSpecVersion_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: a7b9b0a44eb5fd8404eecc3ad355ec280583d690
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520182"
---
# <a name="iwiccomponentinfo_getspecversion_proxy-function"></a>IWICComponentInfo \_ \_ fonction proxy GetSpecVersion

Fonction proxy pour la méthode [**GetSpecVersion**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getspecversion) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IWICComponentInfo_GetSpecVersion_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchSpecVersion,
  _Inout_ WCHAR             *wzSpecVersion,
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

*cchSpecVersion* \[ dans\]
</dt> <dd>

Type : **uint**

Taille de la mémoire tampon *wzSpecVersion* .

</dd> <dt>

*wzSpecVersion* \[ in, out\]
</dt> <dd>

Type : **WCHAR \** _

Lorsque cette méthode est retournée, contient une chaîne invarient de culture de la version de la spécification du composant. Le formulaire de version est NN. NN. NN. NN.

</dd> <dt>

_pcchActual * \[ out\]
</dt> <dd>

Type : **uint \** _

Pointeur qui reçoit la longueur réelle de la version de la spécification du composant.

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



 

 




