---
description: Définit les différents États d’erreur de l’extension de source de média.
ms.assetid: 8FD54833-F60B-49E8-A673-6130F3B06160
title: Énumération MF_MSE_ERROR
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MSE_ERROR
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: 71246aaa2897540b272360a790718f8d5900934108c98dfcc6b4023898f9f2db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104585"
---
# <a name="mf_mse_error-enumeration"></a>\_Énumération des erreurs de MSE MF \_

Définit les différents États d’erreur de l’extension de source de média.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum _MF_MSE_ERROR { 
  MF_MSE_ERROR_NOERROR        =  0,
  MF_MSE_ERROR_NETWORK        = 1,
  MF_MSE_ERROR_DECODE         = 2,
  MF_MSE_ERROR_UNKNOWN_ERROR  =  3
} MF_MSE_ERROR;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MF_MSE_ERROR_NOERROR"></span><span id="mf_mse_error_noerror"></span>**\_erreur MF MSE \_ erreur \_**
</dt> <dd>

Ne spécifie aucune erreur.

</dd> <dt>

<span id="MF_MSE_ERROR_NETWORK"></span><span id="mf_mse_error_network"></span>**\_réseau d' \_ Erreurs MF MSE \_**
</dt> <dd>

Spécifie une erreur avec le réseau.

</dd> <dt>

<span id="MF_MSE_ERROR_DECODE"></span><span id="mf_mse_error_decode"></span>**\_code d' \_ erreur MF MSE \_**
</dt> <dd>

Spécifie une erreur de décodage.

</dd> <dt>

<span id="MF_MSE_ERROR_UNKNOWN_ERROR"></span><span id="mf_mse_error_unknown_error"></span>**erreur MF \_ MSE \_ erreur \_ inconnue \_**
</dt> <dd>

Spécifie une erreur inconnue.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/>                                      |
| MIDL<br/>                      | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations de Media Foundation](media-foundation-enumerations.md)
</dt> </dl>

 

 




