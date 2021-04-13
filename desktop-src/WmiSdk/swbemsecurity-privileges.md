---
description: La propriété Privileges est un objet SWbemPrivilegeSet. Cette propriété est utilisée pour activer ou désactiver des privilèges Windows spécifiques. Vous devrez peut-être définir l’un de ces privilèges pour effectuer des tâches spécifiques à l’aide de l’API Windows Management Instrumentation (WMI).
ms.assetid: 6e4cae22-23d6-4981-b38c-d298654e59ab
ms.tgt_platform: multiple
title: SWbemSecurity. Privileges, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity.Privileges
- ISWbemSecurity.Privileges
- ISWbemSecurity.get_Privileges
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6fd8e1c0f9b6667b49d0956bcea5ac9e187443d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202147"
---
# <a name="swbemsecurityprivileges-property"></a><span data-ttu-id="71d65-105">SWbemSecurity. Privileges, propriété</span><span class="sxs-lookup"><span data-stu-id="71d65-105">SWbemSecurity.Privileges property</span></span>

<span data-ttu-id="71d65-106">La propriété **Privileges** est un objet [**SWbemPrivilegeSet**](swbemprivilegeset.md) .</span><span class="sxs-lookup"><span data-stu-id="71d65-106">The **Privileges** property is an [**SWbemPrivilegeSet**](swbemprivilegeset.md) object.</span></span> <span data-ttu-id="71d65-107">Cette propriété est utilisée pour activer ou désactiver des privilèges Windows spécifiques.</span><span class="sxs-lookup"><span data-stu-id="71d65-107">This property is used to enable or disable specific Windows privileges.</span></span> <span data-ttu-id="71d65-108">Vous devrez peut-être définir l’un de ces privilèges pour effectuer des tâches spécifiques à l’aide de l’API Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="71d65-108">You may need to set one of these privileges to perform specific tasks using the Windows Management Instrumentation (WMI) API.</span></span>

<span data-ttu-id="71d65-109">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="71d65-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="71d65-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="71d65-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="71d65-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="71d65-111">Syntax</span></span>


```VB
SWbemSecurity.Privileges As Object
```



## <a name="property-value"></a><span data-ttu-id="71d65-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="71d65-112">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="71d65-113">Notes</span><span class="sxs-lookup"><span data-stu-id="71d65-113">Remarks</span></span>

