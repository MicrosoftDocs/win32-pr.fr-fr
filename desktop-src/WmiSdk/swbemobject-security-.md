---
description: La \_ propriété Security de l’objet SWbemObject est utilisée pour lire ou définir les paramètres de sécurité d’un objet SWbemObject.
ms.assetid: add77267-d62f-4ee4-a0ff-8ca06a6bf7cd
ms.tgt_platform: multiple
title: SWbemObject.Security_, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Security_
- ISWbemObject.Security_
- ISWbemObject.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f4d4b9aec7b6d800fa27609abd5d0cb1f3a435a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320665"
---
# <a name="swbemobjectsecurity_-property"></a><span data-ttu-id="91902-103">SWbemObject. Security, \_ propriété</span><span class="sxs-lookup"><span data-stu-id="91902-103">SWbemObject.Security\_ property</span></span>

<span data-ttu-id="91902-104">La **propriété \_ Security** de l’objet [**SWbemObject**](swbemobject.md) est utilisée pour lire ou définir les paramètres de sécurité d’un objet **SWbemObject** .</span><span class="sxs-lookup"><span data-stu-id="91902-104">The **Security\_** property of the [**SWbemObject**](swbemobject.md) object is used to read, or set the security settings for an **SWbemObject** object.</span></span> <span data-ttu-id="91902-105">Cette propriété est un objet [**SWbemSecurity**](swbemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="91902-105">This property is an [**SWbemSecurity**](swbemsecurity.md) object.</span></span> <span data-ttu-id="91902-106">Les paramètres de sécurité de cet objet n’indiquent pas les paramètres d’authentification, d’emprunt d’identité ou de privilège effectués sur une connexion à Windows Management Instrumentation (WMI), ou la sécurité en vigueur pour le proxy lorsqu’un objet est remis à un récepteur dans un appel asynchrone.</span><span class="sxs-lookup"><span data-stu-id="91902-106">The security settings in this object do not indicate the authentication, impersonation, or privilege settings made on a connection to Windows Management Instrumentation (WMI), or the security in effect for the proxy when an object is delivered to a sink in an asynchronous call.</span></span> <span data-ttu-id="91902-107">Pour plus d’informations, consultez [maintenance de la sécurité WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="91902-107">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

> [!Note]  
> <span data-ttu-id="91902-108">Le paramétrage de la propriété de **\_ sécurité** d’un objet [**SWbemObject**](swbemobject.md) sur **null** accorde un accès illimité à tout le monde en permanence.</span><span class="sxs-lookup"><span data-stu-id="91902-108">Setting the **Security\_** property of an [**SWbemObject**](swbemobject.md) object to **NULL** grants unlimited access to everyone all the time.</span></span> <span data-ttu-id="91902-109">Pour plus d’informations, consultez [**SWbemSecurity**](swbemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="91902-109">For more information, see [**SWbemSecurity**](swbemsecurity.md).</span></span>

 

<span data-ttu-id="91902-110">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="91902-110">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="91902-111">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="91902-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="91902-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="91902-112">Syntax</span></span>


```VB
SWbemObject.Security_ As Object
```



## <a name="property-value"></a><span data-ttu-id="91902-113">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="91902-113">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="91902-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91902-114">Requirements</span></span>



| <span data-ttu-id="91902-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91902-115">Requirement</span></span> | <span data-ttu-id="91902-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="91902-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="91902-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91902-117">Minimum supported client</span></span><br/> | <span data-ttu-id="91902-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="91902-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="91902-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91902-119">Minimum supported server</span></span><br/> | <span data-ttu-id="91902-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="91902-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="91902-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="91902-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="91902-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="91902-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="91902-123">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="91902-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="91902-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="91902-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="91902-125">DLL</span><span class="sxs-lookup"><span data-stu-id="91902-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91902-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91902-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="91902-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="91902-127">CLSID</span></span><br/>                    | <span data-ttu-id="91902-128">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="91902-128">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="91902-129">IID</span><span class="sxs-lookup"><span data-stu-id="91902-129">IID</span></span><br/>                      | <span data-ttu-id="91902-130">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="91902-130">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="91902-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91902-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91902-132">**M**</span><span class="sxs-lookup"><span data-stu-id="91902-132">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="91902-133">Création d’une application ou d’un script WMI</span><span class="sxs-lookup"><span data-stu-id="91902-133">Creating a WMI Application or Script</span></span>](creating-a-wmi-application-or-script.md)
</dt> <dt>

[<span data-ttu-id="91902-134">Définition de la sécurité des processus d' \_ application cliente \_</span><span class="sxs-lookup"><span data-stu-id="91902-134">Setting Client\_Application\_Process Security</span></span>](setting-client-application-process-security.md)
</dt> <dt>

[<span data-ttu-id="91902-135">**SWbemSecurity**</span><span class="sxs-lookup"><span data-stu-id="91902-135">**SWbemSecurity**</span></span>](swbemsecurity.md)
</dt> <dt>

[<span data-ttu-id="91902-136">**WbemAuthenticationLevelEnum**</span><span class="sxs-lookup"><span data-stu-id="91902-136">**WbemAuthenticationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[<span data-ttu-id="91902-137">**WbemImpersonationLevelEnum**</span><span class="sxs-lookup"><span data-stu-id="91902-137">**WbemImpersonationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> <dt>

[<span data-ttu-id="91902-138">**WbemPrivilegeEnum**</span><span class="sxs-lookup"><span data-stu-id="91902-138">**WbemPrivilegeEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[<span data-ttu-id="91902-139">**Constantes de privilège**</span><span class="sxs-lookup"><span data-stu-id="91902-139">**Privilege Constants**</span></span>](privilege-constants.md)
</dt> </dl>

 

 




