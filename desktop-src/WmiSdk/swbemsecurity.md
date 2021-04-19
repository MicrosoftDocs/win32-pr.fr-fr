---
description: L’objet SWbemSecurity obtient ou définit des paramètres de sécurité, tels que des privilèges, des emprunts d’identité COM et des niveaux d’authentification affectés à un objet.
ms.assetid: 794587fa-5feb-455b-be28-ecfaa25625ad
ms.tgt_platform: multiple
title: Objet SWbemSecurity (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity
- ISWbemSecurity
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: da59c3b996a80384c133336503124141f0907f79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516981"
---
# <a name="swbemsecurity-object"></a><span data-ttu-id="b99d5-103">Objet SWbemSecurity</span><span class="sxs-lookup"><span data-stu-id="b99d5-103">SWbemSecurity object</span></span>

<span data-ttu-id="b99d5-104">L’objet **SWbemSecurity** obtient ou définit des paramètres de sécurité, tels que des privilèges, des emprunts d’identité com et des niveaux d’authentification affectés à un objet.</span><span class="sxs-lookup"><span data-stu-id="b99d5-104">The **SWbemSecurity** object gets or sets security settings, such as privileges, COM impersonations, and authentication levels assigned to an object.</span></span> <span data-ttu-id="b99d5-105">Les objets [**SWbemLocator**](swbemlocator.md), [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md), [**SWbemLastError**](swbemlasterror.md)et [**SWbemEventSource**](swbemeventsource.md) ont une propriété **de \_ sécurité** , qui est l’objet **SWbemSecurity** .</span><span class="sxs-lookup"><span data-stu-id="b99d5-105">The [**SWbemLocator**](swbemlocator.md), [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md), [**SWbemLastError**](swbemlasterror.md), and [**SWbemEventSource**](swbemeventsource.md) objects have a **Security\_** property, which is the **SWbemSecurity** object.</span></span> <span data-ttu-id="b99d5-106">Lorsque vous récupérez une instance ou affichez le journal de sécurité WMI, vous devrez peut-être définir les propriétés de l’objet de **sécurité \_** .</span><span class="sxs-lookup"><span data-stu-id="b99d5-106">When you retrieve an instance or view the WMI security log, you might need to set the properties of the **Security\_** object.</span></span>

<span data-ttu-id="b99d5-107">L’appel de VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) ne peut pas créer l’objet de sécurité.</span><span class="sxs-lookup"><span data-stu-id="b99d5-107">The VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) call cannot create the Security object.</span></span> <span data-ttu-id="b99d5-108">Les paramètres de sécurité de cet objet n’identifient pas les paramètres d’authentification, d’emprunt d’identité ou de privilège sur une connexion à WMI, ou la sécurité en vigueur pour le proxy lorsqu’un objet est remis à un récepteur dans un appel asynchrone.</span><span class="sxs-lookup"><span data-stu-id="b99d5-108">The security settings in this object do not identify the authentication, impersonation, or privilege settings on a connection to WMI, or the security in effect for the proxy when an object is delivered to a sink in an asynchronous call.</span></span> <span data-ttu-id="b99d5-109">Pour plus d’informations, consultez [maintenance de la sécurité WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="b99d5-109">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

## <a name="members"></a><span data-ttu-id="b99d5-110">Membres</span><span class="sxs-lookup"><span data-stu-id="b99d5-110">Members</span></span>

<span data-ttu-id="b99d5-111">L’objet **SWbemSecurity** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b99d5-111">The **SWbemSecurity** object has these types of members:</span></span>

-   [<span data-ttu-id="b99d5-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b99d5-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b99d5-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b99d5-113">Properties</span></span>

<span data-ttu-id="b99d5-114">L’objet **SWbemSecurity** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="b99d5-114">The **SWbemSecurity** object has these properties.</span></span>



| <span data-ttu-id="b99d5-115">Propriété</span><span class="sxs-lookup"><span data-stu-id="b99d5-115">Property</span></span>                                                                    | <span data-ttu-id="b99d5-116">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="b99d5-116">Access type</span></span>           | <span data-ttu-id="b99d5-117">Description</span><span class="sxs-lookup"><span data-stu-id="b99d5-117">Description</span></span>                                                                                                                                                                                                                            |
|:----------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b99d5-118">**AuthenticationLevel**</span><span class="sxs-lookup"><span data-stu-id="b99d5-118">**AuthenticationLevel**</span></span>](swbemsecurity-authenticationlevel.md)<br/> | <span data-ttu-id="b99d5-119">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b99d5-119">Read/write</span></span><br/> | <span data-ttu-id="b99d5-120">Valeur numérique qui définit le niveau d’authentification COM assigné à cet objet.</span><span class="sxs-lookup"><span data-stu-id="b99d5-120">Numeric value that defines the COM Authentication level that is assigned to this object.</span></span> <span data-ttu-id="b99d5-121">Ce paramètre détermine la façon dont vous protégez les informations envoyées à partir de WMI.</span><span class="sxs-lookup"><span data-stu-id="b99d5-121">This setting determines how you protect information sent from WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="b99d5-122">**ImpersonationLevel**</span><span class="sxs-lookup"><span data-stu-id="b99d5-122">**ImpersonationLevel**</span></span>](swbemsecurity-impersonationlevel.md)<br/>   | <span data-ttu-id="b99d5-123">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b99d5-123">Read/write</span></span><br/> | <span data-ttu-id="b99d5-124">Valeur numérique qui définit le niveau d’emprunt d’identité COM assigné à cet objet.</span><span class="sxs-lookup"><span data-stu-id="b99d5-124">Numeric value that defines the COM Impersonation level that is assigned to this object.</span></span> <span data-ttu-id="b99d5-125">Ce paramètre détermine si les processus détenus par WMI peuvent détecter ou utiliser vos informations d’identification de sécurité lorsque vous effectuez des appels à d’autres processus.</span><span class="sxs-lookup"><span data-stu-id="b99d5-125">This setting determines if processes owned by WMI can detect or use your security credentials when making calls to other processes.</span></span><br/> |
| [<span data-ttu-id="b99d5-126">**Autorisations**</span><span class="sxs-lookup"><span data-stu-id="b99d5-126">**Privileges**</span></span>](swbemsecurity-privileges.md)<br/>                   | <span data-ttu-id="b99d5-127">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b99d5-127">Read-only</span></span><br/>  | <span data-ttu-id="b99d5-128">Objet [**SWbemPrivilegeSet**](swbemprivilegeset.md) qui définit des privilèges pour cet objet.</span><span class="sxs-lookup"><span data-stu-id="b99d5-128">An [**SWbemPrivilegeSet**](swbemprivilegeset.md) object that defines privileges for this object.</span></span> <span data-ttu-id="b99d5-129">Pour plus d’informations, consultez [exécution avec des privilèges spéciaux](/windows/desktop/SecBP/running-with-special-privileges).</span><span class="sxs-lookup"><span data-stu-id="b99d5-129">For more information, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span><br/>                    |



 

## <a name="requirements"></a><span data-ttu-id="b99d5-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b99d5-130">Requirements</span></span>



| <span data-ttu-id="b99d5-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b99d5-131">Requirement</span></span> | <span data-ttu-id="b99d5-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="b99d5-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b99d5-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b99d5-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b99d5-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b99d5-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b99d5-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b99d5-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b99d5-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b99d5-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b99d5-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="b99d5-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="b99d5-138"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b99d5-138"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b99d5-139">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="b99d5-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="b99d5-140"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b99d5-140"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b99d5-141">DLL</span><span class="sxs-lookup"><span data-stu-id="b99d5-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b99d5-142"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b99d5-142"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b99d5-143">CLSID</span><span class="sxs-lookup"><span data-stu-id="b99d5-143">CLSID</span></span><br/>                    | <span data-ttu-id="b99d5-144">CLSID \_ SWbemSecurity</span><span class="sxs-lookup"><span data-stu-id="b99d5-144">CLSID\_SWbemSecurity</span></span><br/>                                                         |
| <span data-ttu-id="b99d5-145">IID</span><span class="sxs-lookup"><span data-stu-id="b99d5-145">IID</span></span><br/>                      | <span data-ttu-id="b99d5-146">IID \_ ISWbemSecurity</span><span class="sxs-lookup"><span data-stu-id="b99d5-146">IID\_ISWbemSecurity</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="b99d5-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b99d5-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b99d5-148">Scripts d’objets d’API</span><span class="sxs-lookup"><span data-stu-id="b99d5-148">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> <dt>

[<span data-ttu-id="b99d5-149">Maintenance de la sécurité WMI</span><span class="sxs-lookup"><span data-stu-id="b99d5-149">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> <dt>

[<span data-ttu-id="b99d5-150">Définition de la sécurité des processus d' \_ application cliente \_</span><span class="sxs-lookup"><span data-stu-id="b99d5-150">Setting Client\_Application\_Process Security</span></span>](setting-client-application-process-security.md)
</dt> <dt>

[<span data-ttu-id="b99d5-151">**WbemAuthenticationLevelEnum**</span><span class="sxs-lookup"><span data-stu-id="b99d5-151">**WbemAuthenticationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[<span data-ttu-id="b99d5-152">**WbemImpersonationLevelEnum**</span><span class="sxs-lookup"><span data-stu-id="b99d5-152">**WbemImpersonationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> <dt>

[<span data-ttu-id="b99d5-153">**WbemPrivilegeEnum**</span><span class="sxs-lookup"><span data-stu-id="b99d5-153">**WbemPrivilegeEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> </dl>

 

