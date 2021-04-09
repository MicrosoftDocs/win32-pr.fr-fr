---
description: La \_ propriété de sécurité de l’objet SWbemLocator est utilisée pour lire ou définir les paramètres de sécurité d’un objet SWbemLocator. Cette propriété est un objet SWbemSecurity.
ms.assetid: 75987bef-21ae-4420-b069-afab90499218
ms.tgt_platform: multiple
title: SWbemLocator.Security_, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLocator.Security_
- ISWbemLocator.Security_
- ISWbemLocator.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c2aa61ebc3ef48c82405d960d5de42ab8f23dc53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755028"
---
# <a name="swbemlocatorsecurity_-property"></a><span data-ttu-id="bf182-104">SWbemLocator. Security, \_ propriété</span><span class="sxs-lookup"><span data-stu-id="bf182-104">SWbemLocator.Security\_ property</span></span>

<span data-ttu-id="bf182-105">La propriété de **\_ sécurité** de l’objet [**SWbemLocator**](swbemlocator.md) est utilisée pour lire ou définir les paramètres de sécurité d’un objet **SWbemLocator** .</span><span class="sxs-lookup"><span data-stu-id="bf182-105">The **Security\_** property of the [**SWbemLocator**](swbemlocator.md) object is used to read or set the security settings for an **SWbemLocator** object.</span></span> <span data-ttu-id="bf182-106">Cette propriété est un objet [**SWbemSecurity**](swbemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="bf182-106">This property is an [**SWbemSecurity**](swbemsecurity.md) object.</span></span>

> [!Note]  
> <span data-ttu-id="bf182-107">La définition de la propriété de **sécurité \_** d’un objet [**SWbemLocator**](swbemlocator.md) sur la **valeur null** accorde à tout moment un accès illimité à tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="bf182-107">Setting the **Security\_** property of an [**SWbemLocator**](swbemlocator.md) object to **NULL** grants unlimited access to everyone at all times.</span></span> <span data-ttu-id="bf182-108">Pour plus d’informations, consultez [**SWbemSecurity**](swbemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="bf182-108">For more information, see [**SWbemSecurity**](swbemsecurity.md).</span></span>

 

<span data-ttu-id="bf182-109">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="bf182-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="bf182-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="bf182-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf182-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bf182-111">Syntax</span></span>


```VB
SWbemLocator.Security_ As Object
```



## <a name="property-value"></a><span data-ttu-id="bf182-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="bf182-112">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="bf182-113">Notes</span><span class="sxs-lookup"><span data-stu-id="bf182-113">Remarks</span></span>

<span data-ttu-id="bf182-114">Les propriétés d’un objet **SWbemLocator. \_ Security** n’ont pas de valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="bf182-114">The properties of an **SWbemLocator.Security\_** object have no default values.</span></span> <span data-ttu-id="bf182-115">Si vous tentez d’obtenir la valeur de [**SWbemSecurity. AuthenticationLevel**](swbemsecurity-authenticationlevel.md) ou de [**SWbemSecurity. ImpersonationLevel**](swbemsecurity-impersonationlevel.md) sur un objet [**SWbemLocator**](swbemlocator.md) avant de le définir, une erreur [wbemErrFailed](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum) se produit.</span><span class="sxs-lookup"><span data-stu-id="bf182-115">If you attempt to get the value of [**SWbemSecurity.AuthenticationLevel**](swbemsecurity-authenticationlevel.md) or [**SWbemSecurity.ImpersonationLevel**](swbemsecurity-impersonationlevel.md) on an [**SWbemLocator**](swbemlocator.md) object before you have set it, an [wbemErrFailed](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum) error results.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf182-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf182-116">Requirements</span></span>



| <span data-ttu-id="bf182-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bf182-117">Requirement</span></span> | <span data-ttu-id="bf182-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf182-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf182-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf182-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bf182-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bf182-120">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bf182-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf182-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bf182-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bf182-122">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bf182-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="bf182-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf182-124"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf182-124"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="bf182-125">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="bf182-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="bf182-126"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bf182-126"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bf182-127">DLL</span><span class="sxs-lookup"><span data-stu-id="bf182-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf182-128"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf182-128"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="bf182-129">CLSID</span><span class="sxs-lookup"><span data-stu-id="bf182-129">CLSID</span></span><br/>                    | <span data-ttu-id="bf182-130">CLSID \_ SWbemLocator</span><span class="sxs-lookup"><span data-stu-id="bf182-130">CLSID\_SWbemLocator</span></span><br/>                                                          |
| <span data-ttu-id="bf182-131">IID</span><span class="sxs-lookup"><span data-stu-id="bf182-131">IID</span></span><br/>                      | <span data-ttu-id="bf182-132">IID \_ ISWbemLocator</span><span class="sxs-lookup"><span data-stu-id="bf182-132">IID\_ISWbemLocator</span></span><br/>                                                           |



## <a name="see-also"></a><span data-ttu-id="bf182-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf182-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf182-134">**SWbemLocator**</span><span class="sxs-lookup"><span data-stu-id="bf182-134">**SWbemLocator**</span></span>](swbemlocator.md)
</dt> <dt>

[<span data-ttu-id="bf182-135">Création d’une application ou d’un script WMI</span><span class="sxs-lookup"><span data-stu-id="bf182-135">Creating a WMI Application or Script</span></span>](creating-a-wmi-application-or-script.md)
</dt> <dt>

[<span data-ttu-id="bf182-136">Exécution d’opérations privilégiées à l’aide de VBScript</span><span class="sxs-lookup"><span data-stu-id="bf182-136">Executing Privileged Operations Using VBScript</span></span>](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[<span data-ttu-id="bf182-137">Définition de la sécurité des processus d' \_ application cliente \_</span><span class="sxs-lookup"><span data-stu-id="bf182-137">Setting Client\_Application\_Process Security</span></span>](setting-client-application-process-security.md)
</dt> <dt>

[<span data-ttu-id="bf182-138">**Objet SWbemSecurity**</span><span class="sxs-lookup"><span data-stu-id="bf182-138">**SWbemSecurity object**</span></span>](swbemsecurity.md)
</dt> <dt>

[<span data-ttu-id="bf182-139">Sécurisation d’une connexion WMI à distance</span><span class="sxs-lookup"><span data-stu-id="bf182-139">Securing a Remote WMI Connection</span></span>](securing-a-remote-wmi-connection.md)
</dt> </dl>

 

 




