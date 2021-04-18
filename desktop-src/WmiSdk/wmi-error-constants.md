---
description: Si une erreur se produit, WMI retourne un code d’erreur sous la forme d’une valeur HRESULT. Ces codes peuvent être renvoyés par des scripts, des applications C++ ou WMIC.
ms.assetid: b560f37c-da22-4745-8d1f-b27afdf572ec
ms.tgt_platform: multiple
title: Constantes d’erreur WMI (WbemCli. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e95db7220bdc9669716dbe19f5bf2f4e139dfe5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519816"
---
# <a name="wmi-error-constants"></a><span data-ttu-id="cca14-104">Constantes d’erreur WMI</span><span class="sxs-lookup"><span data-stu-id="cca14-104">WMI Error Constants</span></span>

<span data-ttu-id="cca14-105">Si une erreur se produit, WMI retourne un code d’erreur sous la forme d’une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cca14-105">If an error occurs, WMI returns an error code as an **HRESULT** value.</span></span> <span data-ttu-id="cca14-106">Ces codes peuvent être renvoyés par des scripts, des applications C++ ou [**WMIC**](wmic.md).</span><span class="sxs-lookup"><span data-stu-id="cca14-106">These codes may be returned by scripts, C++ applications, or [**Wmic**](wmic.md).</span></span>

> [!Note]
>
> <span data-ttu-id="cca14-107">La documentation suivante est destinée aux développeurs et aux administrateurs informatiques.</span><span class="sxs-lookup"><span data-stu-id="cca14-107">The following documentation is targeted for developers and IT administrators.</span></span> <span data-ttu-id="cca14-108">Si vous êtes un utilisateur final qui a rencontré un message d’erreur concernant WMI, vous devez accéder à [support Microsoft](https://support.microsoft.com/) et rechercher le code d’erreur que vous voyez dans le message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="cca14-108">If you are an end-user that has experienced an error message concerning WMI, you should go to [Microsoft Support](https://support.microsoft.com/) and search for the error code you see on the error message.</span></span> <span data-ttu-id="cca14-109">Pour plus d’informations sur la résolution des problèmes liés aux scripts WMI et au service WMI, consultez [WMI ne fonctionne pas](/previous-versions/tn-archive/ff406382(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="cca14-109">For more information about troubleshooting problems with WMI scripts and the WMI service, see [WMI Isn't Working!](/previous-versions/tn-archive/ff406382(v=msdn.10)).</span></span>
>
> <span data-ttu-id="cca14-110">Si WMI renvoie des messages d’erreur, sachez qu’ils ne peuvent pas indiquer des problèmes dans le service WMI ou les fournisseurs WMI.</span><span class="sxs-lookup"><span data-stu-id="cca14-110">If WMI returns error messages, be aware that they may not indicate problems in the WMI service or in WMI providers.</span></span> <span data-ttu-id="cca14-111">Les échecs peuvent provenir d’autres parties du système d’exploitation et émerger comme des erreurs via WMI.</span><span class="sxs-lookup"><span data-stu-id="cca14-111">Failures can originate in other parts of the operating system and emerge as errors through WMI.</span></span> <span data-ttu-id="cca14-112">Dans tous les cas, ne supprimez pas le référentiel WMI en tant que première action, car la suppression du dépôt peut endommager le système ou les applications installées.</span><span class="sxs-lookup"><span data-stu-id="cca14-112">Under any circumstances, do not delete the WMI repository as a first action because deleting the repository can cause damage to the system or to installed applications.</span></span>
>
> <span data-ttu-id="cca14-113">Pour obtenir plus d’informations sur la source du problème, vous pouvez télécharger et exécuter l’outil en ligne de commande [WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) diagnostic.</span><span class="sxs-lookup"><span data-stu-id="cca14-113">To obtain more information about the source of the problem, you can download and run the [WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) diagnostic command line tool.</span></span> <span data-ttu-id="cca14-114">Cet outil génère un rapport qui peut généralement isoler la source du problème et fournir des instructions sur la façon de le résoudre.</span><span class="sxs-lookup"><span data-stu-id="cca14-114">This tool produces a report that can usually isolate the source of the problem and provide instructions on how to fix it.</span></span> <span data-ttu-id="cca14-115">Le rapport aide également les services de support technique Microsoft à vous aider.</span><span class="sxs-lookup"><span data-stu-id="cca14-115">The report also aids Microsoft support services in assisting you.</span></span> <span data-ttu-id="cca14-116">Vous pouvez télécharger les WMI Diagnosis Utility [ici](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).</span><span class="sxs-lookup"><span data-stu-id="cca14-116">You can download the WMI Diagnosis Utility [here](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).</span></span>

 

<span data-ttu-id="cca14-117">Certaines méthodes des classes WMI peuvent retourner des codes d’erreur système et réseau (64, par exemple).</span><span class="sxs-lookup"><span data-stu-id="cca14-117">Some methods in WMI classes can return system and network error codes (64 for example).</span></span> <span data-ttu-id="cca14-118">Vous pouvez vérifier la définition de ces types de codes d’erreur à l’aide de la commande **net helpmsg** dans la fenêtre d’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="cca14-118">You can check the definition of these types of error codes by using the **net helpmsg** command in the command prompt window.</span></span> <span data-ttu-id="cca14-119">Par exemple, la commande **net helpmsg 64** retourne le message : le nom réseau spécifié n’est plus disponible.</span><span class="sxs-lookup"><span data-stu-id="cca14-119">For example, the command **net helpmsg 64** returns the message: The specified network name is no longer available.</span></span>

<span data-ttu-id="cca14-120">La liste suivante répertorie certaines plages d’erreurs courantes.</span><span class="sxs-lookup"><span data-stu-id="cca14-120">The following list lists some common ranges of errors.</span></span>

<dl> <dt>

<span data-ttu-id="cca14-121"><span id="0x80041068_-_0x80041099"></span><span id="0X80041068_-_0X80041099"></span>0x80041068 - 0x80041099</span><span class="sxs-lookup"><span data-stu-id="cca14-121"><span id="0x80041068_-_0x80041099"></span><span id="0X80041068_-_0X80041099"></span>0x80041068 - 0x80041099</span></span>
</dt> <dd>

<span data-ttu-id="cca14-122">Erreurs qui proviennent de WMI lui-même.</span><span class="sxs-lookup"><span data-stu-id="cca14-122">Errors that originate in WMI itself.</span></span>

<span data-ttu-id="cca14-123">Une opération WMI spécifique a échoué en raison de</span><span class="sxs-lookup"><span data-stu-id="cca14-123">A specific WMI operation failed because of</span></span>

-   <span data-ttu-id="cca14-124">Une erreur dans la requête, par exemple, une requête WQL échoue ou le compte ne dispose pas des autorisations appropriées.</span><span class="sxs-lookup"><span data-stu-id="cca14-124">An error in the request, for example, a WQL query fails or the account does not have the correct permissions.</span></span>
-   <span data-ttu-id="cca14-125">Un problème d’infrastructure WMI, tel qu’une inscription CIM ou DCOM incorrecte.</span><span class="sxs-lookup"><span data-stu-id="cca14-125">A WMI infrastructure problem, such as incorrect CIM or DCOM registration.</span></span>

</dd> <dt>

<span data-ttu-id="cca14-126"><span id="0x8007xxxx"></span><span id="0X8007XXXX"></span>0x8007xxxx</span><span class="sxs-lookup"><span data-stu-id="cca14-126"><span id="0x8007xxxx"></span><span id="0X8007XXXX"></span>0x8007xxxx</span></span>
</dt> <dd>

<span data-ttu-id="cca14-127">Erreurs provenant du système d’exploitation principal.</span><span class="sxs-lookup"><span data-stu-id="cca14-127">Errors originating in the core operating system.</span></span> <span data-ttu-id="cca14-128">WMI peut renvoyer ce type d’erreur en raison d’une défaillance externe, par exemple, une défaillance de sécurité DCOM.</span><span class="sxs-lookup"><span data-stu-id="cca14-128">WMI may return this type of error because of an external failure, for example, DCOM security failure.</span></span>

</dd> <dt>

<span data-ttu-id="cca14-129"><span id="0x80040xxx"></span><span id="0X80040XXX"></span>0x80040xxx</span><span class="sxs-lookup"><span data-stu-id="cca14-129"><span id="0x80040xxx"></span><span id="0X80040XXX"></span>0x80040xxx</span></span>
</dt> <dd>

<span data-ttu-id="cca14-130">Erreurs provenant de DCOM.</span><span class="sxs-lookup"><span data-stu-id="cca14-130">Errors originating in DCOM.</span></span> <span data-ttu-id="cca14-131">Par exemple, la configuration DCOM pour les opérations sur un ordinateur distant est peut-être incorrecte.</span><span class="sxs-lookup"><span data-stu-id="cca14-131">For example, the DCOM configuration for operations to a remote computer may be incorrect.</span></span>

</dd> <dt>

<span data-ttu-id="cca14-132"><span id="0x8005xxxx"></span><span id="0X8005XXXX"></span>0x8005xxxx</span><span class="sxs-lookup"><span data-stu-id="cca14-132"><span id="0x8005xxxx"></span><span id="0X8005XXXX"></span>0x8005xxxx</span></span>
</dt> <dd>

<span data-ttu-id="cca14-133">Erreur provenant d’ADSI (Active Directory Service Interfaces) ou LDAP (Lightweight Directory Access Protocol), par exemple, un échec d’accès Active Directory lors de l’utilisation des fournisseurs de Active Directory WMI.</span><span class="sxs-lookup"><span data-stu-id="cca14-133">Error originating from ADSI (Active Directory Service Interfaces) or LDAP (Lightweight Directory Access Protocol), for example, an Active Directory access failure when using the WMI Active Directory providers.</span></span>

</dd> </dl>

<span data-ttu-id="cca14-134">Certaines méthodes des classes WMI peuvent retourner des codes d’erreur système et réseau (64, par exemple).</span><span class="sxs-lookup"><span data-stu-id="cca14-134">Some methods in WMI classes can return system and network error codes (64 for example).</span></span> <span data-ttu-id="cca14-135">Vous pouvez vérifier la définition de ces types de codes d’erreur à l’aide de la commande **net helpmsg** dans la fenêtre d’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="cca14-135">You can check the definition of these types of error codes by using the **net helpmsg** command in the command prompt window.</span></span> <span data-ttu-id="cca14-136">Par exemple, la commande **net helpmsg 64** retourne le message : le nom réseau spécifié n’est plus disponible.</span><span class="sxs-lookup"><span data-stu-id="cca14-136">For example, the command **net helpmsg 64** returns the message: The specified network name is no longer available.</span></span> <span data-ttu-id="cca14-137">En C++, vous pouvez appeler [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) et spécifier le module de message **C : \\ Windows \\ system32 \\ WBEM \\wmiutils.dll** .</span><span class="sxs-lookup"><span data-stu-id="cca14-137">In C++, you can call [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) and specify **C:\\Windows\\System32\\wbem\\wmiutils.dll** as the message module.</span></span>

<dl> <dt>

<span data-ttu-id="cca14-138"><span id="WBEM_E_FAILED"></span><span id="wbem_e_failed"></span>**échec de WBEM \_ E \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-138"><span id="WBEM_E_FAILED"></span><span id="wbem_e_failed"></span>**WBEM\_E\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-139">2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="cca14-139">2147749889 (0x80041001)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-140">Échec de l’appel.</span><span class="sxs-lookup"><span data-stu-id="cca14-140">Call failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-141"><span id="WBEM_E_NOT_FOUND"></span><span id="wbem_e_not_found"></span>**WBEM \_ E \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="cca14-141"><span id="WBEM_E_NOT_FOUND"></span><span id="wbem_e_not_found"></span>**WBEM\_E\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-142">2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="cca14-142">2147749890 (0x80041002)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-143">L’objet est introuvable.</span><span class="sxs-lookup"><span data-stu-id="cca14-143">Object cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-144"><span id="WBEM_E_ACCESS_DENIED"></span><span id="wbem_e_access_denied"></span>**\_accès WBEM \_ E \_ refusé**</span><span class="sxs-lookup"><span data-stu-id="cca14-144"><span id="WBEM_E_ACCESS_DENIED"></span><span id="wbem_e_access_denied"></span>**WBEM\_E\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-145">2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="cca14-145">2147749891 (0x80041003)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-146">L’utilisateur actuel n’est pas autorisé à effectuer l’action.</span><span class="sxs-lookup"><span data-stu-id="cca14-146">Current user does not have permission to perform the action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-147"><span id="WBEM_E_PROVIDER_FAILURE"></span><span id="wbem_e_provider_failure"></span>**\_échec du \_ fournisseur WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-147"><span id="WBEM_E_PROVIDER_FAILURE"></span><span id="wbem_e_provider_failure"></span>**WBEM\_E\_PROVIDER\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-148">2147749892 (0x80041004)</span><span class="sxs-lookup"><span data-stu-id="cca14-148">2147749892 (0x80041004)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-149">Le fournisseur a échoué à un moment autre que pendant l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="cca14-149">Provider has failed at some time other than during initialization.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-150"><span id="WBEM_E_TYPE_MISMATCH"></span><span id="wbem_e_type_mismatch"></span>**incompatibilité de \_ type WBEM E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-150"><span id="WBEM_E_TYPE_MISMATCH"></span><span id="wbem_e_type_mismatch"></span>**WBEM\_E\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-151">2147749893 (0x80041005)</span><span class="sxs-lookup"><span data-stu-id="cca14-151">2147749893 (0x80041005)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-152">Une incompatibilité de type s’est produite.</span><span class="sxs-lookup"><span data-stu-id="cca14-152">Type mismatch occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-153"><span id="WBEM_E_OUT_OF_MEMORY"></span><span id="wbem_e_out_of_memory"></span>**\_mémoire WBEM \_ insuffisante \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-153"><span id="WBEM_E_OUT_OF_MEMORY"></span><span id="wbem_e_out_of_memory"></span>**WBEM\_E\_OUT\_OF\_MEMORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-154">2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="cca14-154">2147749894 (0x80041006)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-155">Mémoire insuffisante pour l’opération.</span><span class="sxs-lookup"><span data-stu-id="cca14-155">Not enough memory for the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-156"><span id="WBEM_E_INVALID_CONTEXT"></span><span id="wbem_e_invalid_context"></span>**\_ \_ contexte non valide \_ WBEM**</span><span class="sxs-lookup"><span data-stu-id="cca14-156"><span id="WBEM_E_INVALID_CONTEXT"></span><span id="wbem_e_invalid_context"></span>**WBEM\_E\_INVALID\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-157">2147749895 (0x80041007)</span><span class="sxs-lookup"><span data-stu-id="cca14-157">2147749895 (0x80041007)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-158">L’objet [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="cca14-158">The [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-159"><span id="WBEM_E_INVALID_PARAMETER"></span><span id="wbem_e_invalid_parameter"></span>**\_paramètre WBEM E \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-159"><span id="WBEM_E_INVALID_PARAMETER"></span><span id="wbem_e_invalid_parameter"></span>**WBEM\_E\_INVALID\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-160">2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="cca14-160">2147749896 (0x80041008)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-161">Un des paramètres de l'appel n'est pas correct.</span><span class="sxs-lookup"><span data-stu-id="cca14-161">One of the parameters to the call is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-162"><span id="WBEM_E_NOT_AVAILABLE"></span><span id="wbem_e_not_available"></span>**WBEM \_ E \_ non \_ disponible**</span><span class="sxs-lookup"><span data-stu-id="cca14-162"><span id="WBEM_E_NOT_AVAILABLE"></span><span id="wbem_e_not_available"></span>**WBEM\_E\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-163">2147749897 (0x80041009)</span><span class="sxs-lookup"><span data-stu-id="cca14-163">2147749897 (0x80041009)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-164">La ressource, généralement un serveur distant, n’est pas disponible actuellement.</span><span class="sxs-lookup"><span data-stu-id="cca14-164">Resource, typically a remote server, is not currently available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-165"><span id="WBEM_E_CRITICAL_ERROR"></span><span id="wbem_e_critical_error"></span>**\_erreur WBEM E \_ critique \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-165"><span id="WBEM_E_CRITICAL_ERROR"></span><span id="wbem_e_critical_error"></span>**WBEM\_E\_CRITICAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-166">2147749898 (0x8004100A)</span><span class="sxs-lookup"><span data-stu-id="cca14-166">2147749898 (0x8004100A)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-167">Une erreur interne, critique et inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="cca14-167">Internal, critical, and unexpected error occurred.</span></span> <span data-ttu-id="cca14-168">Signalez l’erreur au support technique Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cca14-168">Report the error to Microsoft Technical Support.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-169"><span id="WBEM_E_INVALID_STREAM"></span><span id="wbem_e_invalid_stream"></span>**\_ \_ flux non valide \_ WBEM**</span><span class="sxs-lookup"><span data-stu-id="cca14-169"><span id="WBEM_E_INVALID_STREAM"></span><span id="wbem_e_invalid_stream"></span>**WBEM\_E\_INVALID\_STREAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-170">2147749899 (0x8004100B)</span><span class="sxs-lookup"><span data-stu-id="cca14-170">2147749899 (0x8004100B)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-171">Un ou plusieurs paquets de réseau ont été endommagés pendant une session distante.</span><span class="sxs-lookup"><span data-stu-id="cca14-171">One or more network packets were corrupted during a remote session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-172"><span id="WBEM_E_NOT_SUPPORTED"></span><span id="wbem_e_not_supported"></span>**WBEM \_ E \_ non \_ pris en charge**</span><span class="sxs-lookup"><span data-stu-id="cca14-172"><span id="WBEM_E_NOT_SUPPORTED"></span><span id="wbem_e_not_supported"></span>**WBEM\_E\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-173">2147749900 (0x8004100C)</span><span class="sxs-lookup"><span data-stu-id="cca14-173">2147749900 (0x8004100C)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-174">La fonctionnalité ou l’opération n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="cca14-174">Feature or operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-175"><span id="WBEM_E_INVALID_SUPERCLASS"></span><span id="wbem_e_invalid_superclass"></span>**la \_ \_ superclasse WBEM E non valide \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-175"><span id="WBEM_E_INVALID_SUPERCLASS"></span><span id="wbem_e_invalid_superclass"></span>**WBEM\_E\_INVALID\_SUPERCLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-176">2147749901 (0x8004100D)</span><span class="sxs-lookup"><span data-stu-id="cca14-176">2147749901 (0x8004100D)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-177">La classe parente spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="cca14-177">Parent class specified is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-178"><span id="WBEM_E_INVALID_NAMESPACE"></span><span id="wbem_e_invalid_namespace"></span>**WBEM \_ E \_ espace de noms non valide \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-178"><span id="WBEM_E_INVALID_NAMESPACE"></span><span id="wbem_e_invalid_namespace"></span>**WBEM\_E\_INVALID\_NAMESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-179">2147749902 (0x8004100E)</span><span class="sxs-lookup"><span data-stu-id="cca14-179">2147749902 (0x8004100E)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-180">L’espace de noms spécifié est introuvable.</span><span class="sxs-lookup"><span data-stu-id="cca14-180">Namespace specified cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-181"><span id="WBEM_E_INVALID_OBJECT"></span><span id="wbem_e_invalid_object"></span>**WBEM \_ E \_ objet non valide \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-181"><span id="WBEM_E_INVALID_OBJECT"></span><span id="wbem_e_invalid_object"></span>**WBEM\_E\_INVALID\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-182">2147749903 (0x8004100F)</span><span class="sxs-lookup"><span data-stu-id="cca14-182">2147749903 (0x8004100F)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-183">L’instance spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="cca14-183">Specified instance is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-184"><span id="WBEM_E_INVALID_CLASS"></span><span id="wbem_e_invalid_class"></span>**WBEM \_ - \_ classe non valide \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-184"><span id="WBEM_E_INVALID_CLASS"></span><span id="wbem_e_invalid_class"></span>**WBEM\_E\_INVALID\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-185">2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="cca14-185">2147749904 (0x80041010)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-186">La classe spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="cca14-186">Specified class is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-187"><span id="WBEM_E_PROVIDER_NOT_FOUND"></span><span id="wbem_e_provider_not_found"></span>**\_fournisseur WBEM \_ E \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="cca14-187"><span id="WBEM_E_PROVIDER_NOT_FOUND"></span><span id="wbem_e_provider_not_found"></span>**WBEM\_E\_PROVIDER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-188">2147749905 (0x80041011)</span><span class="sxs-lookup"><span data-stu-id="cca14-188">2147749905 (0x80041011)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-189">Le fournisseur référencé dans le schéma n’a pas d’inscription correspondante.</span><span class="sxs-lookup"><span data-stu-id="cca14-189">Provider referenced in the schema does not have a corresponding registration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-190"><span id="WBEM_E_INVALID_PROVIDER_REGISTRATION"></span><span id="wbem_e_invalid_provider_registration"></span>**\_inscription du \_ fournisseur non valide pour \_ WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-190"><span id="WBEM_E_INVALID_PROVIDER_REGISTRATION"></span><span id="wbem_e_invalid_provider_registration"></span>**WBEM\_E\_INVALID\_PROVIDER\_REGISTRATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-191">2147749906</span><span class="sxs-lookup"><span data-stu-id="cca14-191">2147749906</span></span>
</dt> <dt>



<span data-ttu-id="cca14-192">Le fournisseur référencé dans le schéma a une inscription incorrecte ou incomplète.</span><span class="sxs-lookup"><span data-stu-id="cca14-192">Provider referenced in the schema has an incorrect or incomplete registration.</span></span>

<span data-ttu-id="cca14-193">Cette erreur peut être due à de nombreuses conditions, y compris les suivantes :</span><span class="sxs-lookup"><span data-stu-id="cca14-193">This error may be caused by many conditions, including the following:</span></span>

-   <span data-ttu-id="cca14-194">Commande de l' [ \# espace de noms pragma](pragma-namespace.md) manquante dans le fichier format MOF (MOF) utilisé pour inscrire le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="cca14-194">A missing [\#pragma namespace](pragma-namespace.md) command in the Managed Object Format (MOF) file used to register the provider.</span></span> <span data-ttu-id="cca14-195">Le fournisseur peut être inscrit dans un espace de noms WMI incorrect.</span><span class="sxs-lookup"><span data-stu-id="cca14-195">The provider may be registered in the wrong WMI namespace.</span></span>
-   <span data-ttu-id="cca14-196">Impossible de récupérer l’inscription COM.</span><span class="sxs-lookup"><span data-stu-id="cca14-196">Failure to retrieve the COM registration.</span></span>
-   <span data-ttu-id="cca14-197">Le modèle d’hébergement n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="cca14-197">Hosting model is not valid.</span></span> <span data-ttu-id="cca14-198">Pour plus d’informations, consultez [hébergement et sécurité du fournisseur](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="cca14-198">For more information, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>
-   <span data-ttu-id="cca14-199">Une classe spécifiée dans l’inscription n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="cca14-199">An class specified in the registration is not valid.</span></span>
-   <span data-ttu-id="cca14-200">Impossible de créer une instance de ou d’hériter de la classe [**\_ \_ Win32Provider**](--win32provider.md) pour créer l’inscription du fournisseur dans le fichier MOF.</span><span class="sxs-lookup"><span data-stu-id="cca14-200">Failure to create an instance of or inherit from the [**\_\_Win32Provider**](--win32provider.md) class to create the provider registration in the MOF file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-201"><span id="WBEM_E_PROVIDER_LOAD_FAILURE"></span><span id="wbem_e_provider_load_failure"></span>**\_échec de \_ chargement du fournisseur WBEM E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-201"><span id="WBEM_E_PROVIDER_LOAD_FAILURE"></span><span id="wbem_e_provider_load_failure"></span>**WBEM\_E\_PROVIDER\_LOAD\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-202">2147749907 (0x80041013)</span><span class="sxs-lookup"><span data-stu-id="cca14-202">2147749907 (0x80041013)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-203">COM ne peut pas localiser un fournisseur référencé dans le schéma.</span><span class="sxs-lookup"><span data-stu-id="cca14-203">COM cannot locate a provider referenced in the schema.</span></span>

<span data-ttu-id="cca14-204">Cette erreur peut être due à de nombreuses conditions, y compris les suivantes :</span><span class="sxs-lookup"><span data-stu-id="cca14-204">This error may be caused by many conditions, including the following:</span></span>

-   <span data-ttu-id="cca14-205">Le fournisseur utilise une DLL WMI qui ne correspond pas au fichier. lib utilisé lors de la génération du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="cca14-205">Provider is using a WMI DLL that does not match the .lib file used when the provider was built.</span></span>
-   <span data-ttu-id="cca14-206">La DLL du fournisseur, ou l’une des dll dont elle dépend, est endommagée.</span><span class="sxs-lookup"><span data-stu-id="cca14-206">Provider's DLL, or any of the DLLs on which it depends, is corrupt.</span></span>
-   <span data-ttu-id="cca14-207">Le fournisseur n’a pas pu exporter [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver).</span><span class="sxs-lookup"><span data-stu-id="cca14-207">Provider failed to export [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver).</span></span>
-   <span data-ttu-id="cca14-208">Le fournisseur in-process n’a pas été inscrit à l’aide de la commande **regsvr32** .</span><span class="sxs-lookup"><span data-stu-id="cca14-208">In-process provider was not registered using the **regsvr32** command.</span></span>
-   <span data-ttu-id="cca14-209">Le fournisseur out-of-process n’a pas été inscrit à l’aide du commutateur **/regserver** .</span><span class="sxs-lookup"><span data-stu-id="cca14-209">Out-of-process provider was not registered using the **/regserver** switch.</span></span> <span data-ttu-id="cca14-210">Par exemple, **myprog.exe/regserver**.</span><span class="sxs-lookup"><span data-stu-id="cca14-210">For example, **myprog.exe /regserver**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-211"><span id="WBEM_E_INITIALIZATION_FAILURE"></span><span id="wbem_e_initialization_failure"></span>**\_ \_ échec d’initialisation d’E WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-211"><span id="WBEM_E_INITIALIZATION_FAILURE"></span><span id="wbem_e_initialization_failure"></span>**WBEM\_E\_INITIALIZATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-212">2147749908 (0x80041014)</span><span class="sxs-lookup"><span data-stu-id="cca14-212">2147749908 (0x80041014)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-213">Échec de l’initialisation d’un composant, tel qu’un fournisseur, pour des raisons internes.</span><span class="sxs-lookup"><span data-stu-id="cca14-213">Component, such as a provider, failed to initialize for internal reasons.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-214"><span id="WBEM_E_TRANSPORT_FAILURE"></span><span id="wbem_e_transport_failure"></span>**\_échec du \_ transport \_ WBEM**</span><span class="sxs-lookup"><span data-stu-id="cca14-214"><span id="WBEM_E_TRANSPORT_FAILURE"></span><span id="wbem_e_transport_failure"></span>**WBEM\_E\_TRANSPORT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-215">2147749909 (0x80041015)</span><span class="sxs-lookup"><span data-stu-id="cca14-215">2147749909 (0x80041015)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-216">Une erreur réseau qui empêche un fonctionnement normal s’est produite.</span><span class="sxs-lookup"><span data-stu-id="cca14-216">Networking error that prevents normal operation has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-217"><span id="WBEM_E_INVALID_OPERATION"></span><span id="wbem_e_invalid_operation"></span>**\_ \_ opération non valide WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-217"><span id="WBEM_E_INVALID_OPERATION"></span><span id="wbem_e_invalid_operation"></span>**WBEM\_E\_INVALID\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-218">2147749910 (0x80041016)</span><span class="sxs-lookup"><span data-stu-id="cca14-218">2147749910 (0x80041016)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-219">L’opération demandée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="cca14-219">Requested operation is not valid.</span></span> <span data-ttu-id="cca14-220">Cette erreur s'applique généralement aux tentatives non valides de suppression de classes ou de propriétés.</span><span class="sxs-lookup"><span data-stu-id="cca14-220">This error usually applies to invalid attempts to delete classes or properties.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-221"><span id="WBEM_E_INVALID_QUERY"></span><span id="wbem_e_invalid_query"></span>**\_requête E \_ non valide \_ WBEM**</span><span class="sxs-lookup"><span data-stu-id="cca14-221"><span id="WBEM_E_INVALID_QUERY"></span><span id="wbem_e_invalid_query"></span>**WBEM\_E\_INVALID\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-222">2147749911 (0x80041017)</span><span class="sxs-lookup"><span data-stu-id="cca14-222">2147749911 (0x80041017)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-223">La syntaxe de la requête n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="cca14-223">Query was not syntactically valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-224"><span id="WBEM_E_INVALID_QUERY_TYPE"></span><span id="wbem_e_invalid_query_type"></span>**\_type de \_ requête non valide WBEM E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-224"><span id="WBEM_E_INVALID_QUERY_TYPE"></span><span id="wbem_e_invalid_query_type"></span>**WBEM\_E\_INVALID\_QUERY\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-225">2147749912 (0x80041018)</span><span class="sxs-lookup"><span data-stu-id="cca14-225">2147749912 (0x80041018)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-226">Le langage de requête demandé n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="cca14-226">Requested query language is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-227"><span id="WBEM_E_ALREADY_EXISTS"></span><span id="wbem_e_already_exists"></span>**WBEM \_ E \_ \_ existe déjà**</span><span class="sxs-lookup"><span data-stu-id="cca14-227"><span id="WBEM_E_ALREADY_EXISTS"></span><span id="wbem_e_already_exists"></span>**WBEM\_E\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-228">2147749913 (0x80041019)</span><span class="sxs-lookup"><span data-stu-id="cca14-228">2147749913 (0x80041019)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-229">Dans une opération Put, l’indicateur **wbemChangeFlagCreateOnly** a été spécifié, mais l’instance existe déjà.</span><span class="sxs-lookup"><span data-stu-id="cca14-229">In a put operation, the **wbemChangeFlagCreateOnly** flag was specified, but the instance already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-230"><span id="WBEM_E_OVERRIDE_NOT_ALLOWED"></span><span id="wbem_e_override_not_allowed"></span>**le \_ \_ remplacement WBEM E \_ n’est pas \_ autorisé**</span><span class="sxs-lookup"><span data-stu-id="cca14-230"><span id="WBEM_E_OVERRIDE_NOT_ALLOWED"></span><span id="wbem_e_override_not_allowed"></span>**WBEM\_E\_OVERRIDE\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-231">2147749914 (0x8004101A)</span><span class="sxs-lookup"><span data-stu-id="cca14-231">2147749914 (0x8004101A)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-232">Impossible d’effectuer l’opération d’ajout sur ce qualificateur, car l’objet propriétaire n’autorise pas les remplacements.</span><span class="sxs-lookup"><span data-stu-id="cca14-232">Not possible to perform the add operation on this qualifier because the owning object does not permit overrides.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-233"><span id="WBEM_E_PROPAGATED_QUALIFIER"></span><span id="wbem_e_propagated_qualifier"></span>**\_ \_ qualificateur PROPAGÉ E WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-233"><span id="WBEM_E_PROPAGATED_QUALIFIER"></span><span id="wbem_e_propagated_qualifier"></span>**WBEM\_E\_PROPAGATED\_QUALIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-234">2147749915 (0x8004101B)</span><span class="sxs-lookup"><span data-stu-id="cca14-234">2147749915 (0x8004101B)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-235">L’utilisateur a tenté de supprimer un qualificateur qui n’était pas détenu.</span><span class="sxs-lookup"><span data-stu-id="cca14-235">User attempted to delete a qualifier that was not owned.</span></span> <span data-ttu-id="cca14-236">Le qualificateur est hérité d'une classe parente.</span><span class="sxs-lookup"><span data-stu-id="cca14-236">The qualifier was inherited from a parent class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-237"><span id="WBEM_E_PROPAGATED_PROPERTY"></span><span id="wbem_e_propagated_property"></span>**\_ \_ propriété propagé E de \_ WBEM**</span><span class="sxs-lookup"><span data-stu-id="cca14-237"><span id="WBEM_E_PROPAGATED_PROPERTY"></span><span id="wbem_e_propagated_property"></span>**WBEM\_E\_PROPAGATED\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-238">2147749916 (0x8004101C)</span><span class="sxs-lookup"><span data-stu-id="cca14-238">2147749916 (0x8004101C)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-239">L’utilisateur a tenté de supprimer une propriété qui n’était pas propriétaire.</span><span class="sxs-lookup"><span data-stu-id="cca14-239">User attempted to delete a property that was not owned.</span></span> <span data-ttu-id="cca14-240">La propriété est héritée d'une classe parente.</span><span class="sxs-lookup"><span data-stu-id="cca14-240">The property was inherited from a parent class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-241"><span id="WBEM_E_UNEXPECTED"></span><span id="wbem_e_unexpected"></span>**WBEM \_ E \_ inattendu**</span><span class="sxs-lookup"><span data-stu-id="cca14-241"><span id="WBEM_E_UNEXPECTED"></span><span id="wbem_e_unexpected"></span>**WBEM\_E\_UNEXPECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-242">2147749917 (0x8004101D)</span><span class="sxs-lookup"><span data-stu-id="cca14-242">2147749917 (0x8004101D)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-243">Le client a effectué une séquence d’appels inattendue et non conforme, telle que l’appel de [**EndEnumeration**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-endenumeration) avant d’appeler [**BeginEnumeration**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-beginenumeration).</span><span class="sxs-lookup"><span data-stu-id="cca14-243">Client made an unexpected and illegal sequence of calls, such as calling [**EndEnumeration**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-endenumeration) before calling [**BeginEnumeration**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-beginenumeration).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-244"><span id="WBEM_E_ILLEGAL_OPERATION"></span><span id="wbem_e_illegal_operation"></span>**\_ \_ opération non conforme WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-244"><span id="WBEM_E_ILLEGAL_OPERATION"></span><span id="wbem_e_illegal_operation"></span>**WBEM\_E\_ILLEGAL\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-245">2147749918 (0x8004101E)</span><span class="sxs-lookup"><span data-stu-id="cca14-245">2147749918 (0x8004101E)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-246">L’utilisateur a demandé une opération non conforme, telle que la génération d’une classe à partir d’une instance.</span><span class="sxs-lookup"><span data-stu-id="cca14-246">User requested an illegal operation, such as spawning a class from an instance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-247"><span id="WBEM_E_CANNOT_BE_KEY"></span><span id="wbem_e_cannot_be_key"></span>**WBEM \_ E \_ ne peut pas \_ être une \_ clé**</span><span class="sxs-lookup"><span data-stu-id="cca14-247"><span id="WBEM_E_CANNOT_BE_KEY"></span><span id="wbem_e_cannot_be_key"></span>**WBEM\_E\_CANNOT\_BE\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-248">2147749919 (0x8004101F)</span><span class="sxs-lookup"><span data-stu-id="cca14-248">2147749919 (0x8004101F)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-249">Tentative non autorisée de spécifier un qualificateur de clé sur une propriété qui ne peut pas être une clé.</span><span class="sxs-lookup"><span data-stu-id="cca14-249">Illegal attempt to specify a key qualifier on a property that cannot be a key.</span></span> <span data-ttu-id="cca14-250">Les clés sont spécifiées dans la définition de classe pour un objet et ne peuvent pas être modifiées au niveau de l'instance.</span><span class="sxs-lookup"><span data-stu-id="cca14-250">The keys are specified in the class definition for an object and cannot be altered on a per-instance basis.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-251"><span id="WBEM_E_INCOMPLETE_CLASS"></span><span id="wbem_e_incomplete_class"></span>**\_ \_ classe incomplète WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-251"><span id="WBEM_E_INCOMPLETE_CLASS"></span><span id="wbem_e_incomplete_class"></span>**WBEM\_E\_INCOMPLETE\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-252">2147749920 (0x80041020)</span><span class="sxs-lookup"><span data-stu-id="cca14-252">2147749920 (0x80041020)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-253">L’objet actuel n’est pas une définition de classe valide.</span><span class="sxs-lookup"><span data-stu-id="cca14-253">Current object is not a valid class definition.</span></span> <span data-ttu-id="cca14-254">Soit il est incomplet, soit il n’a pas été inscrit auprès de WMI à l’aide de [**SWbemObject. put \_**](swbemobject-put-.md).</span><span class="sxs-lookup"><span data-stu-id="cca14-254">Either it is incomplete or it has not been registered with WMI using [**SWbemObject.Put\_**](swbemobject-put-.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-255"><span id="WBEM_E_INVALID_SYNTAX"></span><span id="wbem_e_invalid_syntax"></span>**\_syntaxe WBEM E \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-255"><span id="WBEM_E_INVALID_SYNTAX"></span><span id="wbem_e_invalid_syntax"></span>**WBEM\_E\_INVALID\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-256">2147749921 (0x80041021)</span><span class="sxs-lookup"><span data-stu-id="cca14-256">2147749921 (0x80041021)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-257">La syntaxe de la requête n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="cca14-257">Query is syntactically not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-258"><span id="WBEM_E_NONDECORATED_OBJECT"></span><span id="wbem_e_nondecorated_object"></span>**\_objet non \_ décoré WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-258"><span id="WBEM_E_NONDECORATED_OBJECT"></span><span id="wbem_e_nondecorated_object"></span>**WBEM\_E\_NONDECORATED\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-259">2147749922 (0x80041022)</span><span class="sxs-lookup"><span data-stu-id="cca14-259">2147749922 (0x80041022)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-260">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="cca14-260">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-261"><span id="WBEM_E_READ_ONLY"></span><span id="wbem_e_read_only"></span>**\_ \_ lecture seule WBEM \_ E**</span><span class="sxs-lookup"><span data-stu-id="cca14-261"><span id="WBEM_E_READ_ONLY"></span><span id="wbem_e_read_only"></span>**WBEM\_E\_READ\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-262">2147749923 (0x80041023)</span><span class="sxs-lookup"><span data-stu-id="cca14-262">2147749923 (0x80041023)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-263">Une tentative de modification d’une propriété en lecture seule a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="cca14-263">An attempt was made to modify a read-only property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-264"><span id="WBEM_E_PROVIDER_NOT_CAPABLE"></span><span id="wbem_e_provider_not_capable"></span>**\_fournisseur E \_ WBEM \_ non \_ conforme**</span><span class="sxs-lookup"><span data-stu-id="cca14-264"><span id="WBEM_E_PROVIDER_NOT_CAPABLE"></span><span id="wbem_e_provider_not_capable"></span>**WBEM\_E\_PROVIDER\_NOT\_CAPABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-265">2147749924 (0x80041024)</span><span class="sxs-lookup"><span data-stu-id="cca14-265">2147749924 (0x80041024)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-266">Le fournisseur ne peut pas effectuer l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="cca14-266">Provider cannot perform the requested operation.</span></span> <span data-ttu-id="cca14-267">Il peut s’agir d’une requête trop complexe, de l’extraction d’une instance, de la création ou de la mise à jour d’une classe, de la suppression d’une classe ou de l’énumération d’une classe.</span><span class="sxs-lookup"><span data-stu-id="cca14-267">This can include a query that is too complex, retrieving an instance, creating or updating a class, deleting a class, or enumerating a class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-268"><span id="WBEM_E_CLASS_HAS_CHILDREN"></span><span id="wbem_e_class_has_children"></span>**la \_ classe WBEM E \_ \_ a des \_ enfants**</span><span class="sxs-lookup"><span data-stu-id="cca14-268"><span id="WBEM_E_CLASS_HAS_CHILDREN"></span><span id="wbem_e_class_has_children"></span>**WBEM\_E\_CLASS\_HAS\_CHILDREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-269">2147749925 (0x80041025)</span><span class="sxs-lookup"><span data-stu-id="cca14-269">2147749925 (0x80041025)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-270">Une tentative a été effectuée pour apporter une modification qui invalide une sous-classe.</span><span class="sxs-lookup"><span data-stu-id="cca14-270">Attempt was made to make a change that invalidates a subclass.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-271"><span id="WBEM_E_CLASS_HAS_INSTANCES"></span><span id="wbem_e_class_has_instances"></span>**la \_ classe WBEM E \_ \_ a des \_ instances**</span><span class="sxs-lookup"><span data-stu-id="cca14-271"><span id="WBEM_E_CLASS_HAS_INSTANCES"></span><span id="wbem_e_class_has_instances"></span>**WBEM\_E\_CLASS\_HAS\_INSTANCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-272">2147749926 (0x80041026)</span><span class="sxs-lookup"><span data-stu-id="cca14-272">2147749926 (0x80041026)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-273">Une tentative de suppression ou de modification d’une classe qui a des instances a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="cca14-273">Attempt was made to delete or modify a class that has instances.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-274"><span id="WBEM_E_QUERY_NOT_IMPLEMENTED"></span><span id="wbem_e_query_not_implemented"></span>**\_requête E \_ WBEM \_ non \_ implémentée**</span><span class="sxs-lookup"><span data-stu-id="cca14-274"><span id="WBEM_E_QUERY_NOT_IMPLEMENTED"></span><span id="wbem_e_query_not_implemented"></span>**WBEM\_E\_QUERY\_NOT\_IMPLEMENTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-275">2147749927 (0x80041027)</span><span class="sxs-lookup"><span data-stu-id="cca14-275">2147749927 (0x80041027)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-276">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="cca14-276">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-277"><span id="WBEM_E_ILLEGAL_NULL"></span><span id="wbem_e_illegal_null"></span>**WBEM \_ E \_ null non conforme \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-277"><span id="WBEM_E_ILLEGAL_NULL"></span><span id="wbem_e_illegal_null"></span>**WBEM\_E\_ILLEGAL\_NULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-278">2147749928 (0x80041028)</span><span class="sxs-lookup"><span data-stu-id="cca14-278">2147749928 (0x80041028)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-279">La valeur Nothing/**null** a été spécifiée pour une propriété qui doit avoir une valeur, telle que celle qui est marquée par un qualificateur [**Key**](key-qualifier.md), [**indexé**](optional-qualifiers.md)ou **not \_ null** .</span><span class="sxs-lookup"><span data-stu-id="cca14-279">Value of Nothing/**NULL** was specified for a property that must have a value, such as one that is marked by a [**Key**](key-qualifier.md), [**Indexed**](optional-qualifiers.md), or **Not\_Null** qualifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-280"><span id="WBEM_E_INVALID_QUALIFIER_TYPE"></span><span id="wbem_e_invalid_qualifier_type"></span>**\_type de \_ qualificateur non valide WBEM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-280"><span id="WBEM_E_INVALID_QUALIFIER_TYPE"></span><span id="wbem_e_invalid_qualifier_type"></span>**WBEM\_E\_INVALID\_QUALIFIER\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-281">2147749929 (0x80041029)</span><span class="sxs-lookup"><span data-stu-id="cca14-281">2147749929 (0x80041029)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-282">Une valeur de variante pour un qualificateur a été fournie qui n’est pas un type de qualificateur légal.</span><span class="sxs-lookup"><span data-stu-id="cca14-282">Variant value for a qualifier was provided that is not a legal qualifier type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-283"><span id="WBEM_E_INVALID_PROPERTY_TYPE"></span><span id="wbem_e_invalid_property_type"></span>**\_type de \_ propriété non valide WBEM E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-283"><span id="WBEM_E_INVALID_PROPERTY_TYPE"></span><span id="wbem_e_invalid_property_type"></span>**WBEM\_E\_INVALID\_PROPERTY\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-284">2147749930 (0x8004102A)</span><span class="sxs-lookup"><span data-stu-id="cca14-284">2147749930 (0x8004102A)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-285">Le type CIM spécifié pour une propriété n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="cca14-285">CIM type specified for a property is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-286"><span id="WBEM_E_VALUE_OUT_OF_RANGE"></span><span id="wbem_e_value_out_of_range"></span>**\_valeur WBEM \_ E \_ hors \_ \_ limites**</span><span class="sxs-lookup"><span data-stu-id="cca14-286"><span id="WBEM_E_VALUE_OUT_OF_RANGE"></span><span id="wbem_e_value_out_of_range"></span>**WBEM\_E\_VALUE\_OUT\_OF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-287">2147749931 (0x8004102B)</span><span class="sxs-lookup"><span data-stu-id="cca14-287">2147749931 (0x8004102B)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-288">La demande a été effectuée avec une valeur hors limites ou n’est pas compatible avec le type.</span><span class="sxs-lookup"><span data-stu-id="cca14-288">Request was made with an out-of-range value or it is incompatible with the type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-289"><span id="WBEM_E_CANNOT_BE_SINGLETON"></span><span id="wbem_e_cannot_be_singleton"></span>**WBEM \_ E \_ ne peut pas \_ être \_ Singleton**</span><span class="sxs-lookup"><span data-stu-id="cca14-289"><span id="WBEM_E_CANNOT_BE_SINGLETON"></span><span id="wbem_e_cannot_be_singleton"></span>**WBEM\_E\_CANNOT\_BE\_SINGLETON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-290">2147749932 (0x8004102C)</span><span class="sxs-lookup"><span data-stu-id="cca14-290">2147749932 (0x8004102C)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-291">Une tentative non conforme a été effectuée pour créer un singleton de classe, par exemple lorsque la classe est dérivée d’une classe non Singleton.</span><span class="sxs-lookup"><span data-stu-id="cca14-291">Illegal attempt was made to make a class singleton, such as when the class is derived from a non-singleton class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-292"><span id="WBEM_E_INVALID_CIM_TYPE"></span><span id="wbem_e_invalid_cim_type"></span>**WBEM \_ E \_ \_ type CIM non valide \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-292"><span id="WBEM_E_INVALID_CIM_TYPE"></span><span id="wbem_e_invalid_cim_type"></span>**WBEM\_E\_INVALID\_CIM\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-293">2147749933 (0x8004102D)</span><span class="sxs-lookup"><span data-stu-id="cca14-293">2147749933 (0x8004102D)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-294">Le type CIM spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="cca14-294">CIM type specified is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-295"><span id="WBEM_E_INVALID_METHOD"></span><span id="wbem_e_invalid_method"></span>**WBEM \_ E \_ , \_ méthode non valide**</span><span class="sxs-lookup"><span data-stu-id="cca14-295"><span id="WBEM_E_INVALID_METHOD"></span><span id="wbem_e_invalid_method"></span>**WBEM\_E\_INVALID\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-296">2147749934 (0x8004102E)</span><span class="sxs-lookup"><span data-stu-id="cca14-296">2147749934 (0x8004102E)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-297">La méthode demandée n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="cca14-297">Requested method is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-298"><span id="WBEM_E_INVALID_METHOD_PARAMETERS"></span><span id="wbem_e_invalid_method_parameters"></span>**\_paramètres de méthode WBEM E \_ non valides \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-298"><span id="WBEM_E_INVALID_METHOD_PARAMETERS"></span><span id="wbem_e_invalid_method_parameters"></span>**WBEM\_E\_INVALID\_METHOD\_PARAMETERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-299">2147749935 (0x8004102F)</span><span class="sxs-lookup"><span data-stu-id="cca14-299">2147749935 (0x8004102F)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-300">Les paramètres fournis pour la méthode ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="cca14-300">Parameters provided for the method are not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-301"><span id="WBEM_E_SYSTEM_PROPERTY"></span><span id="wbem_e_system_property"></span>**\_ \_ propriété système WBEM \_ E**</span><span class="sxs-lookup"><span data-stu-id="cca14-301"><span id="WBEM_E_SYSTEM_PROPERTY"></span><span id="wbem_e_system_property"></span>**WBEM\_E\_SYSTEM\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-302">2147749936 (0x80041030)</span><span class="sxs-lookup"><span data-stu-id="cca14-302">2147749936 (0x80041030)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-303">Une tentative a été effectuée pour obtenir des qualificateurs sur une propriété système.</span><span class="sxs-lookup"><span data-stu-id="cca14-303">There was an attempt to get qualifiers on a system property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-304"><span id="WBEM_E_INVALID_PROPERTY"></span><span id="wbem_e_invalid_property"></span>**\_ \_ propriété non valide \_ WBEM**</span><span class="sxs-lookup"><span data-stu-id="cca14-304"><span id="WBEM_E_INVALID_PROPERTY"></span><span id="wbem_e_invalid_property"></span>**WBEM\_E\_INVALID\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-305">2147749937 (0x80041031)</span><span class="sxs-lookup"><span data-stu-id="cca14-305">2147749937 (0x80041031)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-306">Le type de propriété n’est pas reconnu.</span><span class="sxs-lookup"><span data-stu-id="cca14-306">Property type is not recognized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-307"><span id="WBEM_E_CALL_CANCELLED"></span><span id="wbem_e_call_cancelled"></span>**\_appel d’E WBEM \_ \_ annulé**</span><span class="sxs-lookup"><span data-stu-id="cca14-307"><span id="WBEM_E_CALL_CANCELLED"></span><span id="wbem_e_call_cancelled"></span>**WBEM\_E\_CALL\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-308">2147749938 (0x80041032)</span><span class="sxs-lookup"><span data-stu-id="cca14-308">2147749938 (0x80041032)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-309">Le processus asynchrone a été annulé en interne ou par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cca14-309">Asynchronous process has been canceled internally or by the user.</span></span> <span data-ttu-id="cca14-310">Notez qu’en raison de la durée et de la nature de l’opération asynchrone, l’opération n’a peut-être pas été réellement annulée.</span><span class="sxs-lookup"><span data-stu-id="cca14-310">Note that due to the timing and nature of the asynchronous operation, the operation may not have been truly canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-311"><span id="WBEM_E_SHUTTING_DOWN"></span><span id="wbem_e_shutting_down"></span>**fermeture de WBEM \_ E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-311"><span id="WBEM_E_SHUTTING_DOWN"></span><span id="wbem_e_shutting_down"></span>**WBEM\_E\_SHUTTING\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-312">2147749939 (0x80041033)</span><span class="sxs-lookup"><span data-stu-id="cca14-312">2147749939 (0x80041033)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-313">L’utilisateur a demandé une opération alors que WMI est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="cca14-313">User has requested an operation while WMI is in the process of shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-314"><span id="WBEM_E_PROPAGATED_METHOD"></span><span id="wbem_e_propagated_method"></span>**\_ \_ méthode propagée d’E WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-314"><span id="WBEM_E_PROPAGATED_METHOD"></span><span id="wbem_e_propagated_method"></span>**WBEM\_E\_PROPAGATED\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-315">2147749940 (0x80041034)</span><span class="sxs-lookup"><span data-stu-id="cca14-315">2147749940 (0x80041034)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-316">Une tentative de réutilisation d’un nom de méthode existant à partir d’une classe parente a été effectuée et les signatures ne correspondent pas.</span><span class="sxs-lookup"><span data-stu-id="cca14-316">Attempt was made to reuse an existing method name from a parent class and the signatures do not match.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-317"><span id="WBEM_E_UNSUPPORTED_PARAMETER"></span><span id="wbem_e_unsupported_parameter"></span>**\_ \_ paramètre non pris en charge par WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-317"><span id="WBEM_E_UNSUPPORTED_PARAMETER"></span><span id="wbem_e_unsupported_parameter"></span>**WBEM\_E\_UNSUPPORTED\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-318">2147749941 (0x80041035)</span><span class="sxs-lookup"><span data-stu-id="cca14-318">2147749941 (0x80041035)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-319">Une ou plusieurs valeurs de paramètre, telles qu'un texte de requête, sont trop complexes ou non prises en charge.</span><span class="sxs-lookup"><span data-stu-id="cca14-319">One or more parameter values, such as a query text, is too complex or unsupported.</span></span> <span data-ttu-id="cca14-320">WMI est donc invité à réessayer l’opération avec des paramètres plus simples.</span><span class="sxs-lookup"><span data-stu-id="cca14-320">WMI is therefore requested to retry the operation with simpler parameters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-321"><span id="WBEM_E_MISSING_PARAMETER_ID"></span><span id="wbem_e_missing_parameter_id"></span>**\_ID de \_ \_ paramètre manquant \_ dans WBEM E**</span><span class="sxs-lookup"><span data-stu-id="cca14-321"><span id="WBEM_E_MISSING_PARAMETER_ID"></span><span id="wbem_e_missing_parameter_id"></span>**WBEM\_E\_MISSING\_PARAMETER\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-322">2147749942 (0x80041036)</span><span class="sxs-lookup"><span data-stu-id="cca14-322">2147749942 (0x80041036)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-323">Le paramètre était manquant dans l’appel de la méthode.</span><span class="sxs-lookup"><span data-stu-id="cca14-323">Parameter was missing from the method call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-324"><span id="WBEM_E_INVALID_PARAMETER_ID"></span><span id="wbem_e_invalid_parameter_id"></span>**\_ID de paramètre WBEM E \_ non valide \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-324"><span id="WBEM_E_INVALID_PARAMETER_ID"></span><span id="wbem_e_invalid_parameter_id"></span>**WBEM\_E\_INVALID\_PARAMETER\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-325">2147749943 (0x80041037)</span><span class="sxs-lookup"><span data-stu-id="cca14-325">2147749943 (0x80041037)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-326">Le paramètre de la méthode a un qualificateur d' [**ID**](standard-wmi-qualifiers.md) qui n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="cca14-326">Method parameter has an [**ID**](standard-wmi-qualifiers.md) qualifier that is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-327"><span id="WBEM_E_NONCONSECUTIVE_PARAMETER_IDS"></span><span id="wbem_e_nonconsecutive_parameter_ids"></span>**\_ID de paramètres WBEM E \_ inconsécutifs \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-327"><span id="WBEM_E_NONCONSECUTIVE_PARAMETER_IDS"></span><span id="wbem_e_nonconsecutive_parameter_ids"></span>**WBEM\_E\_NONCONSECUTIVE\_PARAMETER\_IDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-328">2147749944 (0x80041038)</span><span class="sxs-lookup"><span data-stu-id="cca14-328">2147749944 (0x80041038)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-329">Un ou plusieurs des paramètres de méthode ont des qualificateurs d' [**ID**](standard-wmi-qualifiers.md) qui sont hors séquence.</span><span class="sxs-lookup"><span data-stu-id="cca14-329">One or more of the method parameters have [**ID**](standard-wmi-qualifiers.md) qualifiers that are out of sequence.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-330"><span id="WBEM_E_PARAMETER_ID_ON_RETVAL"></span><span id="wbem_e_parameter_id_on_retval"></span>**\_ \_ ID de paramètre WBEM E \_ \_ sur \_ retVal**</span><span class="sxs-lookup"><span data-stu-id="cca14-330"><span id="WBEM_E_PARAMETER_ID_ON_RETVAL"></span><span id="wbem_e_parameter_id_on_retval"></span>**WBEM\_E\_PARAMETER\_ID\_ON\_RETVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-331">2147749945 (0x80041039)</span><span class="sxs-lookup"><span data-stu-id="cca14-331">2147749945 (0x80041039)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-332">La valeur de retour d’une méthode a un qualificateur d' [**ID**](standard-wmi-qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="cca14-332">Return value for a method has an [**ID**](standard-wmi-qualifiers.md) qualifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-333"><span id="WBEM_E_INVALID_OBJECT_PATH"></span><span id="wbem_e_invalid_object_path"></span>**WBEM \_ E \_ \_ chemin d’objet non valide \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-333"><span id="WBEM_E_INVALID_OBJECT_PATH"></span><span id="wbem_e_invalid_object_path"></span>**WBEM\_E\_INVALID\_OBJECT\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-334">2147749946 (0x8004103A)</span><span class="sxs-lookup"><span data-stu-id="cca14-334">2147749946 (0x8004103A)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-335">Le chemin d’accès à l’objet spécifié n’était pas valide.</span><span class="sxs-lookup"><span data-stu-id="cca14-335">Specified object path was not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-336"><span id="WBEM_E_OUT_OF_DISK_SPACE"></span><span id="wbem_e_out_of_disk_space"></span>**\_ \_ \_ \_ espace disque insuffisant pour \_ WBEM**</span><span class="sxs-lookup"><span data-stu-id="cca14-336"><span id="WBEM_E_OUT_OF_DISK_SPACE"></span><span id="wbem_e_out_of_disk_space"></span>**WBEM\_E\_OUT\_OF\_DISK\_SPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-337">2147749947 (0x8004103B)</span><span class="sxs-lookup"><span data-stu-id="cca14-337">2147749947 (0x8004103B)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-338">L’espace disque est insuffisant ou la limite de 4 Go sur le référentiel WMI (espace de stockage CIM) est atteinte.</span><span class="sxs-lookup"><span data-stu-id="cca14-338">Disk is out of space or the 4 GB limit on WMI repository (CIM repository) size is reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-339"><span id="WBEM_E_BUFFER_TOO_SMALL"></span><span id="wbem_e_buffer_too_small"></span>**\_ \_ mémoire tampon WBEM E \_ trop \_ petite**</span><span class="sxs-lookup"><span data-stu-id="cca14-339"><span id="WBEM_E_BUFFER_TOO_SMALL"></span><span id="wbem_e_buffer_too_small"></span>**WBEM\_E\_BUFFER\_TOO\_SMALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-340">2147749948 (0x8004103C)</span><span class="sxs-lookup"><span data-stu-id="cca14-340">2147749948 (0x8004103C)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-341">La mémoire tampon fournie est trop petite pour contenir tous les objets de l’énumérateur ou pour lire une propriété de type chaîne.</span><span class="sxs-lookup"><span data-stu-id="cca14-341">Supplied buffer was too small to hold all of the objects in the enumerator or to read a string property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-342"><span id="WBEM_E_UNSUPPORTED_PUT_EXTENSION"></span><span id="wbem_e_unsupported_put_extension"></span>**\_extension d' \_ put non prise en charge par WBEM E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-342"><span id="WBEM_E_UNSUPPORTED_PUT_EXTENSION"></span><span id="wbem_e_unsupported_put_extension"></span>**WBEM\_E\_UNSUPPORTED\_PUT\_EXTENSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-343">2147749949 (0x8004103D)</span><span class="sxs-lookup"><span data-stu-id="cca14-343">2147749949 (0x8004103D)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-344">Le fournisseur ne prend pas en charge l’opération put demandée.</span><span class="sxs-lookup"><span data-stu-id="cca14-344">Provider does not support the requested put operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-345"><span id="WBEM_E_UNKNOWN_OBJECT_TYPE"></span><span id="wbem_e_unknown_object_type"></span>**\_type d' \_ \_ objet inconnu WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-345"><span id="WBEM_E_UNKNOWN_OBJECT_TYPE"></span><span id="wbem_e_unknown_object_type"></span>**WBEM\_E\_UNKNOWN\_OBJECT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-346">2147749950 (0x8004103E)</span><span class="sxs-lookup"><span data-stu-id="cca14-346">2147749950 (0x8004103E)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-347">Un objet avec un type ou une version incorrect a été rencontré pendant le marshaling.</span><span class="sxs-lookup"><span data-stu-id="cca14-347">Object with an incorrect type or version was encountered during marshaling.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-348"><span id="WBEM_E_UNKNOWN_PACKET_TYPE"></span><span id="wbem_e_unknown_packet_type"></span>**\_type de \_ \_ paquet inconnu \_ WBEM**</span><span class="sxs-lookup"><span data-stu-id="cca14-348"><span id="WBEM_E_UNKNOWN_PACKET_TYPE"></span><span id="wbem_e_unknown_packet_type"></span>**WBEM\_E\_UNKNOWN\_PACKET\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-349">2147749951 (0x8004103F)</span><span class="sxs-lookup"><span data-stu-id="cca14-349">2147749951 (0x8004103F)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-350">Un paquet avec un type ou une version incorrect a été rencontré pendant le marshaling.</span><span class="sxs-lookup"><span data-stu-id="cca14-350">Packet with an incorrect type or version was encountered during marshaling.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-351"><span id="WBEM_E_MARSHAL_VERSION_MISMATCH"></span><span id="wbem_e_marshal_version_mismatch"></span>**incompatibilité de \_ \_ version de MARSHALing WBEM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-351"><span id="WBEM_E_MARSHAL_VERSION_MISMATCH"></span><span id="wbem_e_marshal_version_mismatch"></span>**WBEM\_E\_MARSHAL\_VERSION\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-352">2147749952 (0x80041040)</span><span class="sxs-lookup"><span data-stu-id="cca14-352">2147749952 (0x80041040)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-353">La version du paquet n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="cca14-353">Packet has an unsupported version.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-354"><span id="WBEM_E_MARSHAL_INVALID_SIGNATURE"></span><span id="wbem_e_marshal_invalid_signature"></span>**\_ \_ \_ signature non valide du \_ Marshal WBEM**</span><span class="sxs-lookup"><span data-stu-id="cca14-354"><span id="WBEM_E_MARSHAL_INVALID_SIGNATURE"></span><span id="wbem_e_marshal_invalid_signature"></span>**WBEM\_E\_MARSHAL\_INVALID\_SIGNATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-355">2147749953 (0x80041041)</span><span class="sxs-lookup"><span data-stu-id="cca14-355">2147749953 (0x80041041)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-356">Le paquet semble endommagé.</span><span class="sxs-lookup"><span data-stu-id="cca14-356">Packet appears to be corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-357"><span id="WBEM_E_INVALID_QUALIFIER"></span><span id="wbem_e_invalid_qualifier"></span>**\_qualificateur E \_ non valide \_ WBEM**</span><span class="sxs-lookup"><span data-stu-id="cca14-357"><span id="WBEM_E_INVALID_QUALIFIER"></span><span id="wbem_e_invalid_qualifier"></span>**WBEM\_E\_INVALID\_QUALIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-358">2147749954 (0x80041042)</span><span class="sxs-lookup"><span data-stu-id="cca14-358">2147749954 (0x80041042)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-359">Tentative d’incompatibilité de qualificateurs, par exemple en \[ plaçant \] une clé sur un objet au lieu d’une propriété.</span><span class="sxs-lookup"><span data-stu-id="cca14-359">Attempt was made to mismatch qualifiers, such as putting \[key\] on an object instead of a property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-360"><span id="WBEM_E_INVALID_DUPLICATE_PARAMETER"></span><span id="wbem_e_invalid_duplicate_parameter"></span>**\_ \_ \_ paramètre en double non valide pour WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-360"><span id="WBEM_E_INVALID_DUPLICATE_PARAMETER"></span><span id="wbem_e_invalid_duplicate_parameter"></span>**WBEM\_E\_INVALID\_DUPLICATE\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-361">2147749955 (0x80041043)</span><span class="sxs-lookup"><span data-stu-id="cca14-361">2147749955 (0x80041043)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-362">Un paramètre en double a été déclaré dans une méthode CIM.</span><span class="sxs-lookup"><span data-stu-id="cca14-362">Duplicate parameter was declared in a CIM method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-363"><span id="WBEM_E_TOO_MUCH_DATA"></span><span id="wbem_e_too_much_data"></span>**WBEM \_ E \_ de \_ données trop nombreuses \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-363"><span id="WBEM_E_TOO_MUCH_DATA"></span><span id="wbem_e_too_much_data"></span>**WBEM\_E\_TOO\_MUCH\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-364">2147749956 (0x80041044)</span><span class="sxs-lookup"><span data-stu-id="cca14-364">2147749956 (0x80041044)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-365">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="cca14-365">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-366"><span id="WBEM_E_SERVER_TOO_BUSY"></span><span id="wbem_e_server_too_busy"></span>**\_serveur WBEM \_ E \_ encombré \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-366"><span id="WBEM_E_SERVER_TOO_BUSY"></span><span id="wbem_e_server_too_busy"></span>**WBEM\_E\_SERVER\_TOO\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-367">2147749957 (0x80041045)</span><span class="sxs-lookup"><span data-stu-id="cca14-367">2147749957 (0x80041045)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-368">L’appel à [**IWbemObjectSink :: indique**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) a échoué.</span><span class="sxs-lookup"><span data-stu-id="cca14-368">Call to [**IWbemObjectSink::Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) has failed.</span></span> <span data-ttu-id="cca14-369">Le fournisseur peut réactiver l’événement.</span><span class="sxs-lookup"><span data-stu-id="cca14-369">The provider can refire the event.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-370"><span id="WBEM_E_INVALID_FLAVOR"></span><span id="wbem_e_invalid_flavor"></span>**\_version WBEM E \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-370"><span id="WBEM_E_INVALID_FLAVOR"></span><span id="wbem_e_invalid_flavor"></span>**WBEM\_E\_INVALID\_FLAVOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-371">2147749958 (0x80041046)</span><span class="sxs-lookup"><span data-stu-id="cca14-371">2147749958 (0x80041046)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-372">La version de qualificateur spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="cca14-372">Specified qualifier flavor was not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-373"><span id="WBEM_E_CIRCULAR_REFERENCE"></span><span id="wbem_e_circular_reference"></span>**\_ \_ référence circulaire WBEM \_ E**</span><span class="sxs-lookup"><span data-stu-id="cca14-373"><span id="WBEM_E_CIRCULAR_REFERENCE"></span><span id="wbem_e_circular_reference"></span>**WBEM\_E\_CIRCULAR\_REFERENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-374">2147749959 (0x80041047)</span><span class="sxs-lookup"><span data-stu-id="cca14-374">2147749959 (0x80041047)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-375">Une tentative de création d’une référence circulaire (par exemple, la dérivation d’une classe à partir d’elle-même) a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="cca14-375">Attempt was made to create a reference that is circular (for example, deriving a class from itself).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-376"><span id="WBEM_E_UNSUPPORTED_CLASS_UPDATE"></span><span id="wbem_e_unsupported_class_update"></span>**\_ \_ \_ mise à jour de classe non prise en charge par WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-376"><span id="WBEM_E_UNSUPPORTED_CLASS_UPDATE"></span><span id="wbem_e_unsupported_class_update"></span>**WBEM\_E\_UNSUPPORTED\_CLASS\_UPDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-377">2147749960 (0x80041048)</span><span class="sxs-lookup"><span data-stu-id="cca14-377">2147749960 (0x80041048)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-378">La classe spécifiée n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="cca14-378">Specified class is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-379"><span id="WBEM_E_CANNOT_CHANGE_KEY_INHERITANCE"></span><span id="wbem_e_cannot_change_key_inheritance"></span>**WBEM \_ E \_ ne peut pas \_ modifier \_ \_ l’héritage de la clé**</span><span class="sxs-lookup"><span data-stu-id="cca14-379"><span id="WBEM_E_CANNOT_CHANGE_KEY_INHERITANCE"></span><span id="wbem_e_cannot_change_key_inheritance"></span>**WBEM\_E\_CANNOT\_CHANGE\_KEY\_INHERITANCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-380">2147749961 (0x80041049)</span><span class="sxs-lookup"><span data-stu-id="cca14-380">2147749961 (0x80041049)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-381">Tentative de modification d’une clé lorsque des instances ou des sous-classes utilisent déjà la clé.</span><span class="sxs-lookup"><span data-stu-id="cca14-381">Attempt was made to change a key when instances or subclasses are already using the key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-382"><span id="WBEM_E_CANNOT_CHANGE_INDEX_INHERITANCE"></span><span id="wbem_e_cannot_change_index_inheritance"></span>**WBEM \_ E \_ ne peut pas \_ modifier \_ \_ l’héritage d’index**</span><span class="sxs-lookup"><span data-stu-id="cca14-382"><span id="WBEM_E_CANNOT_CHANGE_INDEX_INHERITANCE"></span><span id="wbem_e_cannot_change_index_inheritance"></span>**WBEM\_E\_CANNOT\_CHANGE\_INDEX\_INHERITANCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-383">2147749968 (0x80041050)</span><span class="sxs-lookup"><span data-stu-id="cca14-383">2147749968 (0x80041050)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-384">Une tentative a été effectuée pour modifier un index lorsque des instances ou des sous-classes utilisent déjà l’index.</span><span class="sxs-lookup"><span data-stu-id="cca14-384">An attempt was made to change an index when instances or subclasses are already using the index.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-385"><span id="WBEM_E_TOO_MANY_PROPERTIES"></span><span id="wbem_e_too_many_properties"></span>**WBEM \_ E \_ trop \_ de \_ Propriétés**</span><span class="sxs-lookup"><span data-stu-id="cca14-385"><span id="WBEM_E_TOO_MANY_PROPERTIES"></span><span id="wbem_e_too_many_properties"></span>**WBEM\_E\_TOO\_MANY\_PROPERTIES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-386">2147749969 (0x80041051)</span><span class="sxs-lookup"><span data-stu-id="cca14-386">2147749969 (0x80041051)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-387">Une tentative de création de propriétés supplémentaires que la version actuelle de la classe prend en charge a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="cca14-387">Attempt was made to create more properties than the current version of the class supports.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-388"><span id="WBEM_E_UPDATE_TYPE_MISMATCH"></span><span id="wbem_e_update_type_mismatch"></span>**incompatibilité de \_ \_ type de mise à jour WBEM E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-388"><span id="WBEM_E_UPDATE_TYPE_MISMATCH"></span><span id="wbem_e_update_type_mismatch"></span>**WBEM\_E\_UPDATE\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-389">2147749970 (0x80041052)</span><span class="sxs-lookup"><span data-stu-id="cca14-389">2147749970 (0x80041052)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-390">La propriété a été redéfinie avec un type en conflit dans une classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="cca14-390">Property was redefined with a conflicting type in a derived class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-391"><span id="WBEM_E_UPDATE_OVERRIDE_NOT_ALLOWED"></span><span id="wbem_e_update_override_not_allowed"></span>**REMPLACEMENT de la \_ \_ mise à jour WBEM E \_ \_ non \_ autorisé**</span><span class="sxs-lookup"><span data-stu-id="cca14-391"><span id="WBEM_E_UPDATE_OVERRIDE_NOT_ALLOWED"></span><span id="wbem_e_update_override_not_allowed"></span>**WBEM\_E\_UPDATE\_OVERRIDE\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-392">2147749971 (0x80041053)</span><span class="sxs-lookup"><span data-stu-id="cca14-392">2147749971 (0x80041053)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-393">Une tentative a été effectuée dans une classe dérivée pour substituer un qualificateur qui ne peut pas être substitué.</span><span class="sxs-lookup"><span data-stu-id="cca14-393">Attempt was made in a derived class to override a qualifier that cannot be overridden.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-394"><span id="WBEM_E_UPDATE_PROPAGATED_METHOD"></span><span id="wbem_e_update_propagated_method"></span>**\_méthode de \_ mise à jour \_ propagée WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-394"><span id="WBEM_E_UPDATE_PROPAGATED_METHOD"></span><span id="wbem_e_update_propagated_method"></span>**WBEM\_E\_UPDATE\_PROPAGATED\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-395">2147749972 (0x80041054)</span><span class="sxs-lookup"><span data-stu-id="cca14-395">2147749972 (0x80041054)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-396">La méthode a été déclarée à nouveau avec une signature en conflit dans une classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="cca14-396">Method was re-declared with a conflicting signature in a derived class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-397"><span id="WBEM_E_METHOD_NOT_IMPLEMENTED"></span><span id="wbem_e_method_not_implemented"></span>**\_méthode WBEM \_ E \_ non \_ implémentée**</span><span class="sxs-lookup"><span data-stu-id="cca14-397"><span id="WBEM_E_METHOD_NOT_IMPLEMENTED"></span><span id="wbem_e_method_not_implemented"></span>**WBEM\_E\_METHOD\_NOT\_IMPLEMENTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-398">2147749973 (0x80041055)</span><span class="sxs-lookup"><span data-stu-id="cca14-398">2147749973 (0x80041055)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-399">Une tentative d’exécution d’une méthode non marquée avec \[ implémentée \] dans une classe pertinente a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="cca14-399">Attempt was made to execute a method not marked with \[implemented\] in any relevant class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-400"><span id="WBEM_E_METHOD_DISABLED"></span><span id="wbem_e_method_disabled"></span>**\_méthode WBEM \_ E \_ désactivée**</span><span class="sxs-lookup"><span data-stu-id="cca14-400"><span id="WBEM_E_METHOD_DISABLED"></span><span id="wbem_e_method_disabled"></span>**WBEM\_E\_METHOD\_DISABLED**</span></span>
</dt> <dd> <dl> <span data-ttu-id="cca14-401"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="cca14-401"><dt>


</dt> <dt></span></span>



<span data-ttu-id="cca14-402">Une tentative d’exécution d’une méthode marquée avec l’option \[ Disabled a été effectuée \] .</span><span class="sxs-lookup"><span data-stu-id="cca14-402">Attempt was made to execute a method marked with \[disabled\].</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-403"><span id="WBEM_E_REFRESHER_BUSY"></span><span id="wbem_e_refresher_busy"></span>**\_actualisation E WBEM \_ \_ occupée**</span><span class="sxs-lookup"><span data-stu-id="cca14-403"><span id="WBEM_E_REFRESHER_BUSY"></span><span id="wbem_e_refresher_busy"></span>**WBEM\_E\_REFRESHER\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-404">2147749975 (0x80041057)</span><span class="sxs-lookup"><span data-stu-id="cca14-404">2147749975 (0x80041057)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-405">L’actualisateur est occupé par une autre opération.</span><span class="sxs-lookup"><span data-stu-id="cca14-405">Refresher is busy with another operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-406"><span id="WBEM_E_UNPARSABLE_QUERY"></span><span id="wbem_e_unparsable_query"></span>**\_requête E \_ unanalysable \_ WBEM**</span><span class="sxs-lookup"><span data-stu-id="cca14-406"><span id="WBEM_E_UNPARSABLE_QUERY"></span><span id="wbem_e_unparsable_query"></span>**WBEM\_E\_UNPARSABLE\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-407">2147749976 (0x80041058)</span><span class="sxs-lookup"><span data-stu-id="cca14-407">2147749976 (0x80041058)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-408">La syntaxe de la requête de filtrage n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="cca14-408">Filtering query is syntactically not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-409"><span id="WBEM_E_NOT_EVENT_CLASS"></span><span id="wbem_e_not_event_class"></span>**WBEM \_ E \_ not \_ , \_ classe d’événements**</span><span class="sxs-lookup"><span data-stu-id="cca14-409"><span id="WBEM_E_NOT_EVENT_CLASS"></span><span id="wbem_e_not_event_class"></span>**WBEM\_E\_NOT\_EVENT\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-410">2147749977 (0x80041059)</span><span class="sxs-lookup"><span data-stu-id="cca14-410">2147749977 (0x80041059)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-411">La clause from d’une requête de filtrage fait référence à une classe qui n’est pas une classe d’événements (non dérivée d' [**\_ \_ Event**](--event.md)).</span><span class="sxs-lookup"><span data-stu-id="cca14-411">The FROM clause of a filtering query references a class that is not an event class (not derived from [**\_\_Event**](--event.md)).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-412"><span id="WBEM_E_MISSING_GROUP_WITHIN"></span><span id="wbem_e_missing_group_within"></span>**\_ \_ \_ groupe \_ de**</span><span class="sxs-lookup"><span data-stu-id="cca14-412"><span id="WBEM_E_MISSING_GROUP_WITHIN"></span><span id="wbem_e_missing_group_within"></span>**WBEM\_E\_MISSING\_GROUP\_WITHIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-413">2147749978 (0x8004105A)</span><span class="sxs-lookup"><span data-stu-id="cca14-413">2147749978 (0x8004105A)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-414">Une clause GROUP BY a été utilisée sans la clause GROUP WITHIN correspondante.</span><span class="sxs-lookup"><span data-stu-id="cca14-414">A GROUP BY clause was used without the corresponding GROUP WITHIN clause.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-415"><span id="WBEM_E_MISSING_AGGREGATION_LIST"></span><span id="wbem_e_missing_aggregation_list"></span>**\_liste d' \_ agrégation absente de WBEM E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-415"><span id="WBEM_E_MISSING_AGGREGATION_LIST"></span><span id="wbem_e_missing_aggregation_list"></span>**WBEM\_E\_MISSING\_AGGREGATION\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-416">2147749979 (0x8004105B)</span><span class="sxs-lookup"><span data-stu-id="cca14-416">2147749979 (0x8004105B)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-417">Une clause GROUP BY a été utilisée.</span><span class="sxs-lookup"><span data-stu-id="cca14-417">A GROUP BY clause was used.</span></span> <span data-ttu-id="cca14-418">L'agrégation sur toutes les propriétés n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="cca14-418">Aggregation on all properties is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-419"><span id="WBEM_E_PROPERTY_NOT_AN_OBJECT"></span><span id="wbem_e_property_not_an_object"></span>**la \_ propriété WBEM E \_ \_ n’est pas \_ un \_ objet**</span><span class="sxs-lookup"><span data-stu-id="cca14-419"><span id="WBEM_E_PROPERTY_NOT_AN_OBJECT"></span><span id="wbem_e_property_not_an_object"></span>**WBEM\_E\_PROPERTY\_NOT\_AN\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-420">2147749980 (0x8004105C)</span><span class="sxs-lookup"><span data-stu-id="cca14-420">2147749980 (0x8004105C)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-421">La notation à points a été utilisée sur une propriété qui n'est pas un objet incorporé.</span><span class="sxs-lookup"><span data-stu-id="cca14-421">Dot notation was used on a property that is not an embedded object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-422"><span id="WBEM_E_AGGREGATING_BY_OBJECT"></span><span id="wbem_e_aggregating_by_object"></span>**\_ \_ \_ l’agrégation par l' \_ objet WBEM E**</span><span class="sxs-lookup"><span data-stu-id="cca14-422"><span id="WBEM_E_AGGREGATING_BY_OBJECT"></span><span id="wbem_e_aggregating_by_object"></span>**WBEM\_E\_AGGREGATING\_BY\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-423">2147749981 (0x8004105D)</span><span class="sxs-lookup"><span data-stu-id="cca14-423">2147749981 (0x8004105D)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-424">Une clause GROUP BY référence une propriété qui est un objet incorporé sans utiliser de notation à points.</span><span class="sxs-lookup"><span data-stu-id="cca14-424">A GROUP BY clause references a property that is an embedded object without using dot notation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-425"><span id="WBEM_E_UNINTERPRETABLE_PROVIDER_QUERY"></span><span id="wbem_e_uninterpretable_provider_query"></span>**\_requête de \_ fournisseur ininterprétable WBEM E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-425"><span id="WBEM_E_UNINTERPRETABLE_PROVIDER_QUERY"></span><span id="wbem_e_uninterpretable_provider_query"></span>**WBEM\_E\_UNINTERPRETABLE\_PROVIDER\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-426">2147749983 (0x8004105F)</span><span class="sxs-lookup"><span data-stu-id="cca14-426">2147749983 (0x8004105F)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-427">La requête d’inscription du fournisseur d’événements ([**\_ \_ EventProviderRegistration**](--eventproviderregistration.md)) n’a pas spécifié les classes pour lesquelles des événements ont été fournis.</span><span class="sxs-lookup"><span data-stu-id="cca14-427">Event provider registration query ([**\_\_EventProviderRegistration**](--eventproviderregistration.md)) did not specify the classes for which events were provided.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-428"><span id="WBEM_E_BACKUP_RESTORE_WINMGMT_RUNNING"></span><span id="wbem_e_backup_restore_winmgmt_running"></span>**restauration de la \_ sauvegarde WBEM E \_ \_ \_ winmgmt \_ en cours d’exécution**</span><span class="sxs-lookup"><span data-stu-id="cca14-428"><span id="WBEM_E_BACKUP_RESTORE_WINMGMT_RUNNING"></span><span id="wbem_e_backup_restore_winmgmt_running"></span>**WBEM\_E\_BACKUP\_RESTORE\_WINMGMT\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-429">2147749984 (0x80041060)</span><span class="sxs-lookup"><span data-stu-id="cca14-429">2147749984 (0x80041060)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-430">La demande a été faite pour sauvegarder ou restaurer le référentiel pendant qu’il était utilisé par WinMgmt.exe ou par le processus SVCHOST qui contient le service WMI.</span><span class="sxs-lookup"><span data-stu-id="cca14-430">Request was made to back up or restore the repository while it was in use by WinMgmt.exe, or by the SVCHOST process that contains the WMI service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-431"><span id="WBEM_E_QUEUE_OVERFLOW"></span><span id="wbem_e_queue_overflow"></span>**dépassement de la \_ \_ file d’attente WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-431"><span id="WBEM_E_QUEUE_OVERFLOW"></span><span id="wbem_e_queue_overflow"></span>**WBEM\_E\_QUEUE\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-432">2147749985 (0x80041061)</span><span class="sxs-lookup"><span data-stu-id="cca14-432">2147749985 (0x80041061)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-433">Dépassement de la capacité de la file d’attente de remise asynchrone du consommateur d’événements trop lent.</span><span class="sxs-lookup"><span data-stu-id="cca14-433">Asynchronous delivery queue overflowed from the event consumer being too slow.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-434"><span id="WBEM_E_PRIVILEGE_NOT_HELD"></span><span id="wbem_e_privilege_not_held"></span>**\_privilège WBEM \_ E \_ non \_ détenu**</span><span class="sxs-lookup"><span data-stu-id="cca14-434"><span id="WBEM_E_PRIVILEGE_NOT_HELD"></span><span id="wbem_e_privilege_not_held"></span>**WBEM\_E\_PRIVILEGE\_NOT\_HELD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-435">2147749986 (0x80041062)</span><span class="sxs-lookup"><span data-stu-id="cca14-435">2147749986 (0x80041062)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-436">L’opération a échoué car le client n’a pas le privilège de sécurité nécessaire.</span><span class="sxs-lookup"><span data-stu-id="cca14-436">Operation failed because the client did not have the necessary security privilege.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-437"><span id="WBEM_E_INVALID_OPERATOR"></span><span id="wbem_e_invalid_operator"></span>**WBEM \_ E \_ opérateur non valide \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-437"><span id="WBEM_E_INVALID_OPERATOR"></span><span id="wbem_e_invalid_operator"></span>**WBEM\_E\_INVALID\_OPERATOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-438">2147749987 (0x80041063)</span><span class="sxs-lookup"><span data-stu-id="cca14-438">2147749987 (0x80041063)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-439">L’opérateur n’est pas valide pour ce type de propriété.</span><span class="sxs-lookup"><span data-stu-id="cca14-439">Operator is not valid for this property type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-440"><span id="WBEM_E_LOCAL_CREDENTIALS"></span><span id="wbem_e_local_credentials"></span>**\_ \_ \_ informations d’identification locales WBEM**</span><span class="sxs-lookup"><span data-stu-id="cca14-440"><span id="WBEM_E_LOCAL_CREDENTIALS"></span><span id="wbem_e_local_credentials"></span>**WBEM\_E\_LOCAL\_CREDENTIALS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-441">2147749988 (0x80041064)</span><span class="sxs-lookup"><span data-stu-id="cca14-441">2147749988 (0x80041064)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-442">L’utilisateur a spécifié un nom d’utilisateur/mot de passe/autorité sur une connexion locale.</span><span class="sxs-lookup"><span data-stu-id="cca14-442">User specified a username/password/authority on a local connection.</span></span> <span data-ttu-id="cca14-443">L’utilisateur doit utiliser un nom d’utilisateur/mot de passe vide et s’appuyer sur la sécurité par défaut.</span><span class="sxs-lookup"><span data-stu-id="cca14-443">The user must use a blank username/password and rely on default security.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-444"><span id="WBEM_E_CANNOT_BE_ABSTRACT"></span><span id="wbem_e_cannot_be_abstract"></span>**WBEM \_ E \_ ne peut pas \_ être \_ abstract**</span><span class="sxs-lookup"><span data-stu-id="cca14-444"><span id="WBEM_E_CANNOT_BE_ABSTRACT"></span><span id="wbem_e_cannot_be_abstract"></span>**WBEM\_E\_CANNOT\_BE\_ABSTRACT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-445">2147749989 (0x80041065)</span><span class="sxs-lookup"><span data-stu-id="cca14-445">2147749989 (0x80041065)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-446">La classe a été rendue abstraite lorsque sa classe parente n’est pas abstraite.</span><span class="sxs-lookup"><span data-stu-id="cca14-446">Class was made abstract when its parent class is not abstract.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-447"><span id="WBEM_E_AMENDED_OBJECT"></span><span id="wbem_e_amended_object"></span>**WBEM \_ E a \_ modifié l' \_ objet**</span><span class="sxs-lookup"><span data-stu-id="cca14-447"><span id="WBEM_E_AMENDED_OBJECT"></span><span id="wbem_e_amended_object"></span>**WBEM\_E\_AMENDED\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-448">2147749990 (0x80041066)</span><span class="sxs-lookup"><span data-stu-id="cca14-448">2147749990 (0x80041066)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-449">L’objet modifié a été écrit sans que l’indicateur **WBEM \_ \_ use \_ Modified \_ Qualifiers** ne soit spécifié.</span><span class="sxs-lookup"><span data-stu-id="cca14-449">Amended object was written without the **WBEM\_FLAG\_USE\_AMENDED\_QUALIFIERS** flag being specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-450"><span id="WBEM_E_CLIENT_TOO_SLOW"></span><span id="wbem_e_client_too_slow"></span>**\_client WBEM \_ E \_ trop \_ lent**</span><span class="sxs-lookup"><span data-stu-id="cca14-450"><span id="WBEM_E_CLIENT_TOO_SLOW"></span><span id="wbem_e_client_too_slow"></span>**WBEM\_E\_CLIENT\_TOO\_SLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-451">2147749991 (0x80041067)</span><span class="sxs-lookup"><span data-stu-id="cca14-451">2147749991 (0x80041067)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-452">Le client n’a pas récupéré d’objets assez rapidement à partir d’une énumération.</span><span class="sxs-lookup"><span data-stu-id="cca14-452">Client did not retrieve objects quickly enough from an enumeration.</span></span> <span data-ttu-id="cca14-453">Cette constante est retournée lorsqu’un client crée un objet d’énumération, mais ne récupère pas les objets de l’énumérateur à temps, ce qui entraîne la sauvegarde des caches d’objets de l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="cca14-453">This constant is returned when a client creates an enumeration object, but does not retrieve objects from the enumerator in a timely fashion, causing the enumerator's object caches to back up.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-454"><span id="WBEM_E_NULL_SECURITY_DESCRIPTOR"></span><span id="wbem_e_null_security_descriptor"></span>**descripteur de sécurité de WBEM \_ E \_ null \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-454"><span id="WBEM_E_NULL_SECURITY_DESCRIPTOR"></span><span id="wbem_e_null_security_descriptor"></span>**WBEM\_E\_NULL\_SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-455">2147749992 (0x80041068)</span><span class="sxs-lookup"><span data-stu-id="cca14-455">2147749992 (0x80041068)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-456">Le descripteur de sécurité null a été utilisé.</span><span class="sxs-lookup"><span data-stu-id="cca14-456">Null security descriptor was used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-457"><span id="WBEM_E_TIMED_OUT"></span><span id="wbem_e_timed_out"></span>**délai d’attente de WBEM \_ E \_ dépassé \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-457"><span id="WBEM_E_TIMED_OUT"></span><span id="wbem_e_timed_out"></span>**WBEM\_E\_TIMED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-458">2147749993 (0x80041069)</span><span class="sxs-lookup"><span data-stu-id="cca14-458">2147749993 (0x80041069)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-459">L’opération a expiré.</span><span class="sxs-lookup"><span data-stu-id="cca14-459">Operation timed out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-460"><span id="WBEM_E_INVALID_ASSOCIATION"></span><span id="wbem_e_invalid_association"></span>**\_ \_ Association non valide \_ WBEM**</span><span class="sxs-lookup"><span data-stu-id="cca14-460"><span id="WBEM_E_INVALID_ASSOCIATION"></span><span id="wbem_e_invalid_association"></span>**WBEM\_E\_INVALID\_ASSOCIATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-461">2147749994</span><span class="sxs-lookup"><span data-stu-id="cca14-461">2147749994</span></span>
</dt> <dt>



<span data-ttu-id="cca14-462">Association non valide.</span><span class="sxs-lookup"><span data-stu-id="cca14-462">Association is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-463"><span id="WBEM_E_AMBIGUOUS_OPERATION"></span><span id="wbem_e_ambiguous_operation"></span>**\_ \_ opération ambiguë d’E WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-463"><span id="WBEM_E_AMBIGUOUS_OPERATION"></span><span id="wbem_e_ambiguous_operation"></span>**WBEM\_E\_AMBIGUOUS\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-464">2147749995 (0x8004106B)</span><span class="sxs-lookup"><span data-stu-id="cca14-464">2147749995 (0x8004106B)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-465">L’opération était ambiguë.</span><span class="sxs-lookup"><span data-stu-id="cca14-465">Operation was ambiguous.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-466"><span id="WBEM_E_QUOTA_VIOLATION"></span><span id="wbem_e_quota_violation"></span>**\_violation de \_ quota d’E WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-466"><span id="WBEM_E_QUOTA_VIOLATION"></span><span id="wbem_e_quota_violation"></span>**WBEM\_E\_QUOTA\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-467">2147749996 (0x8004106C)</span><span class="sxs-lookup"><span data-stu-id="cca14-467">2147749996 (0x8004106C)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-468">WMI prend trop de mémoire.</span><span class="sxs-lookup"><span data-stu-id="cca14-468">WMI is taking up too much memory.</span></span> <span data-ttu-id="cca14-469">Cela peut être dû à une faible disponibilité de la mémoire ou à une consommation excessive de la mémoire par WMI.</span><span class="sxs-lookup"><span data-stu-id="cca14-469">This can be caused by low memory availability or excessive memory consumption by WMI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-470"><span id="WBEM_E_TRANSACTION_CONFLICT"></span><span id="wbem_e_transaction_conflict"></span>**\_conflit de \_ transactions WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-470"><span id="WBEM_E_TRANSACTION_CONFLICT"></span><span id="wbem_e_transaction_conflict"></span>**WBEM\_E\_TRANSACTION\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-471">2147749997 (0x8004106D)</span><span class="sxs-lookup"><span data-stu-id="cca14-471">2147749997 (0x8004106D)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-472">L’opération a entraîné un conflit de transactions.</span><span class="sxs-lookup"><span data-stu-id="cca14-472">Operation resulted in a transaction conflict.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-473"><span id="WBEM_E_FORCED_ROLLBACK"></span><span id="wbem_e_forced_rollback"></span>**\_ \_ restauration forcée de WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-473"><span id="WBEM_E_FORCED_ROLLBACK"></span><span id="wbem_e_forced_rollback"></span>**WBEM\_E\_FORCED\_ROLLBACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-474">2147749998 (0x8004106E)</span><span class="sxs-lookup"><span data-stu-id="cca14-474">2147749998 (0x8004106E)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-475">La transaction a forcé une restauration.</span><span class="sxs-lookup"><span data-stu-id="cca14-475">Transaction forced a rollback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-476"><span id="WBEM_E_UNSUPPORTED_LOCALE"></span><span id="wbem_e_unsupported_locale"></span>**\_ \_ paramètres régionaux non pris en charge par WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-476"><span id="WBEM_E_UNSUPPORTED_LOCALE"></span><span id="wbem_e_unsupported_locale"></span>**WBEM\_E\_UNSUPPORTED\_LOCALE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-477">2147749999 (0x8004106F)</span><span class="sxs-lookup"><span data-stu-id="cca14-477">2147749999 (0x8004106F)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-478">Les paramètres régionaux utilisés dans l’appel ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="cca14-478">Locale used in the call is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-479"><span id="WBEM_E_HANDLE_OUT_OF_DATE"></span><span id="wbem_e_handle_out_of_date"></span>**\_ \_ gestion de WBEM \_ E \_ obsolète \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-479"><span id="WBEM_E_HANDLE_OUT_OF_DATE"></span><span id="wbem_e_handle_out_of_date"></span>**WBEM\_E\_HANDLE\_OUT\_OF\_DATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-480">2147750000 (0x80041070)</span><span class="sxs-lookup"><span data-stu-id="cca14-480">2147750000 (0x80041070)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-481">Le descripteur d’objet est obsolète.</span><span class="sxs-lookup"><span data-stu-id="cca14-481">Object handle is out-of-date.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-482"><span id="WBEM_E_CONNECTION_FAILED"></span><span id="wbem_e_connection_failed"></span>**échec de la \_ connexion E WBEM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-482"><span id="WBEM_E_CONNECTION_FAILED"></span><span id="wbem_e_connection_failed"></span>**WBEM\_E\_CONNECTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-483">2147750001 (0x80041071)</span><span class="sxs-lookup"><span data-stu-id="cca14-483">2147750001 (0x80041071)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-484">Échec de la connexion à la base de données SQL.</span><span class="sxs-lookup"><span data-stu-id="cca14-484">Connection to the SQL database failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-485"><span id="WBEM_E_INVALID_HANDLE_REQUEST"></span><span id="wbem_e_invalid_handle_request"></span>**\_demande de \_ \_ descripteur WBEM non valide \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-485"><span id="WBEM_E_INVALID_HANDLE_REQUEST"></span><span id="wbem_e_invalid_handle_request"></span>**WBEM\_E\_INVALID\_HANDLE\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-486">2147750002 (0x80041072)</span><span class="sxs-lookup"><span data-stu-id="cca14-486">2147750002 (0x80041072)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-487">La requête de handle n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="cca14-487">Handle request was not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-488"><span id="WBEM_E_PROPERTY_NAME_TOO_WIDE"></span><span id="wbem_e_property_name_too_wide"></span>**\_nom de propriété WBEM E \_ \_ \_ trop \_ grand**</span><span class="sxs-lookup"><span data-stu-id="cca14-488"><span id="WBEM_E_PROPERTY_NAME_TOO_WIDE"></span><span id="wbem_e_property_name_too_wide"></span>**WBEM\_E\_PROPERTY\_NAME\_TOO\_WIDE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-489">2147750003 (0x80041073)</span><span class="sxs-lookup"><span data-stu-id="cca14-489">2147750003 (0x80041073)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-490">Le nom de la propriété contient plus de 255 caractères.</span><span class="sxs-lookup"><span data-stu-id="cca14-490">Property name contains more than 255 characters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-491"><span id="WBEM_E_CLASS_NAME_TOO_WIDE"></span><span id="wbem_e_class_name_too_wide"></span>**\_nom de \_ classe E WBEM \_ \_ trop \_ grand**</span><span class="sxs-lookup"><span data-stu-id="cca14-491"><span id="WBEM_E_CLASS_NAME_TOO_WIDE"></span><span id="wbem_e_class_name_too_wide"></span>**WBEM\_E\_CLASS\_NAME\_TOO\_WIDE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-492">2147750004 (0x80041074)</span><span class="sxs-lookup"><span data-stu-id="cca14-492">2147750004 (0x80041074)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-493">Le nom de la classe contient plus de 255 caractères.</span><span class="sxs-lookup"><span data-stu-id="cca14-493">Class name contains more than 255 characters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-494"><span id="WBEM_E_METHOD_NAME_TOO_WIDE"></span><span id="wbem_e_method_name_too_wide"></span>**nom de la \_ méthode WBEM E \_ \_ \_ trop \_ grand**</span><span class="sxs-lookup"><span data-stu-id="cca14-494"><span id="WBEM_E_METHOD_NAME_TOO_WIDE"></span><span id="wbem_e_method_name_too_wide"></span>**WBEM\_E\_METHOD\_NAME\_TOO\_WIDE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-495">2147750005 (0x80041075)</span><span class="sxs-lookup"><span data-stu-id="cca14-495">2147750005 (0x80041075)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-496">Le nom de la méthode contient plus de 255 caractères.</span><span class="sxs-lookup"><span data-stu-id="cca14-496">Method name contains more than 255 characters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-497"><span id="WBEM_E_QUALIFIER_NAME_TOO_WIDE"></span><span id="wbem_e_qualifier_name_too_wide"></span>**\_nom de qualificateur d’E WBEM \_ \_ \_ trop \_ grand**</span><span class="sxs-lookup"><span data-stu-id="cca14-497"><span id="WBEM_E_QUALIFIER_NAME_TOO_WIDE"></span><span id="wbem_e_qualifier_name_too_wide"></span>**WBEM\_E\_QUALIFIER\_NAME\_TOO\_WIDE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-498">2147750006 (0x80041076)</span><span class="sxs-lookup"><span data-stu-id="cca14-498">2147750006 (0x80041076)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-499">Le nom du qualificateur contient plus de 255 caractères.</span><span class="sxs-lookup"><span data-stu-id="cca14-499">Qualifier name contains more than 255 characters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-500"><span id="WBEM_E_RERUN_COMMAND"></span><span id="wbem_e_rerun_command"></span>**\_commande WBEM E \_ relancer \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-500"><span id="WBEM_E_RERUN_COMMAND"></span><span id="wbem_e_rerun_command"></span>**WBEM\_E\_RERUN\_COMMAND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-501">2147750007 (0x80041077)</span><span class="sxs-lookup"><span data-stu-id="cca14-501">2147750007 (0x80041077)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-502">La commande SQL doit être réexécutée en raison d’un blocage dans SQL.</span><span class="sxs-lookup"><span data-stu-id="cca14-502">The SQL command must be rerun because there is a deadlock in SQL.</span></span> <span data-ttu-id="cca14-503">Cela peut être retourné uniquement lorsque des données sont stockées dans une base de données SQL.</span><span class="sxs-lookup"><span data-stu-id="cca14-503">This can be returned only when data is being stored in an SQL database.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-504"><span id="WBEM_E_DATABASE_VER_MISMATCH"></span><span id="wbem_e_database_ver_mismatch"></span>**\_incompatibilité \_ de la base de données WBEM E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-504"><span id="WBEM_E_DATABASE_VER_MISMATCH"></span><span id="wbem_e_database_ver_mismatch"></span>**WBEM\_E\_DATABASE\_VER\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-505">2147750008 (0x80041078)</span><span class="sxs-lookup"><span data-stu-id="cca14-505">2147750008 (0x80041078)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-506">La version de la base de données ne correspond pas à la version que le pilote du référentiel traite.</span><span class="sxs-lookup"><span data-stu-id="cca14-506">The database version does not match the version that the repository driver processes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-507"><span id="WBEM_E_VETO_DELETE"></span><span id="wbem_e_veto_delete"></span>**WBEM \_ E \_ veto \_ Supprimer**</span><span class="sxs-lookup"><span data-stu-id="cca14-507"><span id="WBEM_E_VETO_DELETE"></span><span id="wbem_e_veto_delete"></span>**WBEM\_E\_VETO\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-508">2147750009 (0x80041079)</span><span class="sxs-lookup"><span data-stu-id="cca14-508">2147750009 (0x80041079)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-509">WMI ne peut pas exécuter l’opération de suppression, car le fournisseur ne l’autorise pas.</span><span class="sxs-lookup"><span data-stu-id="cca14-509">WMI cannot execute the delete operation because the provider does not allow it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-510"><span id="WBEM_E_VETO_PUT"></span><span id="wbem_e_veto_put"></span>**WBEM \_ E \_ veto \_ put**</span><span class="sxs-lookup"><span data-stu-id="cca14-510"><span id="WBEM_E_VETO_PUT"></span><span id="wbem_e_veto_put"></span>**WBEM\_E\_VETO\_PUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-511">2147750010 (0x8004107A)</span><span class="sxs-lookup"><span data-stu-id="cca14-511">2147750010 (0x8004107A)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-512">WMI ne peut pas exécuter l’opération Put, car le fournisseur ne l’autorise pas.</span><span class="sxs-lookup"><span data-stu-id="cca14-512">WMI cannot execute the put operation because the provider does not allow it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-513"><span id="WBEM_E_INVALID_LOCALE"></span><span id="wbem_e_invalid_locale"></span>**\_ \_ paramètres régionaux WBEM non valides \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-513"><span id="WBEM_E_INVALID_LOCALE"></span><span id="wbem_e_invalid_locale"></span>**WBEM\_E\_INVALID\_LOCALE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-514">2147750016 (0x80041080)</span><span class="sxs-lookup"><span data-stu-id="cca14-514">2147750016 (0x80041080)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-515">L’identificateur de paramètres régionaux spécifié n’est pas valide pour l’opération.</span><span class="sxs-lookup"><span data-stu-id="cca14-515">Specified locale identifier was not valid for the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-516"><span id="WBEM_E_PROVIDER_SUSPENDED"></span><span id="wbem_e_provider_suspended"></span>**\_fournisseur WBEM \_ E \_ suspendu**</span><span class="sxs-lookup"><span data-stu-id="cca14-516"><span id="WBEM_E_PROVIDER_SUSPENDED"></span><span id="wbem_e_provider_suspended"></span>**WBEM\_E\_PROVIDER\_SUSPENDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-517">2147750017 (0x80041081)</span><span class="sxs-lookup"><span data-stu-id="cca14-517">2147750017 (0x80041081)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-518">Le fournisseur est suspendu.</span><span class="sxs-lookup"><span data-stu-id="cca14-518">Provider is suspended.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-519"><span id="WBEM_E_SYNCHRONIZATION_REQUIRED"></span><span id="wbem_e_synchronization_required"></span>**\_synchronisation WBEM \_ E \_ requise**</span><span class="sxs-lookup"><span data-stu-id="cca14-519"><span id="WBEM_E_SYNCHRONIZATION_REQUIRED"></span><span id="wbem_e_synchronization_required"></span>**WBEM\_E\_SYNCHRONIZATION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-520">2147750018 (0x80041082)</span><span class="sxs-lookup"><span data-stu-id="cca14-520">2147750018 (0x80041082)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-521">L’objet doit être écrit dans le référentiel WMI et récupéré à nouveau avant que l’opération demandée puisse aboutir.</span><span class="sxs-lookup"><span data-stu-id="cca14-521">Object must be written to the WMI repository and retrieved again before the requested operation can succeed.</span></span> <span data-ttu-id="cca14-522">Cette constante est retournée lorsqu’un objet doit être validé et récupéré pour voir la valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="cca14-522">This constant is returned when an object must be committed and retrieved to see the property value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-523"><span id="WBEM_E_NO_SCHEMA"></span><span id="wbem_e_no_schema"></span>**\_schéma E \_ non \_ WBEM**</span><span class="sxs-lookup"><span data-stu-id="cca14-523"><span id="WBEM_E_NO_SCHEMA"></span><span id="wbem_e_no_schema"></span>**WBEM\_E\_NO\_SCHEMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-524">2147750019 (0x80041083)</span><span class="sxs-lookup"><span data-stu-id="cca14-524">2147750019 (0x80041083)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-525">L’opération ne peut pas être terminée ; aucun schéma n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="cca14-525">Operation cannot be completed; no schema is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-526"><span id="WBEM_E_PROVIDER_ALREADY_REGISTERED"></span><span id="wbem_e_provider_already_registered"></span>**le \_ fournisseur WBEM E est \_ \_ déjà \_ inscrit**</span><span class="sxs-lookup"><span data-stu-id="cca14-526"><span id="WBEM_E_PROVIDER_ALREADY_REGISTERED"></span><span id="wbem_e_provider_already_registered"></span>**WBEM\_E\_PROVIDER\_ALREADY\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-527">02147750020 (0x119FD010)</span><span class="sxs-lookup"><span data-stu-id="cca14-527">02147750020 (0x119FD010)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-528">Impossible d’inscrire le fournisseur, car il est déjà inscrit.</span><span class="sxs-lookup"><span data-stu-id="cca14-528">Provider cannot be registered because it is already registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-529"><span id="WBEM_E_PROVIDER_NOT_REGISTERED"></span><span id="wbem_e_provider_not_registered"></span>**\_fournisseur WBEM \_ E \_ non \_ inscrit**</span><span class="sxs-lookup"><span data-stu-id="cca14-529"><span id="WBEM_E_PROVIDER_NOT_REGISTERED"></span><span id="wbem_e_provider_not_registered"></span>**WBEM\_E\_PROVIDER\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-530">2147750021 (0x80041085)</span><span class="sxs-lookup"><span data-stu-id="cca14-530">2147750021 (0x80041085)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-531">Le fournisseur n’a pas été inscrit.</span><span class="sxs-lookup"><span data-stu-id="cca14-531">Provider was not registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-532"><span id="WBEM_E_FATAL_TRANSPORT_ERROR"></span><span id="wbem_e_fatal_transport_error"></span>**\_erreur de \_ transport non récupérable \_ \_ WBEM**</span><span class="sxs-lookup"><span data-stu-id="cca14-532"><span id="WBEM_E_FATAL_TRANSPORT_ERROR"></span><span id="wbem_e_fatal_transport_error"></span>**WBEM\_E\_FATAL\_TRANSPORT\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-533">2147750022 (0x80041086)</span><span class="sxs-lookup"><span data-stu-id="cca14-533">2147750022 (0x80041086)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-534">Une erreur de transport irrécupérable s’est produite.</span><span class="sxs-lookup"><span data-stu-id="cca14-534">A fatal transport error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-535"><span id="WBEM_E_ENCRYPTED_CONNECTION_REQUIRED"></span><span id="wbem_e_encrypted_connection_required"></span>**\_ \_ connexion chiffrée WBEM \_ \_ requise**</span><span class="sxs-lookup"><span data-stu-id="cca14-535"><span id="WBEM_E_ENCRYPTED_CONNECTION_REQUIRED"></span><span id="wbem_e_encrypted_connection_required"></span>**WBEM\_E\_ENCRYPTED\_CONNECTION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-536">2147750023 (0x80041087)</span><span class="sxs-lookup"><span data-stu-id="cca14-536">2147750023 (0x80041087)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-537">L’utilisateur a tenté de définir un nom d’ordinateur ou un domaine sans connexion chiffrée.</span><span class="sxs-lookup"><span data-stu-id="cca14-537">User attempted to set a computer name or domain without an encrypted connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-538"><span id="WBEM_E_PROVIDER_TIMED_OUT"></span><span id="wbem_e_provider_timed_out"></span>**délai d’attente du \_ fournisseur WBEM E \_ \_ dépassé \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-538"><span id="WBEM_E_PROVIDER_TIMED_OUT"></span><span id="wbem_e_provider_timed_out"></span>**WBEM\_E\_PROVIDER\_TIMED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-539">2147750024 (0x80041088)</span><span class="sxs-lookup"><span data-stu-id="cca14-539">2147750024 (0x80041088)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-540">Un fournisseur n’a pas pu signaler les résultats dans le délai d’attente spécifié.</span><span class="sxs-lookup"><span data-stu-id="cca14-540">A provider failed to report results within the specified timeout.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-541"><span id="WBEM_E_NO_KEY"></span><span id="wbem_e_no_key"></span>**\_clé E \_ non \_ WBEM**</span><span class="sxs-lookup"><span data-stu-id="cca14-541"><span id="WBEM_E_NO_KEY"></span><span id="wbem_e_no_key"></span>**WBEM\_E\_NO\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-542">2147750025 (0x80041089)</span><span class="sxs-lookup"><span data-stu-id="cca14-542">2147750025 (0x80041089)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-543">L’utilisateur a tenté de mettre une instance sans clé définie.</span><span class="sxs-lookup"><span data-stu-id="cca14-543">User attempted to put an instance with no defined key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-544"><span id="WBEM_E_PROVIDER_DISABLED"></span><span id="wbem_e_provider_disabled"></span>**\_fournisseur WBEM \_ E \_ désactivé**</span><span class="sxs-lookup"><span data-stu-id="cca14-544"><span id="WBEM_E_PROVIDER_DISABLED"></span><span id="wbem_e_provider_disabled"></span>**WBEM\_E\_PROVIDER\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-545">2147750026 (0x8004108A)</span><span class="sxs-lookup"><span data-stu-id="cca14-545">2147750026 (0x8004108A)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-546">L’utilisateur a tenté d’inscrire une instance de fournisseur, mais le serveur COM pour l’instance du fournisseur a été déchargé.</span><span class="sxs-lookup"><span data-stu-id="cca14-546">User attempted to register a provider instance but the COM server for the provider instance was unloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-547"><span id="WBEMESS_E_REGISTRATION_TOO_BROAD"></span><span id="wbemess_e_registration_too_broad"></span>**\_inscription WBEMESS \_ E \_ trop \_ large**</span><span class="sxs-lookup"><span data-stu-id="cca14-547"><span id="WBEMESS_E_REGISTRATION_TOO_BROAD"></span><span id="wbemess_e_registration_too_broad"></span>**WBEMESS\_E\_REGISTRATION\_TOO\_BROAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-548">2147753985 (0x80042001)</span><span class="sxs-lookup"><span data-stu-id="cca14-548">2147753985 (0x80042001)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-549">L’inscription du fournisseur chevauche le domaine d’événements système.</span><span class="sxs-lookup"><span data-stu-id="cca14-549">Provider registration overlaps with the system event domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-550"><span id="WBEMESS_E_REGISTRATION_TOO_PRECISE"></span><span id="wbemess_e_registration_too_precise"></span>**\_inscription WBEMESS \_ E \_ trop \_ précise**</span><span class="sxs-lookup"><span data-stu-id="cca14-550"><span id="WBEMESS_E_REGISTRATION_TOO_PRECISE"></span><span id="wbemess_e_registration_too_precise"></span>**WBEMESS\_E\_REGISTRATION\_TOO\_PRECISE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-551">2147753986 (0x80042002)</span><span class="sxs-lookup"><span data-stu-id="cca14-551">2147753986 (0x80042002)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-552">Une clause WITHIN n'est pas utilisée dans cette requête.</span><span class="sxs-lookup"><span data-stu-id="cca14-552">A WITHIN clause was not used in this query.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-553"><span id="WBEMESS_E_AUTHZ_NOT_PRIVILEGED"></span><span id="wbemess_e_authz_not_privileged"></span>**WBEMESS \_ E \_ auth \_ non \_ privilégié**</span><span class="sxs-lookup"><span data-stu-id="cca14-553"><span id="WBEMESS_E_AUTHZ_NOT_PRIVILEGED"></span><span id="wbemess_e_authz_not_privileged"></span>**WBEMESS\_E\_AUTHZ\_NOT\_PRIVILEGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-554">2147753987 (0x80042003)</span><span class="sxs-lookup"><span data-stu-id="cca14-554">2147753987 (0x80042003)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-555">Cet ordinateur ne dispose pas des autorisations de domaine nécessaires pour prendre en charge les fonctions de sécurité associées à l’instance d’abonnement créée.</span><span class="sxs-lookup"><span data-stu-id="cca14-555">This computer does not have the necessary domain permissions to support the security functions that relate to the created subscription instance.</span></span> <span data-ttu-id="cca14-556">Contactez l’administrateur de domaine pour que cet ordinateur soit ajouté au groupe d’accès d’autorisation Windows.</span><span class="sxs-lookup"><span data-stu-id="cca14-556">Contact the Domain Administrator to get this computer added to the Windows Authorization Access Group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-557"><span id="WBEM_E_RETRY_LATER"></span><span id="wbem_e_retry_later"></span>**WBEM \_ \_ Réessayer \_ plus tard**</span><span class="sxs-lookup"><span data-stu-id="cca14-557"><span id="WBEM_E_RETRY_LATER"></span><span id="wbem_e_retry_later"></span>**WBEM\_E\_RETRY\_LATER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-558">2147758081 (0x80043001)</span><span class="sxs-lookup"><span data-stu-id="cca14-558">2147758081 (0x80043001)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-559">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="cca14-559">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-560"><span id="WBEM_E_RESOURCE_CONTENTION"></span><span id="wbem_e_resource_contention"></span>**\_conflit de \_ ressources WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-560"><span id="WBEM_E_RESOURCE_CONTENTION"></span><span id="wbem_e_resource_contention"></span>**WBEM\_E\_RESOURCE\_CONTENTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-561">2147758082 (0x80043002)</span><span class="sxs-lookup"><span data-stu-id="cca14-561">2147758082 (0x80043002)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-562">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="cca14-562">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-563"><span id="WBEMMOF_E_EXPECTED_QUALIFIER_NAME"></span><span id="wbemmof_e_expected_qualifier_name"></span>**WBEMMOF \_ E \_ \_ nom du qualificateur attendu \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-563"><span id="WBEMMOF_E_EXPECTED_QUALIFIER_NAME"></span><span id="wbemmof_e_expected_qualifier_name"></span>**WBEMMOF\_E\_EXPECTED\_QUALIFIER\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-564">2147762177 (0x80044001)</span><span class="sxs-lookup"><span data-stu-id="cca14-564">2147762177 (0x80044001)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-565">Nom de qualificateur attendu.</span><span class="sxs-lookup"><span data-stu-id="cca14-565">Expected a qualifier name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-566"><span id="WBEMMOF_E_EXPECTED_SEMI"></span><span id="wbemmof_e_expected_semi"></span>**WBEMMOF \_ E \_ attendu \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-566"><span id="WBEMMOF_E_EXPECTED_SEMI"></span><span id="wbemmof_e_expected_semi"></span>**WBEMMOF\_E\_EXPECTED\_SEMI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-567">2147762178 (0x80044002)</span><span class="sxs-lookup"><span data-stu-id="cca14-567">2147762178 (0x80044002)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-568">Point-virgule ou' = 'attendu.</span><span class="sxs-lookup"><span data-stu-id="cca14-568">Expected semicolon or '='.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-569"><span id="WBEMMOF_E_EXPECTED_OPEN_BRACE"></span><span id="wbemmof_e_expected_open_brace"></span>**WBEMMOF \_ E \_ \_ accolade ouvrante attendue \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-569"><span id="WBEMMOF_E_EXPECTED_OPEN_BRACE"></span><span id="wbemmof_e_expected_open_brace"></span>**WBEMMOF\_E\_EXPECTED\_OPEN\_BRACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-570">2147762179 (0x80044003)</span><span class="sxs-lookup"><span data-stu-id="cca14-570">2147762179 (0x80044003)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-571">Accolade ouvrante attendue.</span><span class="sxs-lookup"><span data-stu-id="cca14-571">Expected an opening brace.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-572"><span id="WBEMMOF_E_EXPECTED_CLOSE_BRACE"></span><span id="wbemmof_e_expected_close_brace"></span>**WBEMMOF \_ E \_ \_ accolade fermante attendue \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-572"><span id="WBEMMOF_E_EXPECTED_CLOSE_BRACE"></span><span id="wbemmof_e_expected_close_brace"></span>**WBEMMOF\_E\_EXPECTED\_CLOSE\_BRACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-573">2147762180 (0x80044004)</span><span class="sxs-lookup"><span data-stu-id="cca14-573">2147762180 (0x80044004)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-574">Accolade fermante manquante ou élément de tableau non conforme.</span><span class="sxs-lookup"><span data-stu-id="cca14-574">Missing closing brace or an illegal array element.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-575"><span id="WBEMMOF_E_EXPECTED_CLOSE_BRACKET"></span><span id="wbemmof_e_expected_close_bracket"></span>**WBEMMOF \_ E \_ \_ crochet fermant \_ attendu**</span><span class="sxs-lookup"><span data-stu-id="cca14-575"><span id="WBEMMOF_E_EXPECTED_CLOSE_BRACKET"></span><span id="wbemmof_e_expected_close_bracket"></span>**WBEMMOF\_E\_EXPECTED\_CLOSE\_BRACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-576">2147762181 (0x80044005)</span><span class="sxs-lookup"><span data-stu-id="cca14-576">2147762181 (0x80044005)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-577">Crochet fermant attendu.</span><span class="sxs-lookup"><span data-stu-id="cca14-577">Expected a closing bracket.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-578"><span id="WBEMMOF_E_EXPECTED_CLOSE_PAREN"></span><span id="wbemmof_e_expected_close_paren"></span>**WBEMMOF \_ E \_ \_ parenthèse fermante attendue \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-578"><span id="WBEMMOF_E_EXPECTED_CLOSE_PAREN"></span><span id="wbemmof_e_expected_close_paren"></span>**WBEMMOF\_E\_EXPECTED\_CLOSE\_PAREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-579">2147762182 (0x80044006)</span><span class="sxs-lookup"><span data-stu-id="cca14-579">2147762182 (0x80044006)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-580">Parenthèse fermante attendue.</span><span class="sxs-lookup"><span data-stu-id="cca14-580">Expected closing parenthesis.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-581"><span id="WBEMMOF_E_ILLEGAL_CONSTANT_VALUE"></span><span id="wbemmof_e_illegal_constant_value"></span>**WBEMMOF \_ E \_ \_ valeur constante non conforme \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-581"><span id="WBEMMOF_E_ILLEGAL_CONSTANT_VALUE"></span><span id="wbemmof_e_illegal_constant_value"></span>**WBEMMOF\_E\_ILLEGAL\_CONSTANT\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-582">2147762183 (0x80044007)</span><span class="sxs-lookup"><span data-stu-id="cca14-582">2147762183 (0x80044007)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-583">Valeur numérique hors limites ou chaînes sans guillemets.</span><span class="sxs-lookup"><span data-stu-id="cca14-583">Numeric value out of range or strings without quotes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-584"><span id="WBEMMOF_E_EXPECTED_TYPE_IDENTIFIER"></span><span id="wbemmof_e_expected_type_identifier"></span>**WBEMMOF \_ E \_ \_ identificateur de type attendu \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-584"><span id="WBEMMOF_E_EXPECTED_TYPE_IDENTIFIER"></span><span id="wbemmof_e_expected_type_identifier"></span>**WBEMMOF\_E\_EXPECTED\_TYPE\_IDENTIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-585">2147762184 (0x80044008)</span><span class="sxs-lookup"><span data-stu-id="cca14-585">2147762184 (0x80044008)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-586">Identificateur de type attendu.</span><span class="sxs-lookup"><span data-stu-id="cca14-586">Expected a type identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-587"><span id="WBEMMOF_E_EXPECTED_OPEN_PAREN"></span><span id="wbemmof_e_expected_open_paren"></span>**WBEMMOF \_ E \_ \_ parenthèse ouverte attendue \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-587"><span id="WBEMMOF_E_EXPECTED_OPEN_PAREN"></span><span id="wbemmof_e_expected_open_paren"></span>**WBEMMOF\_E\_EXPECTED\_OPEN\_PAREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-588">2147762185 (0x80044009)</span><span class="sxs-lookup"><span data-stu-id="cca14-588">2147762185 (0x80044009)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-589">Parenthèse ouverte attendue.</span><span class="sxs-lookup"><span data-stu-id="cca14-589">Expected an open parenthesis.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-590"><span id="WBEMMOF_E_UNRECOGNIZED_TOKEN"></span><span id="wbemmof_e_unrecognized_token"></span>**WBEMMOF \_ E \_ jeton non reconnu \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-590"><span id="WBEMMOF_E_UNRECOGNIZED_TOKEN"></span><span id="wbemmof_e_unrecognized_token"></span>**WBEMMOF\_E\_UNRECOGNIZED\_TOKEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-591">2147762186 (0x8004400A)</span><span class="sxs-lookup"><span data-stu-id="cca14-591">2147762186 (0x8004400A)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-592">Jeton inattendu dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="cca14-592">Unexpected token in the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-593"><span id="WBEMMOF_E_UNRECOGNIZED_TYPE"></span><span id="wbemmof_e_unrecognized_type"></span>**WBEMMOF \_ E \_ type non reconnu \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-593"><span id="WBEMMOF_E_UNRECOGNIZED_TYPE"></span><span id="wbemmof_e_unrecognized_type"></span>**WBEMMOF\_E\_UNRECOGNIZED\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-594">2147762187 (0x8004400B)</span><span class="sxs-lookup"><span data-stu-id="cca14-594">2147762187 (0x8004400B)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-595">Identificateur de type non reconnu ou non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="cca14-595">Unrecognized or unsupported type identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-596"><span id="WBEMMOF_E_EXPECTED_PROPERTY_NAME"></span><span id="wbemmof_e_expected_property_name"></span>**WBEMMOF \_ E \_ nom de la propriété attendue \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-596"><span id="WBEMMOF_E_EXPECTED_PROPERTY_NAME"></span><span id="wbemmof_e_expected_property_name"></span>**WBEMMOF\_E\_EXPECTED\_PROPERTY\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-597">2147762187 (0x8004400B)</span><span class="sxs-lookup"><span data-stu-id="cca14-597">2147762187 (0x8004400B)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-598">Nom de la propriété ou de la méthode attendu.</span><span class="sxs-lookup"><span data-stu-id="cca14-598">Expected property or method name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-599"><span id="WBEMMOF_E_TYPEDEF_NOT_SUPPORTED"></span><span id="wbemmof_e_typedef_not_supported"></span>**WBEMMOF \_ E \_ typedef \_ non \_ pris en charge**</span><span class="sxs-lookup"><span data-stu-id="cca14-599"><span id="WBEMMOF_E_TYPEDEF_NOT_SUPPORTED"></span><span id="wbemmof_e_typedef_not_supported"></span>**WBEMMOF\_E\_TYPEDEF\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-600">2147762189 (0x8004400D)</span><span class="sxs-lookup"><span data-stu-id="cca14-600">2147762189 (0x8004400D)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-601">Les typedefs et les types énumérés ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="cca14-601">Typedefs and enumerated types are not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-602"><span id="WBEMMOF_E_UNEXPECTED_ALIAS"></span><span id="wbemmof_e_unexpected_alias"></span>**WBEMMOF \_ E \_ \_ alias inattendu**</span><span class="sxs-lookup"><span data-stu-id="cca14-602"><span id="WBEMMOF_E_UNEXPECTED_ALIAS"></span><span id="wbemmof_e_unexpected_alias"></span>**WBEMMOF\_E\_UNEXPECTED\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-603">2147762190 (0x8004400E)</span><span class="sxs-lookup"><span data-stu-id="cca14-603">2147762190 (0x8004400E)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-604">Seule une référence à un objet de classe peut avoir une valeur d’alias.</span><span class="sxs-lookup"><span data-stu-id="cca14-604">Only a reference to a class object can have an alias value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-605"><span id="WBEMMOF_E_UNEXPECTED_ARRAY_INIT"></span><span id="wbemmof_e_unexpected_array_init"></span>**WBEMMOF \_ E \_ inattendue de \_ tableau \_ init**</span><span class="sxs-lookup"><span data-stu-id="cca14-605"><span id="WBEMMOF_E_UNEXPECTED_ARRAY_INIT"></span><span id="wbemmof_e_unexpected_array_init"></span>**WBEMMOF\_E\_UNEXPECTED\_ARRAY\_INIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-606">2147762191 (0x8004400F)</span><span class="sxs-lookup"><span data-stu-id="cca14-606">2147762191 (0x8004400F)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-607">Initialisation de tableau inattendue.</span><span class="sxs-lookup"><span data-stu-id="cca14-607">Unexpected array initialization.</span></span> <span data-ttu-id="cca14-608">Les tableaux doivent être déclarés avec \[ \] .</span><span class="sxs-lookup"><span data-stu-id="cca14-608">Arrays must be declared with \[\].</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-609"><span id="WBEMMOF_E_INVALID_AMENDMENT_SYNTAX"></span><span id="wbemmof_e_invalid_amendment_syntax"></span>**WBEMMOF \_ E \_ \_ syntaxe d’amendement non valide \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-609"><span id="WBEMMOF_E_INVALID_AMENDMENT_SYNTAX"></span><span id="wbemmof_e_invalid_amendment_syntax"></span>**WBEMMOF\_E\_INVALID\_AMENDMENT\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-610">2147762192 (0x80044010)</span><span class="sxs-lookup"><span data-stu-id="cca14-610">2147762192 (0x80044010)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-611">La syntaxe du chemin d’accès de l’espace de noms n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="cca14-611">Namespace path syntax is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-612"><span id="WBEMMOF_E_INVALID_DUPLICATE_AMENDMENT"></span><span id="wbemmof_e_invalid_duplicate_amendment"></span>**WBEMMOF \_ E \_ \_ Amendement dupliqué non valide \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-612"><span id="WBEMMOF_E_INVALID_DUPLICATE_AMENDMENT"></span><span id="wbemmof_e_invalid_duplicate_amendment"></span>**WBEMMOF\_E\_INVALID\_DUPLICATE\_AMENDMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-613">2147762193 (0x80044011)</span><span class="sxs-lookup"><span data-stu-id="cca14-613">2147762193 (0x80044011)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-614">Spécificateurs d’amendement en double.</span><span class="sxs-lookup"><span data-stu-id="cca14-614">Duplicate amendment specifiers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-615"><span id="WBEMMOF_E_INVALID_PRAGMA"></span><span id="wbemmof_e_invalid_pragma"></span>**WBEMMOF \_ E \_ pragma non valide \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-615"><span id="WBEMMOF_E_INVALID_PRAGMA"></span><span id="wbemmof_e_invalid_pragma"></span>**WBEMMOF\_E\_INVALID\_PRAGMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-616">2147762194 (0x80044012)</span><span class="sxs-lookup"><span data-stu-id="cca14-616">2147762194 (0x80044012)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-617">le [ \# pragma](pragma-namespace.md) doit être suivi d’un mot clé valide.</span><span class="sxs-lookup"><span data-stu-id="cca14-617">[\#pragma](pragma-namespace.md) must be followed by a valid keyword.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-618"><span id="WBEMMOF_E_INVALID_NAMESPACE_SYNTAX"></span><span id="wbemmof_e_invalid_namespace_syntax"></span>**WBEMMOF \_ E \_ syntaxe d’espace de noms non valide \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-618"><span id="WBEMMOF_E_INVALID_NAMESPACE_SYNTAX"></span><span id="wbemmof_e_invalid_namespace_syntax"></span>**WBEMMOF\_E\_INVALID\_NAMESPACE\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-619">2147762195 (0x80044013)</span><span class="sxs-lookup"><span data-stu-id="cca14-619">2147762195 (0x80044013)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-620">La syntaxe du chemin d’accès de l’espace de noms n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="cca14-620">Namespace path syntax is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-621"><span id="WBEMMOF_E_EXPECTED_CLASS_NAME"></span><span id="wbemmof_e_expected_class_name"></span>**WBEMMOF \_ E \_ \_ nom de classe attendu \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-621"><span id="WBEMMOF_E_EXPECTED_CLASS_NAME"></span><span id="wbemmof_e_expected_class_name"></span>**WBEMMOF\_E\_EXPECTED\_CLASS\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-622">2147762196 (0x80044014)</span><span class="sxs-lookup"><span data-stu-id="cca14-622">2147762196 (0x80044014)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-623">Un caractère inattendu dans le nom de la classe doit être un identificateur.</span><span class="sxs-lookup"><span data-stu-id="cca14-623">Unexpected character in class name must be an identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-624"><span id="WBEMMOF_E_TYPE_MISMATCH"></span><span id="wbemmof_e_type_mismatch"></span>**incompatibilité de \_ type E WBEMMOF \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-624"><span id="WBEMMOF_E_TYPE_MISMATCH"></span><span id="wbemmof_e_type_mismatch"></span>**WBEMMOF\_E\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-625">2147762197 (0x80044015)</span><span class="sxs-lookup"><span data-stu-id="cca14-625">2147762197 (0x80044015)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-626">La valeur spécifiée ne peut pas être transformée dans le type approprié.</span><span class="sxs-lookup"><span data-stu-id="cca14-626">The value specified cannot be made into the appropriate type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-627"><span id="WBEMMOF_E_EXPECTED_ALIAS_NAME"></span><span id="wbemmof_e_expected_alias_name"></span>**WBEMMOF \_ E \_ \_ nom d’alias attendu \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-627"><span id="WBEMMOF_E_EXPECTED_ALIAS_NAME"></span><span id="wbemmof_e_expected_alias_name"></span>**WBEMMOF\_E\_EXPECTED\_ALIAS\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-628">2147762198 (0x80044016)</span><span class="sxs-lookup"><span data-stu-id="cca14-628">2147762198 (0x80044016)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-629">Le signe dollar doit être suivi d’un nom d’alias en tant qu’identificateur.</span><span class="sxs-lookup"><span data-stu-id="cca14-629">Dollar sign must be followed by an alias name as an identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-630"><span id="WBEMMOF_E_INVALID_CLASS_DECLARATION"></span><span id="wbemmof_e_invalid_class_declaration"></span>**WBEMMOF \_ E \_ \_ déclaration de classe non valide \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-630"><span id="WBEMMOF_E_INVALID_CLASS_DECLARATION"></span><span id="wbemmof_e_invalid_class_declaration"></span>**WBEMMOF\_E\_INVALID\_CLASS\_DECLARATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-631">2147762199 (0x80044017)</span><span class="sxs-lookup"><span data-stu-id="cca14-631">2147762199 (0x80044017)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-632">La déclaration de classe n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="cca14-632">Class declaration is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-633"><span id="WBEMMOF_E_INVALID_INSTANCE_DECLARATION"></span><span id="wbemmof_e_invalid_instance_declaration"></span>**WBEMMOF \_ E \_ \_ déclaration d’instance non valide \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-633"><span id="WBEMMOF_E_INVALID_INSTANCE_DECLARATION"></span><span id="wbemmof_e_invalid_instance_declaration"></span>**WBEMMOF\_E\_INVALID\_INSTANCE\_DECLARATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-634">2147762200 (0x80044018)</span><span class="sxs-lookup"><span data-stu-id="cca14-634">2147762200 (0x80044018)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-635">La déclaration d’instance n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="cca14-635">The instance declaration is not valid.</span></span> <span data-ttu-id="cca14-636">Il doit commencer par « instance de »</span><span class="sxs-lookup"><span data-stu-id="cca14-636">It must start with "instance of"</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-637"><span id="WBEMMOF_E_EXPECTED_DOLLAR"></span><span id="wbemmof_e_expected_dollar"></span>**WBEMMOF \_ E \_ \_ dollar ATTENDU**</span><span class="sxs-lookup"><span data-stu-id="cca14-637"><span id="WBEMMOF_E_EXPECTED_DOLLAR"></span><span id="wbemmof_e_expected_dollar"></span>**WBEMMOF\_E\_EXPECTED\_DOLLAR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-638">2147762201 (0x80044019)</span><span class="sxs-lookup"><span data-stu-id="cca14-638">2147762201 (0x80044019)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-639">Signe dollar attendu.</span><span class="sxs-lookup"><span data-stu-id="cca14-639">Expected dollar sign.</span></span> <span data-ttu-id="cca14-640">Un alias au format « $name » doit suivre le mot clé « As ».</span><span class="sxs-lookup"><span data-stu-id="cca14-640">An alias in the form "$name" must follow the "as" keyword.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-641"><span id="WBEMMOF_E_CIMTYPE_QUALIFIER"></span><span id="wbemmof_e_cimtype_qualifier"></span>**\_QUALIFICATEUR WBEMMOF E \_ CimType \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-641"><span id="WBEMMOF_E_CIMTYPE_QUALIFIER"></span><span id="wbemmof_e_cimtype_qualifier"></span>**WBEMMOF\_E\_CIMTYPE\_QUALIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-642">2147762202 (0x8004401A)</span><span class="sxs-lookup"><span data-stu-id="cca14-642">2147762202 (0x8004401A)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-643">Le qualificateur « CIMTYPE » ne peut pas être spécifié directement dans un fichier MOF.</span><span class="sxs-lookup"><span data-stu-id="cca14-643">"CIMTYPE" qualifier cannot be specified directly in a MOF file.</span></span> <span data-ttu-id="cca14-644">Utilisez la notation de type standard.</span><span class="sxs-lookup"><span data-stu-id="cca14-644">Use standard type notation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-645"><span id="WBEMMOF_E_DUPLICATE_PROPERTY"></span><span id="wbemmof_e_duplicate_property"></span>**WBEMMOF \_ E \_ , \_ propriété dupliquée**</span><span class="sxs-lookup"><span data-stu-id="cca14-645"><span id="WBEMMOF_E_DUPLICATE_PROPERTY"></span><span id="wbemmof_e_duplicate_property"></span>**WBEMMOF\_E\_DUPLICATE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-646">2147762203 (0x8004401B)</span><span class="sxs-lookup"><span data-stu-id="cca14-646">2147762203 (0x8004401B)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-647">Un nom de propriété dupliqué a été trouvé dans le MOF.</span><span class="sxs-lookup"><span data-stu-id="cca14-647">Duplicate property name was found in the MOF.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-648"><span id="WBEMMOF_E_INVALID_NAMESPACE_SPECIFICATION"></span><span id="wbemmof_e_invalid_namespace_specification"></span>**WBEMMOF \_ E \_ spécification d’espace de noms non valide \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-648"><span id="WBEMMOF_E_INVALID_NAMESPACE_SPECIFICATION"></span><span id="wbemmof_e_invalid_namespace_specification"></span>**WBEMMOF\_E\_INVALID\_NAMESPACE\_SPECIFICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-649">2147762204 (0x8004401C)</span><span class="sxs-lookup"><span data-stu-id="cca14-649">2147762204 (0x8004401C)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-650">La syntaxe de l’espace de noms n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="cca14-650">Namespace syntax is not valid.</span></span> <span data-ttu-id="cca14-651">Les références à d’autres serveurs ne sont pas autorisées.</span><span class="sxs-lookup"><span data-stu-id="cca14-651">References to other servers are not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-652"><span id="WBEMMOF_E_OUT_OF_RANGE"></span><span id="wbemmof_e_out_of_range"></span>**WBEMMOF \_ E \_ hors \_ \_ limites**</span><span class="sxs-lookup"><span data-stu-id="cca14-652"><span id="WBEMMOF_E_OUT_OF_RANGE"></span><span id="wbemmof_e_out_of_range"></span>**WBEMMOF\_E\_OUT\_OF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-653">2147762205 (0x8004401D)</span><span class="sxs-lookup"><span data-stu-id="cca14-653">2147762205 (0x8004401D)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-654">Valeur hors limites.</span><span class="sxs-lookup"><span data-stu-id="cca14-654">Value out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-655"><span id="WBEMMOF_E_INVALID_FILE"></span><span id="wbemmof_e_invalid_file"></span>**WBEMMOF \_ E \_ fichier non valide \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-655"><span id="WBEMMOF_E_INVALID_FILE"></span><span id="wbemmof_e_invalid_file"></span>**WBEMMOF\_E\_INVALID\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-656">2147762206 (0x8004401E)</span><span class="sxs-lookup"><span data-stu-id="cca14-656">2147762206 (0x8004401E)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-657">Le fichier n’est pas un fichier MOF de texte valide ou un fichier MOF binaire.</span><span class="sxs-lookup"><span data-stu-id="cca14-657">The file is not a valid text MOF file or binary MOF file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-658"><span id="WBEMMOF_E_ALIASES_IN_EMBEDDED"></span><span id="wbemmof_e_aliases_in_embedded"></span>**\_alias WBEMMOF E \_ \_ dans \_ Embedded**</span><span class="sxs-lookup"><span data-stu-id="cca14-658"><span id="WBEMMOF_E_ALIASES_IN_EMBEDDED"></span><span id="wbemmof_e_aliases_in_embedded"></span>**WBEMMOF\_E\_ALIASES\_IN\_EMBEDDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-659">2147762207 (0x8004401F)</span><span class="sxs-lookup"><span data-stu-id="cca14-659">2147762207 (0x8004401F)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-660">Les objets incorporés ne peuvent pas être des alias.</span><span class="sxs-lookup"><span data-stu-id="cca14-660">Embedded objects cannot be aliases.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-661"><span id="WBEMMOF_E_NULL_ARRAY_ELEM"></span><span id="wbemmof_e_null_array_elem"></span>**WBEMMOF \_ E \_ \_ tableau null \_ elem**</span><span class="sxs-lookup"><span data-stu-id="cca14-661"><span id="WBEMMOF_E_NULL_ARRAY_ELEM"></span><span id="wbemmof_e_null_array_elem"></span>**WBEMMOF\_E\_NULL\_ARRAY\_ELEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-662">2147762208 (0x80044020)</span><span class="sxs-lookup"><span data-stu-id="cca14-662">2147762208 (0x80044020)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-663">Les éléments NULL d’un tableau ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="cca14-663">NULL elements in an array are not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-664"><span id="WBEMMOF_E_DUPLICATE_QUALIFIER"></span><span id="wbemmof_e_duplicate_qualifier"></span>**\_QUALIFICATEUR WBEMMOF E \_ dupliqué \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-664"><span id="WBEMMOF_E_DUPLICATE_QUALIFIER"></span><span id="wbemmof_e_duplicate_qualifier"></span>**WBEMMOF\_E\_DUPLICATE\_QUALIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-665">2147762209 (0x80044021)</span><span class="sxs-lookup"><span data-stu-id="cca14-665">2147762209 (0x80044021)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-666">Le qualificateur a été utilisé plusieurs fois sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="cca14-666">Qualifier was used more than once on the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-667"><span id="WBEMMOF_E_EXPECTED_FLAVOR_TYPE"></span><span id="wbemmof_e_expected_flavor_type"></span>**WBEMMOF \_ E \_ \_ type de version attendu \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-667"><span id="WBEMMOF_E_EXPECTED_FLAVOR_TYPE"></span><span id="wbemmof_e_expected_flavor_type"></span>**WBEMMOF\_E\_EXPECTED\_FLAVOR\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-668">2147762210 (0x80044022)</span><span class="sxs-lookup"><span data-stu-id="cca14-668">2147762210 (0x80044022)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-669">Type de version attendu, tel que **ToInstance**, **ToSubClass**, **EnableOverride** ou **DisableOverride**.</span><span class="sxs-lookup"><span data-stu-id="cca14-669">Expected a flavor type such as **ToInstance**, **ToSubClass**, **EnableOverride**, or **DisableOverride**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-670"><span id="WBEMMOF_E_INCOMPATIBLE_FLAVOR_TYPES"></span><span id="wbemmof_e_incompatible_flavor_types"></span>**WBEMMOF \_ E \_ types de version incompatibles \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-670"><span id="WBEMMOF_E_INCOMPATIBLE_FLAVOR_TYPES"></span><span id="wbemmof_e_incompatible_flavor_types"></span>**WBEMMOF\_E\_INCOMPATIBLE\_FLAVOR\_TYPES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-671">2147762211 (0x80044023)</span><span class="sxs-lookup"><span data-stu-id="cca14-671">2147762211 (0x80044023)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-672">La combinaison de **EnableOverride** et de **DisableOverride** sur le même qualificateur n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="cca14-672">Combining **EnableOverride** and **DisableOverride** on same qualifier is not legal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-673"><span id="WBEMMOF_E_MULTIPLE_ALIASES"></span><span id="wbemmof_e_multiple_aliases"></span>**WBEMMOF \_ E \_ \_ alias multiples**</span><span class="sxs-lookup"><span data-stu-id="cca14-673"><span id="WBEMMOF_E_MULTIPLE_ALIASES"></span><span id="wbemmof_e_multiple_aliases"></span>**WBEMMOF\_E\_MULTIPLE\_ALIASES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-674">2147762212 (0x80044024)</span><span class="sxs-lookup"><span data-stu-id="cca14-674">2147762212 (0x80044024)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-675">Un alias ne peut pas être utilisé deux fois.</span><span class="sxs-lookup"><span data-stu-id="cca14-675">An alias cannot be used twice.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-676"><span id="WBEMMOF_E_INCOMPATIBLE_FLAVOR_TYPES2"></span><span id="wbemmof_e_incompatible_flavor_types2"></span>**WBEMMOF \_ E \_ \_ TYPES2 version incompatible \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-676"><span id="WBEMMOF_E_INCOMPATIBLE_FLAVOR_TYPES2"></span><span id="wbemmof_e_incompatible_flavor_types2"></span>**WBEMMOF\_E\_INCOMPATIBLE\_FLAVOR\_TYPES2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-677">2147762213 (0x80044025)</span><span class="sxs-lookup"><span data-stu-id="cca14-677">2147762213 (0x80044025)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-678">La combinaison de **Restricted**, de **ToInstance** ou de **ToSubClass** n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="cca14-678">Combining **Restricted**, and **ToInstance** or **ToSubClass** is not legal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-679"><span id="WBEMMOF_E_NO_ARRAYS_RETURNED"></span><span id="wbemmof_e_no_arrays_returned"></span>**WBEMMOF \_ E \_ aucun \_ tableau \_ retourné**</span><span class="sxs-lookup"><span data-stu-id="cca14-679"><span id="WBEMMOF_E_NO_ARRAYS_RETURNED"></span><span id="wbemmof_e_no_arrays_returned"></span>**WBEMMOF\_E\_NO\_ARRAYS\_RETURNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-680">2147762214 (0x80044026)</span><span class="sxs-lookup"><span data-stu-id="cca14-680">2147762214 (0x80044026)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-681">Les méthodes ne peuvent pas retourner de valeurs de tableau.</span><span class="sxs-lookup"><span data-stu-id="cca14-681">Methods cannot return array values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-682"><span id="WBEMMOF_E_MUST_BE_IN_OR_OUT"></span><span id="wbemmof_e_must_be_in_or_out"></span>**WBEMMOF \_ E \_ doit \_ être \_ in \_ ou \_ out**</span><span class="sxs-lookup"><span data-stu-id="cca14-682"><span id="WBEMMOF_E_MUST_BE_IN_OR_OUT"></span><span id="wbemmof_e_must_be_in_or_out"></span>**WBEMMOF\_E\_MUST\_BE\_IN\_OR\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-683">2147762215 (0x80044027)</span><span class="sxs-lookup"><span data-stu-id="cca14-683">2147762215 (0x80044027)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-684">Les arguments doivent avoir un qualificateur **in** ou **out** .</span><span class="sxs-lookup"><span data-stu-id="cca14-684">Arguments must have an **In** or **Out** qualifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-685"><span id="WBEMMOF_E_INVALID_FLAGS_SYNTAX"></span><span id="wbemmof_e_invalid_flags_syntax"></span>**WBEMMOF \_ E \_ \_ syntaxe des indicateurs non valides \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-685"><span id="WBEMMOF_E_INVALID_FLAGS_SYNTAX"></span><span id="wbemmof_e_invalid_flags_syntax"></span>**WBEMMOF\_E\_INVALID\_FLAGS\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-686">2147762216 (0x80044028)</span><span class="sxs-lookup"><span data-stu-id="cca14-686">2147762216 (0x80044028)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-687">La syntaxe des indicateurs n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="cca14-687">Flags syntax is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-688"><span id="WBEMMOF_E_EXPECTED_BRACE_OR_BAD_TYPE"></span><span id="wbemmof_e_expected_brace_or_bad_type"></span>**WBEMMOF \_ E \_ \_ accolade attendue \_ ou \_ type incorrect \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-688"><span id="WBEMMOF_E_EXPECTED_BRACE_OR_BAD_TYPE"></span><span id="wbemmof_e_expected_brace_or_bad_type"></span>**WBEMMOF\_E\_EXPECTED\_BRACE\_OR\_BAD\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-689">2147762217 (0x80044029)</span><span class="sxs-lookup"><span data-stu-id="cca14-689">2147762217 (0x80044029)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-690">La dernière accolade et le point-virgule pour une classe sont manquants.</span><span class="sxs-lookup"><span data-stu-id="cca14-690">The final brace and semi-colon for a class are missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-691"><span id="WBEMMOF_E_UNSUPPORTED_CIMV22_QUAL_VALUE"></span><span id="wbemmof_e_unsupported_cimv22_qual_value"></span>**WBEMMOF \_ E \_ valeur de la \_ Qualys CIMV22 non prise en charge \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-691"><span id="WBEMMOF_E_UNSUPPORTED_CIMV22_QUAL_VALUE"></span><span id="wbemmof_e_unsupported_cimv22_qual_value"></span>**WBEMMOF\_E\_UNSUPPORTED\_CIMV22\_QUAL\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-692">2147762218 (0x8004402A)</span><span class="sxs-lookup"><span data-stu-id="cca14-692">2147762218 (0x8004402A)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-693">Une fonctionnalité CIM version 2,2 n’est pas prise en charge pour une valeur de qualificateur.</span><span class="sxs-lookup"><span data-stu-id="cca14-693">A CIM version 2.2 feature is not supported for a qualifier value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-694"><span id="WBEMMOF_E_UNSUPPORTED_CIMV22_DATA_TYPE"></span><span id="wbemmof_e_unsupported_cimv22_data_type"></span>**WBEMMOF \_ E \_ \_ type de données CIMV22 \_ non pris en charge \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-694"><span id="WBEMMOF_E_UNSUPPORTED_CIMV22_DATA_TYPE"></span><span id="wbemmof_e_unsupported_cimv22_data_type"></span>**WBEMMOF\_E\_UNSUPPORTED\_CIMV22\_DATA\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-695">2147762219 (0x8004402B)</span><span class="sxs-lookup"><span data-stu-id="cca14-695">2147762219 (0x8004402B)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-696">Le type de données CIM version 2,2 n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="cca14-696">The CIM version 2.2 data type is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-697"><span id="WBEMMOF_E_INVALID_DELETEINSTANCE_SYNTAX"></span><span id="wbemmof_e_invalid_deleteinstance_syntax"></span>**WBEMMOF \_ E \_ \_ syntaxe DELETEINSTANCE non valide \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-697"><span id="WBEMMOF_E_INVALID_DELETEINSTANCE_SYNTAX"></span><span id="wbemmof_e_invalid_deleteinstance_syntax"></span>**WBEMMOF\_E\_INVALID\_DELETEINSTANCE\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-698">2147762220 (0x8004402C)</span><span class="sxs-lookup"><span data-stu-id="cca14-698">2147762220 (0x8004402C)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-699">La syntaxe de suppression d’instance n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="cca14-699">The delete instance syntax is not valid.</span></span> <span data-ttu-id="cca14-700">Elle doit être `#pragma DeleteInstance("instancepath", FAIL|NOFAIL)`</span><span class="sxs-lookup"><span data-stu-id="cca14-700">It should be `#pragma DeleteInstance("instancepath", FAIL|NOFAIL)`</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-701"><span id="WBEMMOF_E_INVALID_QUALIFIER_SYNTAX"></span><span id="wbemmof_e_invalid_qualifier_syntax"></span>**WBEMMOF \_ E \_ syntaxe de qualificateur non valide \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-701"><span id="WBEMMOF_E_INVALID_QUALIFIER_SYNTAX"></span><span id="wbemmof_e_invalid_qualifier_syntax"></span>**WBEMMOF\_E\_INVALID\_QUALIFIER\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-702">2147762221 (0x8004402D)</span><span class="sxs-lookup"><span data-stu-id="cca14-702">2147762221 (0x8004402D)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-703">La syntaxe du qualificateur n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="cca14-703">The qualifier syntax is not valid.</span></span> <span data-ttu-id="cca14-704">Elle doit avoir la valeur `qualifiername:type=value,scope(class|instance), flavorname`.</span><span class="sxs-lookup"><span data-stu-id="cca14-704">It should be `qualifiername:type=value,scope(class|instance), flavorname`.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-705"><span id="WBEMMOF_E_QUALIFIER_USED_OUTSIDE_SCOPE"></span><span id="wbemmof_e_qualifier_used_outside_scope"></span>**\_QUALIFICATEUR WBEMMOF E \_ \_ utilisé \_ en dehors de l' \_ étendue**</span><span class="sxs-lookup"><span data-stu-id="cca14-705"><span id="WBEMMOF_E_QUALIFIER_USED_OUTSIDE_SCOPE"></span><span id="wbemmof_e_qualifier_used_outside_scope"></span>**WBEMMOF\_E\_QUALIFIER\_USED\_OUTSIDE\_SCOPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-706">2147762222 (0x8004402E)</span><span class="sxs-lookup"><span data-stu-id="cca14-706">2147762222 (0x8004402E)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-707">Le qualificateur est utilisé en dehors de son étendue.</span><span class="sxs-lookup"><span data-stu-id="cca14-707">The qualifier is used outside of its scope.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-708"><span id="WBEMMOF_E_ERROR_CREATING_TEMP_FILE"></span><span id="wbemmof_e_error_creating_temp_file"></span>**WBEMMOF \_ E \_ erreur lors de la \_ création du \_ \_ fichier temporaire**</span><span class="sxs-lookup"><span data-stu-id="cca14-708"><span id="WBEMMOF_E_ERROR_CREATING_TEMP_FILE"></span><span id="wbemmof_e_error_creating_temp_file"></span>**WBEMMOF\_E\_ERROR\_CREATING\_TEMP\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-709">2147762223 (0x8004402F)</span><span class="sxs-lookup"><span data-stu-id="cca14-709">2147762223 (0x8004402F)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-710">Erreur lors de la création du fichier temporaire.</span><span class="sxs-lookup"><span data-stu-id="cca14-710">Error creating temporary file.</span></span> <span data-ttu-id="cca14-711">Le fichier temporaire est une étape intermédiaire de la compilation MOF.</span><span class="sxs-lookup"><span data-stu-id="cca14-711">The temporary file is an intermediate stage in the MOF compilation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-712"><span id="WBEMMOF_E_ERROR_INVALID_INCLUDE_FILE"></span><span id="wbemmof_e_error_invalid_include_file"></span>**\_erreur WBEMMOF \_ E \_ \_ fichier include non valide \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-712"><span id="WBEMMOF_E_ERROR_INVALID_INCLUDE_FILE"></span><span id="wbemmof_e_error_invalid_include_file"></span>**WBEMMOF\_E\_ERROR\_INVALID\_INCLUDE\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-713">2147762224 (0x80044030)</span><span class="sxs-lookup"><span data-stu-id="cca14-713">2147762224 (0x80044030)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-714">Un fichier inclus dans le fichier MOF par la commande de préprocesseur n’est pas valide. [ \# ](-include.md)</span><span class="sxs-lookup"><span data-stu-id="cca14-714">A file included in the MOF by the preprocessor command [\#include](-include.md) is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cca14-715"><span id="WBEMMOF_E_INVALID_DELETECLASS_SYNTAX"></span><span id="wbemmof_e_invalid_deleteclass_syntax"></span>**WBEMMOF \_ E \_ \_ syntaxe DELETECLASS non valide \_**</span><span class="sxs-lookup"><span data-stu-id="cca14-715"><span id="WBEMMOF_E_INVALID_DELETECLASS_SYNTAX"></span><span id="wbemmof_e_invalid_deleteclass_syntax"></span>**WBEMMOF\_E\_INVALID\_DELETECLASS\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca14-716">2147762225 (0x80044031)</span><span class="sxs-lookup"><span data-stu-id="cca14-716">2147762225 (0x80044031)</span></span>
</dt> <dt>



<span data-ttu-id="cca14-717">La syntaxe des commandes de préprocesseur [ \# pragma DeleteInstance](pragma-deleteinstance.md) ou [ \# pragma deleteclass](pragma-deleteclass.md) n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="cca14-717">The syntax for the preprocessor commands [\#pragma deleteinstance](pragma-deleteinstance.md) or [\#pragma deleteclass](pragma-deleteclass.md) is not valid.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cca14-718">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cca14-718">Requirements</span></span>



| <span data-ttu-id="cca14-719">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cca14-719">Requirement</span></span> | <span data-ttu-id="cca14-720">Valeur</span><span class="sxs-lookup"><span data-stu-id="cca14-720">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cca14-721">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cca14-721">Minimum supported client</span></span><br/> | <span data-ttu-id="cca14-722">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cca14-722">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="cca14-723">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cca14-723">Minimum supported server</span></span><br/> | <span data-ttu-id="cca14-724">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cca14-724">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="cca14-725">En-tête</span><span class="sxs-lookup"><span data-stu-id="cca14-725">Header</span></span><br/>                   | <dl> <span data-ttu-id="cca14-726"><dt>WbemCli. h</dt></span><span class="sxs-lookup"><span data-stu-id="cca14-726"><dt>WbemCli.h</dt></span></span> </dl>   |
| <span data-ttu-id="cca14-727">MIDL</span><span class="sxs-lookup"><span data-stu-id="cca14-727">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cca14-728"><dt>WbemCli. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cca14-728"><dt>WbemCli.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cca14-729">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cca14-729">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cca14-730">Codes de retour WMI</span><span class="sxs-lookup"><span data-stu-id="cca14-730">WMI Return Codes</span></span>](wmi-return-codes.md)
</dt> </dl>

 

