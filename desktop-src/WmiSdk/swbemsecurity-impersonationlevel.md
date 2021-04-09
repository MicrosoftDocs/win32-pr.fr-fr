---
description: La propriété ImpersonationLevel est un entier qui définit le niveau d’emprunt d’identité COM affecté à cet objet.
ms.assetid: cf57620b-7827-4552-a969-d25e5eb13a89
ms.tgt_platform: multiple
title: SWbemSecurity. ImpersonationLevel, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity.ImpersonationLevel
- ISWbemSecurity.ImpersonationLevel
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3b996d5920aba91fddf880ee9ddf6bf8081fb39f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868742"
---
# <a name="swbemsecurityimpersonationlevel-property"></a><span data-ttu-id="7ed5f-103">SWbemSecurity. ImpersonationLevel, propriété</span><span class="sxs-lookup"><span data-stu-id="7ed5f-103">SWbemSecurity.ImpersonationLevel property</span></span>

<span data-ttu-id="7ed5f-104">La propriété **ImpersonationLevel** est un entier qui définit le niveau d’emprunt d’identité com affecté à cet objet.</span><span class="sxs-lookup"><span data-stu-id="7ed5f-104">The **ImpersonationLevel** property is an integer that defines the COM impersonation level that is assigned to this object.</span></span> <span data-ttu-id="7ed5f-105">Ce paramètre détermine si les processus appartenant à Windows Management Instrumentation (WMI) peuvent détecter ou utiliser vos informations d’identification de sécurité lorsque vous effectuez des appels à d’autres processus.</span><span class="sxs-lookup"><span data-stu-id="7ed5f-105">This setting determines if processes owned by Windows Management Instrumentation (WMI) can detect or use your security credentials when making calls to other processes.</span></span> <span data-ttu-id="7ed5f-106">Pour plus d’informations sur les niveaux d’emprunt d’identité, consultez Définition de la [ \_ sécurité des \_ processus de l’application cliente](setting-client-application-process-security.md).</span><span class="sxs-lookup"><span data-stu-id="7ed5f-106">For more information about impersonation levels, see [Setting Client\_Application\_Process Security](setting-client-application-process-security.md).</span></span>

