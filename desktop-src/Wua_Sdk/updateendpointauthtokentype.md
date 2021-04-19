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
ms.openlocfilehash: c978841511b7cfff895a15936a41d169a8500927
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515403"
---
# <a name="updateendpointauthtokentype-enumeration"></a><span data-ttu-id="e13f2-103">Énumération UpdateEndpointAuthTokenType</span><span class="sxs-lookup"><span data-stu-id="e13f2-103">UpdateEndpointAuthTokenType enumeration</span></span>

<span data-ttu-id="e13f2-104">Définit le type des jetons qui peuvent être utilisés pour l’authentification auprès d’un point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="e13f2-104">Defines the type of tokens that can be used for authenticating with an endpoint.</span></span>

## <a name="syntax"></a><span data-ttu-id="e13f2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e13f2-105">Syntax</span></span>


```C++
typedef enum tagUpdateEndpointAuthTokenType { 
  ueattInvalidTokenType  = 0x0,
  ueattSAML11Token       = 0X1
} UpdateEndpointAuthTokenType;
```



## <a name="constants"></a><span data-ttu-id="e13f2-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="e13f2-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e13f2-107"><span id="ueattInvalidTokenType"></span><span id="ueattinvalidtokentype"></span><span id="UEATTINVALIDTOKENTYPE"></span>**ueattInvalidTokenType**</span><span class="sxs-lookup"><span data-stu-id="e13f2-107"><span id="ueattInvalidTokenType"></span><span id="ueattinvalidtokentype"></span><span id="UEATTINVALIDTOKENTYPE"></span>**ueattInvalidTokenType**</span></span>
</dt> <dd>

<span data-ttu-id="e13f2-108">Aucun jeton d’authentification n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="e13f2-108">No authentication token is needed.</span></span>

</dd> <dt>

<span data-ttu-id="e13f2-109"><span id="ueattSAML11Token"></span><span id="ueattsaml11token"></span><span id="UEATTSAML11TOKEN"></span>**ueattSAML11Token**</span><span class="sxs-lookup"><span data-stu-id="e13f2-109"><span id="ueattSAML11Token"></span><span id="ueattsaml11token"></span><span id="UEATTSAML11TOKEN"></span>**ueattSAML11Token**</span></span>
</dt> <dd>

<span data-ttu-id="e13f2-110">Le jeton d’authentification du point de terminaison est un jeton WS-Security SAML (Security Assertion Markup Language) 1,1.</span><span class="sxs-lookup"><span data-stu-id="e13f2-110">The authentication token for the endpoint is a WS-Security SAML (Security Assertion Markup Language) 1.1 token.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e13f2-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e13f2-111">Requirements</span></span>



| <span data-ttu-id="e13f2-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e13f2-112">Requirement</span></span> | <span data-ttu-id="e13f2-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="e13f2-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e13f2-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e13f2-114">Minimum supported client</span></span><br/> | <span data-ttu-id="e13f2-115">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e13f2-115">Windows 8 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="e13f2-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e13f2-116">Minimum supported server</span></span><br/> | <span data-ttu-id="e13f2-117">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e13f2-117">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="e13f2-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="e13f2-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="e13f2-119"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="e13f2-119"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="e13f2-120">MIDL</span><span class="sxs-lookup"><span data-stu-id="e13f2-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e13f2-121"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e13f2-121"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |



 

 




