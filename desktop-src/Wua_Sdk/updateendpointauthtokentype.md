---
description: Définit le type des jetons qui peuvent être utilisés pour l’authentification auprès d’un point de terminaison.
ms.assetid: 2048BD09-056F-47C1-AD2F-998DE6C52EA6
title: Énumération UpdateEndpointAuthTokenType (UpdateEndpointAuth. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateEndpointAuthTokenType
api_type:
- HeaderDef
api_location:
- UpdateEndpointAuth.h
ms.openlocfilehash: b9e3efbff48097dcede12d5c8d3117171ef622f20a3bf017b12c6d3ce13a1c00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118814711"
---
# <a name="updateendpointauthtokentype-enumeration"></a>Énumération UpdateEndpointAuthTokenType

Définit le type des jetons qui peuvent être utilisés pour l’authentification auprès d’un point de terminaison.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum tagUpdateEndpointAuthTokenType { 
  ueattInvalidTokenType  = 0x0,
  ueattSAML11Token       = 0X1
} UpdateEndpointAuthTokenType;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="ueattInvalidTokenType"></span><span id="ueattinvalidtokentype"></span><span id="UEATTINVALIDTOKENTYPE"></span>**ueattInvalidTokenType**
</dt> <dd>

Aucun jeton d’authentification n’est nécessaire.

</dd> <dt>

<span id="ueattSAML11Token"></span><span id="ueattsaml11token"></span><span id="UEATTSAML11TOKEN"></span>**ueattSAML11Token**
</dt> <dd>

Le jeton d’authentification du point de terminaison est un jeton WS-Security SAML (Security Assertion Markup Language) 1,1.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                        |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                              |
| En-tête<br/>                   | <dl> <dt>UpdateEndpointAuth. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>UpdateEndpointAuth. idl</dt> </dl> |



 

 