<span data-ttu-id="7ed5f-107">Si vous ne définissez pas spécifiquement le niveau d’emprunt d’identité dans un moniker, ou en définissant la propriété **SWBemSecurity. ImpersonationLevel** sur un objet sécurisable, WMI définit le niveau d’emprunt d’identité par défaut sur la valeur spécifiée dans la [clé de Registre niveau d’emprunt d’identité par défaut](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="7ed5f-107">If you do not set the impersonation level specifically in either a moniker, or by setting the **SWBemSecurity.ImpersonationLevel** property on a securable object, WMI sets the default impersonation level to the value specified in the [default impersonation level registry key](setting-the-default-process-security-level-using-vbscript.md).</span></span> <span data-ttu-id="7ed5f-108">Si ce paramètre n’est pas suffisant, le fournisseur ne prend pas en service votre demande et l’appel à l’API WMI peut échouer avec un code d’erreur **wbemErrAccessDenied** (2147749891/0x80041003).</span><span class="sxs-lookup"><span data-stu-id="7ed5f-108">If this setting is not sufficient, the provider does not service your request, and the call to the WMI API can fail with an error code of **wbemErrAccessDenied** (2147749891/0x80041003).</span></span>

<span data-ttu-id="7ed5f-109">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="7ed5f-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="7ed5f-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="7ed5f-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ed5f-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ed5f-111">Syntax</span></span>


```VB
SWbemSecurity.ImpersonationLevel As Integer
```



## <a name="property-value"></a><span data-ttu-id="7ed5f-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="7ed5f-112">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="7ed5f-113">Notes</span><span class="sxs-lookup"><span data-stu-id="7ed5f-113">Remarks</span></span>

<span data-ttu-id="7ed5f-114">En tant que niveau d’emprunt d’identité DCOM, cette propriété peut être définie sur l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="7ed5f-114">As a DCOM impersonation level, this property can be set to one of the following values:</span></span>



| <span data-ttu-id="7ed5f-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ed5f-115">Value</span></span>           | <span data-ttu-id="7ed5f-116">Description</span><span class="sxs-lookup"><span data-stu-id="7ed5f-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ed5f-117">**Anonyme**</span><span class="sxs-lookup"><span data-stu-id="7ed5f-117">**Anonymous**</span></span>   | <span data-ttu-id="7ed5f-118">Masque les informations d'identification de l'appelant.</span><span class="sxs-lookup"><span data-stu-id="7ed5f-118">Hides the credentials of the caller.</span></span> <span data-ttu-id="7ed5f-119">WMI ne prend pas en charge ce niveau d’emprunt d’identité. Si un script spécifie impersonationLevel = Anonymous, WMI met à niveau silencieusement le niveau d’emprunt d’identité pour identifier.</span><span class="sxs-lookup"><span data-stu-id="7ed5f-119">WMI does not actually support this impersonation level; if a script specifies impersonationLevel=Anonymous, WMI will silently upgrade the impersonation level to Identify.</span></span> <span data-ttu-id="7ed5f-120">Il s’agit d’un exercice non significatif, toutefois, car les scripts utilisant le niveau d’identification risquent d’échouer.</span><span class="sxs-lookup"><span data-stu-id="7ed5f-120">This is in some ways a meaningless exercise, however, because scripts using the Identify level are likely to fail.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="7ed5f-121">**Repérer**</span><span class="sxs-lookup"><span data-stu-id="7ed5f-121">**Identify**</span></span>    | <span data-ttu-id="7ed5f-122">Permet aux objets d’interroger les informations d’identification de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7ed5f-122">Enables objects to query the credentials of the caller.</span></span> <span data-ttu-id="7ed5f-123">Les scripts utilisant ce niveau d’emprunt d’identité risquent d’échouer ; le niveau d’identification ne vous permet généralement pas de vérifier les listes de contrôle d’accès.</span><span class="sxs-lookup"><span data-stu-id="7ed5f-123">Scripts using this impersonation level are likely to fail; the Identify level typically lets you do no more than check access control lists.</span></span> <span data-ttu-id="7ed5f-124">Vous ne pouvez pas exécuter de scripts sur des ordinateurs distants à l’aide de l’identification.</span><span class="sxs-lookup"><span data-stu-id="7ed5f-124">You will not be able to run scripts against remote computers using Identify.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="7ed5f-125">**Impersonate**</span><span class="sxs-lookup"><span data-stu-id="7ed5f-125">**Impersonate**</span></span> | <span data-ttu-id="7ed5f-126">Permet aux objets d’utiliser les informations d’identification de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7ed5f-126">Enables objects to use the credentials of the caller.</span></span> <span data-ttu-id="7ed5f-127">Il est recommandé d’utiliser ce niveau d’emprunt d’identité avec les scripts WMI.</span><span class="sxs-lookup"><span data-stu-id="7ed5f-127">It is recommended that you use this impersonation level with WMI scripts.</span></span> <span data-ttu-id="7ed5f-128">Dans ce cas, le script WMI utilise les informations d’identification de l’utilisateur. par conséquent, il sera en mesure d’effectuer toutes les tâches que vous êtes en mesure d’effectuer.</span><span class="sxs-lookup"><span data-stu-id="7ed5f-128">When you do so, the WMI script will use your user credentials; as a result, it will be able to perform any tasks that you are able to perform.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="7ed5f-129">**Délégué**</span><span class="sxs-lookup"><span data-stu-id="7ed5f-129">**Delegate**</span></span>    | <span data-ttu-id="7ed5f-130">Permet aux objets d’autoriser d’autres objets à utiliser les informations d’identification de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7ed5f-130">Enables objects to permit other objects to use the credentials of the caller.</span></span> <span data-ttu-id="7ed5f-131">La délégation permet à un script d’utiliser vos informations d’identification sur un ordinateur distant, puis permet à cet ordinateur distant d’utiliser vos informations d’identification sur un autre ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="7ed5f-131">Delegation allows a script to use your credentials on a remote computer and then enables that remote computer to use your credentials on another remote computer.</span></span> <span data-ttu-id="7ed5f-132">Bien que vous puissiez utiliser ce niveau d’emprunt d’identité dans les scripts WMI, vous devez le faire uniquement si nécessaire, car cela peut poser un risque pour la sécurité.</span><span class="sxs-lookup"><span data-stu-id="7ed5f-132">While you can use this impersonation level within WMI scripts, you should do so only if necessary because it might pose a security risk.</span></span><br/> <span data-ttu-id="7ed5f-133">Vous ne pouvez pas utiliser le niveau d’emprunt d’identité de délégué, sauf si tous les comptes d’utilisateur et les comptes d’ordinateur impliqués dans la transaction ont tous été marqués comme approuvés pour la délégation dans Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7ed5f-133">You cannot use the Delegate impersonation level unless all the user accounts and computer accounts involved in the transaction have all been marked as Trusted for delegation in Active Directory.</span></span> <span data-ttu-id="7ed5f-134">Cela permet de réduire les risques de sécurité.</span><span class="sxs-lookup"><span data-stu-id="7ed5f-134">This helps minimize the security risks.</span></span> <span data-ttu-id="7ed5f-135">Bien qu’un ordinateur distant puisse utiliser vos informations d’identification, il ne peut le faire que si celui-ci et les autres ordinateurs impliqués dans la transaction sont approuvés pour la délégation.</span><span class="sxs-lookup"><span data-stu-id="7ed5f-135">Although a remote computer can use your credentials, it can do so only if both it and any other computers involved in the transaction are trusted for delegation.</span></span><br/> |



 

<span data-ttu-id="7ed5f-136">Comme indiqué précédemment, l’emprunt d’identité anonyme masque vos informations d’identification et identifie l’autorisation d’un objet distant à interroger vos informations d’identification, mais l’objet distant ne peut pas emprunter l’identité de votre contexte de sécurité.</span><span class="sxs-lookup"><span data-stu-id="7ed5f-136">As noted, Anonymous impersonation hides your credentials and Identify permits a remote object to query your credentials, but the remote object cannot impersonate your security context.</span></span> <span data-ttu-id="7ed5f-137">(En d’autres termes, bien que l’objet distant sache qui vous êtes, il ne peut pas être « prétend ».) Les scripts WMI qui accèdent à des ordinateurs distants en utilisant l’un de ces deux paramètres échouent généralement.</span><span class="sxs-lookup"><span data-stu-id="7ed5f-137">(In other words, although the remote object knows who you are, it cannot "pretend" to be you.) WMI scripts accessing remote computers using one of these two settings will generally fail.</span></span> <span data-ttu-id="7ed5f-138">En fait, la plupart des scripts exécutés sur l’ordinateur local à l’aide de l’un de ces deux paramètres échouent également.</span><span class="sxs-lookup"><span data-stu-id="7ed5f-138">In fact, most scripts run on the local computer using one of these two settings will also fail.</span></span>

<span data-ttu-id="7ed5f-139">Impersonate permet au service WMI distant d’utiliser votre contexte de sécurité pour effectuer l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="7ed5f-139">Impersonate permits the remote WMI service to use your security context to perform the requested operation.</span></span> <span data-ttu-id="7ed5f-140">Une demande WMI distante qui utilise le paramètre Impersonate fonctionne généralement, à condition que vos informations d’identification aient des privilèges suffisants pour effectuer l’opération prévue.</span><span class="sxs-lookup"><span data-stu-id="7ed5f-140">A remote WMI request that uses the Impersonate setting typically succeeds, provided your credentials have sufficient privileges to perform the intended operation.</span></span> <span data-ttu-id="7ed5f-141">En d’autres termes, vous ne pouvez pas utiliser WMI pour effectuer une action (à distance ou autre) que vous n’avez pas l’autorisation d’effectuer en dehors de WMI.</span><span class="sxs-lookup"><span data-stu-id="7ed5f-141">In other words, you cannot use WMI to perform an action (remotely or otherwise) that you do not have permission to perform outside WMI.</span></span>

<span data-ttu-id="7ed5f-142">La définition de impersonationLevel à déléguer permet au service WMI distant de transmettre vos informations d’identification à d’autres objets et est généralement considéré comme un risque pour la sécurité.</span><span class="sxs-lookup"><span data-stu-id="7ed5f-142">Setting impersonationLevel to Delegate permits the remote WMI service to pass your credentials on to other objects and is generally considered a security risk.</span></span>

<span data-ttu-id="7ed5f-143">Vous pouvez définir le niveau d’emprunt d’identité d’un objet [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md)et [**SwbemLocator**](swbemlocator.md) en affectant à la propriété **ImpersonationLevel** la valeur souhaitée.</span><span class="sxs-lookup"><span data-stu-id="7ed5f-143">You can set the impersonation level of an [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md), and [**SwbemLocator**](swbemlocator.md) object by setting the **ImpersonationLevel** property to the desired value.</span></span> <span data-ttu-id="7ed5f-144">L’exemple suivant montre comment définir le niveau d’emprunt d’identité pour un objet **SWbemObject** :</span><span class="sxs-lookup"><span data-stu-id="7ed5f-144">The following example shows you how to set the impersonation level for an **SWbemObject** object:</span></span>


```VB
objinstance.Security_.ImpersonationLevel = _
    wbemImpersonationLevelImpersonate
```



<span data-ttu-id="7ed5f-145">Vous pouvez également spécifier des niveaux d’emprunt d’identité dans le cadre d’un moniker.</span><span class="sxs-lookup"><span data-stu-id="7ed5f-145">You can also specify impersonation levels as part of a moniker.</span></span> <span data-ttu-id="7ed5f-146">L’exemple suivant définit le niveau d’authentification et le niveau d’emprunt d’identité, et récupère une instance [**du \_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="7ed5f-146">The following example sets the authentication level and the impersonation level, and retrieves an instance of [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>


```VB
Set objinst = GetObject("WinMgmts:{impersonationLevel=impersonate,"& _
                         "authenticationLevel=pktPrivacy}"& _
                         "!root/cimv2:Win32_service='ALERTER'")
```



## <a name="requirements"></a><span data-ttu-id="7ed5f-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7ed5f-147">Requirements</span></span>



| <span data-ttu-id="7ed5f-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ed5f-148">Requirement</span></span> | <span data-ttu-id="7ed5f-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ed5f-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ed5f-150">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ed5f-150">Minimum supported client</span></span><br/> | <span data-ttu-id="7ed5f-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7ed5f-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7ed5f-152">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ed5f-152">Minimum supported server</span></span><br/> | <span data-ttu-id="7ed5f-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7ed5f-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7ed5f-154">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="7ed5f-154">Type library</span></span><br/>             | <dl> <span data-ttu-id="7ed5f-155"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7ed5f-155"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7ed5f-156">DLL</span><span class="sxs-lookup"><span data-stu-id="7ed5f-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ed5f-157"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ed5f-157"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7ed5f-158">CLSID</span><span class="sxs-lookup"><span data-stu-id="7ed5f-158">CLSID</span></span><br/>                    | <span data-ttu-id="7ed5f-159">CLSID \_ SWbemSecurity</span><span class="sxs-lookup"><span data-stu-id="7ed5f-159">CLSID\_SWbemSecurity</span></span><br/>                                                         |
| <span data-ttu-id="7ed5f-160">IID</span><span class="sxs-lookup"><span data-stu-id="7ed5f-160">IID</span></span><br/>                      | <span data-ttu-id="7ed5f-161">IID \_ ISWbemSecurity</span><span class="sxs-lookup"><span data-stu-id="7ed5f-161">IID\_ISWbemSecurity</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="7ed5f-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ed5f-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ed5f-163">**SWbemSecurity**</span><span class="sxs-lookup"><span data-stu-id="7ed5f-163">**SWbemSecurity**</span></span>](swbemsecurity.md)
</dt> <dt>

[<span data-ttu-id="7ed5f-164">Définition de la sécurité des processus d' \_ application cliente \_</span><span class="sxs-lookup"><span data-stu-id="7ed5f-164">Setting Client\_Application\_Process Security</span></span>](setting-client-application-process-security.md)
</dt> <dt>

[<span data-ttu-id="7ed5f-165">**WbemImpersonationLevelEnum**</span><span class="sxs-lookup"><span data-stu-id="7ed5f-165">**WbemImpersonationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> </dl>

 