<span data-ttu-id="71d65-114">Ce paramètre vous permet d’accorder ou de révoquer des privilèges dans le cadre d’une chaîne de moniker WMI.</span><span class="sxs-lookup"><span data-stu-id="71d65-114">This setting allows you to grant or revoke privileges as part of a WMI moniker string.</span></span> <span data-ttu-id="71d65-115">Pour obtenir la liste complète des valeurs applicables, consultez [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) et [**constantes de privilège**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="71d65-115">For the complete list of applicable values, see [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) and [**Privilege Constants**](privilege-constants.md).</span></span>

<span data-ttu-id="71d65-116">Vous pouvez modifier les privilèges définis pour les objets [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md)et [**SwbemLocator**](swbemlocator.md) en ajoutant des objets [**SWbemPrivilege**](swbemprivilege.md) à la propriété **Privileges** .</span><span class="sxs-lookup"><span data-stu-id="71d65-116">You can change the privileges defined for the [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md), and [**SwbemLocator**](swbemlocator.md) objects by adding [**SWbemPrivilege**](swbemprivilege.md) objects to the **Privileges** property.</span></span>

<span data-ttu-id="71d65-117">Il existe des différences fondamentales dans la façon dont les différentes versions de Windows gèrent les modifications des privilèges.</span><span class="sxs-lookup"><span data-stu-id="71d65-117">There are fundamental differences in how different versions of Windows handle changes to privileges.</span></span> <span data-ttu-id="71d65-118">Si vous développez une application qui est utilisée uniquement sur des plateformes Windows, vous pouvez définir ou révoquer des privilèges à tout moment.</span><span class="sxs-lookup"><span data-stu-id="71d65-118">If you are developing an application that is only used on Windows platforms, you can set or revoke privileges at any time.</span></span>

<span data-ttu-id="71d65-119">L’exemple suivant définit **SeDebugPrivilege** sur la connexion initiale du moniker pour obtenir un objet [**SWbemServices**](swbemservices.md) .</span><span class="sxs-lookup"><span data-stu-id="71d65-119">The following example sets the **SeDebugPrivilege** on the initial moniker connection to obtain an [**SWbemServices**](swbemservices.md) object.</span></span>


```VB
Set Service = GetObject( _
    "winmgmts:{impersonationLevel=impersonate, (Debug)}")
```



<span data-ttu-id="71d65-120">Pour plus d’informations sur la façon de mettre en forme la chaîne de sécurité pour une connexion de moniker, consultez [**constantes de privilège**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="71d65-120">For more information about how to format the security string for a moniker connection, see [**Privilege Constants**](privilege-constants.md).</span></span>

<span data-ttu-id="71d65-121">L’exemple suivant effectue la même tâche, mais définit le privilège après la connexion initiale à WMI.</span><span class="sxs-lookup"><span data-stu-id="71d65-121">The following example performs the same task, but it sets the privilege after the initial log on to WMI.</span></span>


```VB
Set Service = GetObject( _
    "winmgmts:{impersonationLevel=impersonate}")
Service.Security_.Privileges.AddAsString "SeDebugPrivilege", True
```



<span data-ttu-id="71d65-122">Notez que pour les appels à [**SwbemPrivilegeSet. AddAsString**](swbemprivilegeset-addasstring.md), vous devez utiliser le nom complet du privilège de sécurité, par exemple, « SeDebugPrivilege » au lieu de « Debug ».</span><span class="sxs-lookup"><span data-stu-id="71d65-122">Note that for calls to [**SwbemPrivilegeSet.AddAsString**](swbemprivilegeset-addasstring.md), you must use the full name of the security privilege, for example, "SeDebugPrivilege" instead of "Debug".</span></span>

## <a name="requirements"></a><span data-ttu-id="71d65-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71d65-123">Requirements</span></span>



| <span data-ttu-id="71d65-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71d65-124">Requirement</span></span> | <span data-ttu-id="71d65-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="71d65-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="71d65-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71d65-126">Minimum supported client</span></span><br/> | <span data-ttu-id="71d65-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="71d65-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="71d65-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71d65-128">Minimum supported server</span></span><br/> | <span data-ttu-id="71d65-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="71d65-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="71d65-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="71d65-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="71d65-131"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="71d65-131"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="71d65-132">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="71d65-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="71d65-133"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="71d65-133"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="71d65-134">DLL</span><span class="sxs-lookup"><span data-stu-id="71d65-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71d65-135"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71d65-135"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="71d65-136">CLSID</span><span class="sxs-lookup"><span data-stu-id="71d65-136">CLSID</span></span><br/>                    | <span data-ttu-id="71d65-137">CLSID \_ SWbemSecurity</span><span class="sxs-lookup"><span data-stu-id="71d65-137">CLSID\_SWbemSecurity</span></span><br/>                                                         |
| <span data-ttu-id="71d65-138">IID</span><span class="sxs-lookup"><span data-stu-id="71d65-138">IID</span></span><br/>                      | <span data-ttu-id="71d65-139">IID \_ ISWbemSecurity</span><span class="sxs-lookup"><span data-stu-id="71d65-139">IID\_ISWbemSecurity</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="71d65-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71d65-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71d65-141">**SWbemSecurity**</span><span class="sxs-lookup"><span data-stu-id="71d65-141">**SWbemSecurity**</span></span>](swbemsecurity.md)
</dt> <dt>

[<span data-ttu-id="71d65-142">Exécution des opérations privilégiées</span><span class="sxs-lookup"><span data-stu-id="71d65-142">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="71d65-143">**SWbemPrivilegeSet**</span><span class="sxs-lookup"><span data-stu-id="71d65-143">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)
</dt> </dl>

 

 




