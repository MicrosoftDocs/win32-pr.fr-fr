---
title: AuthenticationLevel
description: Définit le niveau d’authentification pour les applications qui n’appellent pas CoInitializeSecurity ou pour les applications qui appellent CoInitializeSecurity et spécifient un AppID.
ms.assetid: 137cbffe-6f45-43f4-bf35-b064b3607fcc
keywords:
- Valeur de Registre AuthenticationLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 697b04bcf4992c8a6943bcb515fa0a4eae616fec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311506"
---
# <a name="authenticationlevel"></a><span data-ttu-id="fd334-104">AuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="fd334-104">AuthenticationLevel</span></span>

<span data-ttu-id="fd334-105">Définit le niveau d’authentification pour les applications qui n’appellent pas [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ou pour les applications qui appellent **CoInitializeSecurity** et spécifient un AppID.</span><span class="sxs-lookup"><span data-stu-id="fd334-105">Sets the authentication level for applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) or for applications that call **CoInitializeSecurity** and specify an AppID.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="fd334-106">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="fd334-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AuthenticationLevel = value
```

## <a name="remarks"></a><span data-ttu-id="fd334-107">Notes</span><span class="sxs-lookup"><span data-stu-id="fd334-107">Remarks</span></span>

<span data-ttu-id="fd334-108">Il s’agit d’une valeur **reg \_ DWORD** qui est équivalente \_ aux \_ constantes de niveau d’authentification RPC C \_ .</span><span class="sxs-lookup"><span data-stu-id="fd334-108">This is a **REG\_DWORD** value that is equivalent to the RPC\_C\_AUTHN\_LEVEL constants.</span></span>



| <span data-ttu-id="fd334-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd334-109">Value</span></span> | <span data-ttu-id="fd334-110">Constante</span><span class="sxs-lookup"><span data-stu-id="fd334-110">Constant</span></span>                             |
|-------|--------------------------------------|
| <span data-ttu-id="fd334-111">1</span><span class="sxs-lookup"><span data-stu-id="fd334-111">1</span></span>     | <span data-ttu-id="fd334-112">RPC \_ C \_ Authn \_ niveau \_ aucun</span><span class="sxs-lookup"><span data-stu-id="fd334-112">RPC\_C\_AUTHN\_LEVEL\_NONE</span></span>           |
| <span data-ttu-id="fd334-113">2</span><span class="sxs-lookup"><span data-stu-id="fd334-113">2</span></span>     | <span data-ttu-id="fd334-114">\_ \_ \_ connexion au niveau AUTHn C RPC \_</span><span class="sxs-lookup"><span data-stu-id="fd334-114">RPC\_C\_AUTHN\_LEVEL\_CONNECT</span></span>        |
| <span data-ttu-id="fd334-115">3</span><span class="sxs-lookup"><span data-stu-id="fd334-115">3</span></span>     | <span data-ttu-id="fd334-116">\_ \_ \_ appel au niveau d’authentification RPC C \_</span><span class="sxs-lookup"><span data-stu-id="fd334-116">RPC\_C\_AUTHN\_LEVEL\_CALL</span></span>           |
| <span data-ttu-id="fd334-117">4</span><span class="sxs-lookup"><span data-stu-id="fd334-117">4</span></span>     | <span data-ttu-id="fd334-118">protocole d’authentification de l' \_ authentification RPC C \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="fd334-118">RPC\_C\_AUTHN\_LEVEL\_PKT</span></span>            |
| <span data-ttu-id="fd334-119">5</span><span class="sxs-lookup"><span data-stu-id="fd334-119">5</span></span>     | <span data-ttu-id="fd334-120">\_ \_ \_ intégrité PKT du niveau d’authentification RPC \_ C \_</span><span class="sxs-lookup"><span data-stu-id="fd334-120">RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY</span></span> |
| <span data-ttu-id="fd334-121">6</span><span class="sxs-lookup"><span data-stu-id="fd334-121">6</span></span>     | <span data-ttu-id="fd334-122">\_confidentialité du \_ niveau d’authentification RPC C \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="fd334-122">RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY</span></span>   |



 

<span data-ttu-id="fd334-123">La valeur **AuthenticationLevel** est similaire à la valeur [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md) .</span><span class="sxs-lookup"><span data-stu-id="fd334-123">The **AuthenticationLevel** value is similar to the [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md) value.</span></span> <span data-ttu-id="fd334-124">Si la valeur **AuthenticationLevel** est présente, elle est utilisée à la place de la valeur **LegacyAuthenticationLevel** pour cet AppID.</span><span class="sxs-lookup"><span data-stu-id="fd334-124">If the **AuthenticationLevel** value is present, it is used instead of the **LegacyAuthenticationLevel** value for that AppID.</span></span>

<span data-ttu-id="fd334-125">Si la valeur de **AuthenticationLevel** est de type incorrect ou hors limites, [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) échoue, provoquant l’échec du marshaling de l’interface.</span><span class="sxs-lookup"><span data-stu-id="fd334-125">If the **AuthenticationLevel** value is of the wrong type or out of range, [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) fails, causing interface marshaling to fail.</span></span> <span data-ttu-id="fd334-126">Cela empêche l’application d’effectuer des appels (Cross-Apartment, Cross-thread, Cross-process ou Cross-Computer).</span><span class="sxs-lookup"><span data-stu-id="fd334-126">This prevents the application from making any calls at all (cross-apartment, cross-thread, cross-process, or cross-computer).</span></span>

<span data-ttu-id="fd334-127">Les valeurs **AuthenticationLevel** et [**AccessPermission**](accesspermission.md) sont indépendantes.</span><span class="sxs-lookup"><span data-stu-id="fd334-127">The **AuthenticationLevel** and [**AccessPermission**](accesspermission.md) values are independent.</span></span> <span data-ttu-id="fd334-128">Si aucun n’est présent, la valeur par défaut est utilisée.</span><span class="sxs-lookup"><span data-stu-id="fd334-128">If one is not present, the default is used.</span></span> <span data-ttu-id="fd334-129">Les règles suivantes répertorient l’interaction entre la valeur **AuthenticationLevel** et la valeur **AccessPermission** :</span><span class="sxs-lookup"><span data-stu-id="fd334-129">The following rules list the interaction between the **AuthenticationLevel** value and the **AccessPermission** value:</span></span>

-   <span data-ttu-id="fd334-130">Si **AuthenticationLevel** a la valeur None, les valeurs [**AccessPermission**](accesspermission.md) et [**DefaultAccessPermission**](defaultaccesspermission.md) sont ignorées (pour cette application).</span><span class="sxs-lookup"><span data-stu-id="fd334-130">If the **AuthenticationLevel** is NONE, the [**AccessPermission**](accesspermission.md) and [**DefaultAccessPermission**](defaultaccesspermission.md) values are ignored (for that application).</span></span>
-   <span data-ttu-id="fd334-131">Si **AuthenticationLevel** n’est pas présent et que [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md) a la valeur None, les valeurs [**AccessPermission**](accesspermission.md) et [**DefaultAccessPermission**](defaultaccesspermission.md) sont ignorées (pour cette application).</span><span class="sxs-lookup"><span data-stu-id="fd334-131">If the **AuthenticationLevel** is not present and the [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md) is NONE, the [**AccessPermission**](accesspermission.md) and [**DefaultAccessPermission**](defaultaccesspermission.md) values are ignored (for that application).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fd334-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fd334-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd334-133">Constantes de niveau d’authentification</span><span class="sxs-lookup"><span data-stu-id="fd334-133">Authentication Level Constants</span></span>](com-authentication-level-constants.md)
</dt> <dt>

[<span data-ttu-id="fd334-134">**LegacyAuthenticationLevel**</span><span class="sxs-lookup"><span data-stu-id="fd334-134">**LegacyAuthenticationLevel**</span></span>](legacyauthenticationlevel.md)
</dt> <dt>

[<span data-ttu-id="fd334-135">Inscription des serveurs COM</span><span class="sxs-lookup"><span data-stu-id="fd334-135">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="fd334-136">Sécurité dans COM</span><span class="sxs-lookup"><span data-stu-id="fd334-136">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




