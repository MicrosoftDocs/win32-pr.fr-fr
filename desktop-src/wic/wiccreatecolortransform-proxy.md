---
description: Crée un objet de transformation de couleur qui implémente IWICColorTransform. Cet objet COM prend en charge le modèle objet à thread libre.
ms.assetid: 43DCC3FB-B687-45F0-AAC6-DED76214716C
title: WICCreateColorTransform_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WICCreateColorTransform_Proxy
api_type:
- DllExport
api_location:
- WindowsCodecsExt.dll
ms.openlocfilehash: 451b549aa44e785e406f50ccf4eb7a8317edf6b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540204"
---
# <a name="wiccreatecolortransform_proxy-function"></a>\_Fonction proxy WICCreateColorTransform

Crée un objet de transformation de couleur qui implémente [**IWICColorTransform**](/windows/win32/api/wincodec/nn-wincodec-iwiccolortransform). Cet objet COM prend en charge le modèle objet à thread libre.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI WICCreateColorTransform_Proxy(
  _Out_  **ppIColorTransform
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppIColorTransform* \[ à\]
</dt> <dd>

Transformation de couleur créée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|-------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>WindowsCodecsExt.dll</dt> </dl> |



 

 
