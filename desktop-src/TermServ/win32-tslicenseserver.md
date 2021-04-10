---
title: Classe Win32_TSLicenseServer
description: Fournit des méthodes et des propriétés permettant d’afficher et de configurer des licences Bureau à distance (licences des services Bureau à distance) sur un serveur de licences Bureau à distance.
ms.assetid: 699ddd9f-a91a-450c-b131-a7471252a4cc
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseServer de la classe Services Bureau à distance
- Win32_TSLicenseServer de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer
- Win32_TSLicenseServer.FirstName
- Win32_TSLicenseServer.LastName
- Win32_TSLicenseServer.Company
- Win32_TSLicenseServer.CountryRegion
- Win32_TSLicenseServer.eMail
- Win32_TSLicenseServer.OrgUnit
- Win32_TSLicenseServer.Address
- Win32_TSLicenseServer.City
- Win32_TSLicenseServer.State
- Win32_TSLicenseServer.PostalCode
- Win32_TSLicenseServer.ServerRole
- Win32_TSLicenseServer.DatabasePath
- Win32_TSLicenseServer.ProductId
- Win32_TSLicenseServer.Version
- Win32_TSLicenseServer.VersionNumber
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31951b943723e620414b2f714327db8c786f9ab9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942406"
---
# <a name="win32_tslicenseserver-class"></a><span data-ttu-id="fa72d-105">\_Classe TSLicenseServer Win32</span><span class="sxs-lookup"><span data-stu-id="fa72d-105">Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="fa72d-106">Fournit des méthodes et des propriétés permettant d’afficher et de configurer des licences Bureau à distance (licences des services Bureau à distance) sur un serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="fa72d-106">Provides methods and properties to view and configure Remote Desktop Licensing (RD Licensing) on a Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa72d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa72d-107">Syntax</span></span>

``` syntax
[singleton, dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSLicenseServer
{
  string FirstName;
  string LastName;
  string Company;
  string CountryRegion;
  string eMail;
  string OrgUnit;
  string Address;
  string City;
  string State;
  string PostalCode;
  uint32 ServerRole;
  string DatabasePath;
  string ProductId;
  string Version;
  string VersionNumber;
};
```

## <a name="members"></a><span data-ttu-id="fa72d-108">Membres</span><span class="sxs-lookup"><span data-stu-id="fa72d-108">Members</span></span>

<span data-ttu-id="fa72d-109">La classe **Win32 \_ TSLicenseServer** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fa72d-109">The **Win32\_TSLicenseServer** class has these types of members:</span></span>

-   [<span data-ttu-id="fa72d-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="fa72d-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="fa72d-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fa72d-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="fa72d-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="fa72d-112">Methods</span></span>

<span data-ttu-id="fa72d-113">La classe **Win32 \_ TSLicenseServer** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="fa72d-113">The **Win32\_TSLicenseServer** class has these methods.</span></span>



| <span data-ttu-id="fa72d-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="fa72d-114">Method</span></span>                                                                                   | <span data-ttu-id="fa72d-115">Description</span><span class="sxs-lookup"><span data-stu-id="fa72d-115">Description</span></span>                                                                                                                                                                                                                                   |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa72d-116">**ActivateServer**</span><span class="sxs-lookup"><span data-stu-id="fa72d-116">**ActivateServer**</span></span>](activateserver-win32-tslicenseserver.md)                           | <span data-ttu-id="fa72d-117">Active le serveur de licences Bureau à distance à l’aide d’un ID de serveur de licences Bureau à distance qui est obtenu sur le téléphone ou sur Internet.</span><span class="sxs-lookup"><span data-stu-id="fa72d-117">Activates the Remote Desktop license server by using a Remote Desktop license server ID that is obtained over the phone or the Internet.</span></span><br/>                                                                                           |
| [<span data-ttu-id="fa72d-118">**ActivateServerAutomatic**</span><span class="sxs-lookup"><span data-stu-id="fa72d-118">**ActivateServerAutomatic**</span></span>](activateserverautomatic-win32-tslicenseserver.md)         | <span data-ttu-id="fa72d-119">Active automatiquement le serveur de licences Bureau à distance via Internet.</span><span class="sxs-lookup"><span data-stu-id="fa72d-119">Activates the Remote Desktop license server automatically over the Internet.</span></span> <span data-ttu-id="fa72d-120">Les propriétés **FirstName**, **LastName**, **Company** et **PaysRégion** ne doivent pas être vides lorsque cette méthode est appelée, sinon la méthode échoue.</span><span class="sxs-lookup"><span data-stu-id="fa72d-120">The **FirstName**, **LastName**, **Company**, and **CountryRegion** properties must not be empty when this method is called, or the method will fail.</span></span><br/> |
| [<span data-ttu-id="fa72d-121">**AddLStoTSLSGroup**</span><span class="sxs-lookup"><span data-stu-id="fa72d-121">**AddLStoTSLSGroup**</span></span>](addlstotslsgroup-win32-tslicenseserver.md)                       | <span data-ttu-id="fa72d-122">Ajoute le Bureau à distance serveur de licences au groupe serveurs de licences Bureau à distance sur un contrôleur de domaine dans le même domaine que le serveur de licences.</span><span class="sxs-lookup"><span data-stu-id="fa72d-122">Adds the Remote Desktop license server to the Remote Desktop License Servers group on a domain controller in the same domain as the license server.</span></span><br/>                                                                                |
| [<span data-ttu-id="fa72d-123">**ChangeRole**</span><span class="sxs-lookup"><span data-stu-id="fa72d-123">**ChangeRole**</span></span>](changerole-win32-tslicenseserver.md)                                   | <span data-ttu-id="fa72d-124">Modifie l’étendue de la découverte du serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="fa72d-124">Changes the discovery scope of the Remote Desktop license server.</span></span><br/>                                                                                                                                                                  |
| [<span data-ttu-id="fa72d-125">**CreateTSCGroup**</span><span class="sxs-lookup"><span data-stu-id="fa72d-125">**CreateTSCGroup**</span></span>](createtscgroup-win32-tslicenseserver.md)                           | <span data-ttu-id="fa72d-126">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="fa72d-126">This method is not supported.</span></span><br/> <span data-ttu-id="fa72d-127">**Windows server 2008 R2 et Windows server 2008 :** Crée le groupe local ordinateurs Terminal Server sur le serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="fa72d-127">**Windows Server 2008 R2 and Windows Server 2008:** Creates the Terminal Server Computers local group on the Remote Desktop license server.</span></span><br/>                                               |
| [<span data-ttu-id="fa72d-128">**DeactivateServer**</span><span class="sxs-lookup"><span data-stu-id="fa72d-128">**DeactivateServer**</span></span>](deactivateserver-win32-tslicenseserver.md)                       | <span data-ttu-id="fa72d-129">Désactive le serveur de licences Bureau à distance à l’aide d’un code de confirmation reçu sur le téléphone.</span><span class="sxs-lookup"><span data-stu-id="fa72d-129">Deactivates the Remote Desktop license server by using a confirmation code that is received over the phone.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="fa72d-130">**DeactivateServerAutomatic**</span><span class="sxs-lookup"><span data-stu-id="fa72d-130">**DeactivateServerAutomatic**</span></span>](deactivateserverautomatic-win32-tslicenseserver.md)     | <span data-ttu-id="fa72d-131">Désactive le serveur de licences Bureau à distance sur Internet.</span><span class="sxs-lookup"><span data-stu-id="fa72d-131">Deactivates the Remote Desktop license server over the Internet.</span></span> <span data-ttu-id="fa72d-132">Les propriétés **FirstName** et **LastName** ne doivent pas être vides lorsque cette méthode est appelée, sinon la méthode échoue.</span><span class="sxs-lookup"><span data-stu-id="fa72d-132">The **FirstName** and **LastName** properties must not be empty when this method is called, or the method will fail.</span></span><br/>                                              |
| [<span data-ttu-id="fa72d-133">**GetActivationStatus**</span><span class="sxs-lookup"><span data-stu-id="fa72d-133">**GetActivationStatus**</span></span>](getactivationstatus-win32-tslicenseserver.md)                 | <span data-ttu-id="fa72d-134">Récupère l’état d’activation actuel.</span><span class="sxs-lookup"><span data-stu-id="fa72d-134">Retrieves the current activation status.</span></span><br/>                                                                                                                                                                                           |
| [<span data-ttu-id="fa72d-135">**GetLicenseServerId**</span><span class="sxs-lookup"><span data-stu-id="fa72d-135">**GetLicenseServerId**</span></span>](getlicenseserverid-win32-tslicenseserver.md)                   | <span data-ttu-id="fa72d-136">Récupère un Bureau à distance ID du serveur de licences si le serveur est actuellement activé.</span><span class="sxs-lookup"><span data-stu-id="fa72d-136">Retrieves a Remote Desktop license server ID if the server is currently activated.</span></span><br/>                                                                                                                                                 |
| [<span data-ttu-id="fa72d-137">**IsLSinTSLSGroup**</span><span class="sxs-lookup"><span data-stu-id="fa72d-137">**IsLSinTSLSGroup**</span></span>](islsintslsgroup-win32-tslicenseserver.md)                         | <span data-ttu-id="fa72d-138">Récupère si le Bureau à distance serveur de licences est membre du groupe serveurs de licences Bureau à distance sur un contrôleur de domaine dans un domaine donné.</span><span class="sxs-lookup"><span data-stu-id="fa72d-138">Retrieves whether the Remote Desktop license server is a member of the Remote Desktop License Servers group on a domain controller in a given domain.</span></span><br/>                                                                              |
| [<span data-ttu-id="fa72d-139">**IsLSonDC**</span><span class="sxs-lookup"><span data-stu-id="fa72d-139">**IsLSonDC**</span></span>](islsondc-win32-tslicenseserver.md)                                       | <span data-ttu-id="fa72d-140">Récupère si le gestionnaire de licences des services Bureau à distance est installé sur un contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="fa72d-140">Retrieves whether RD Licensing is installed on a domain controller.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="fa72d-141">**IsLSPreventUpgradeGPEnabled**</span><span class="sxs-lookup"><span data-stu-id="fa72d-141">**IsLSPreventUpgradeGPEnabled**</span></span>](islspreventupgradegpenabled-win32-tslicenseserver.md) | <span data-ttu-id="fa72d-142">Récupère si le paramètre de stratégie de groupe « empêcher la mise à niveau de licence » est activé sur le serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="fa72d-142">Retrieves whether the "prevent license upgrade" group policy setting is enabled on the Remote Desktop license server.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="fa72d-143">**IsLSPublished**</span><span class="sxs-lookup"><span data-stu-id="fa72d-143">**IsLSPublished**</span></span>](islspublished-win32-tslicenseserver.md)                             | <span data-ttu-id="fa72d-144">Récupère si le serveur de licences Bureau à distance est publié dans Active Directory Domain Services (AD DS).</span><span class="sxs-lookup"><span data-stu-id="fa72d-144">Retrieves whether the Remote Desktop license server is published in Active Directory Domain Services (AD DS).</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="fa72d-145">**IsLSRegisteredToSCP**</span><span class="sxs-lookup"><span data-stu-id="fa72d-145">**IsLSRegisteredToSCP**</span></span>](win32-tslicenseserver-islsregisteredtoscp.md)                 | <span data-ttu-id="fa72d-146">Récupère si le serveur de licences Bureau à distance est inscrit en tant que point de connexion de service dans Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="fa72d-146">Retrieves whether the Remote Desktop license server is registered as a service connection point in Active Directory Domain Services.</span></span><br/>                                                                                               |
| [<span data-ttu-id="fa72d-147">**IsLSSecGrpGPEnabled**</span><span class="sxs-lookup"><span data-stu-id="fa72d-147">**IsLSSecGrpGPEnabled**</span></span>](islssecgrpgpenabled-win32-tslicenseserver.md)                 | <span data-ttu-id="fa72d-148">Récupère si le paramètre de stratégie de groupe « Groupe de sécurité du serveur de licences » est activé sur le serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="fa72d-148">Retrieves whether the "license server security group" group policy setting is enabled on the Remote Desktop license server.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="fa72d-149">**IsSecureAccessAllowed**</span><span class="sxs-lookup"><span data-stu-id="fa72d-149">**IsSecureAccessAllowed**</span></span>](issecureaccessallowed-win32-tslicenseserver.md)             | <span data-ttu-id="fa72d-150">Récupère une valeur indiquant si un serveur hôte de session Bureau à distance est autorisé à demander Services Bureau à distance licences d’accès client (CAL RDS) à partir du serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="fa72d-150">Retrieves whether an RD Session Host server is allowed to request Remote Desktop Services client access licenses (RDS CALs) from the Remote Desktop license server.</span></span><br/>                                                                |
| [<span data-ttu-id="fa72d-151">**IsTSCGroupPresent**</span><span class="sxs-lookup"><span data-stu-id="fa72d-151">**IsTSCGroupPresent**</span></span>](istscgrouppresent-win32-tslicenseserver.md)                     | <span data-ttu-id="fa72d-152">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="fa72d-152">This method is not supported.</span></span><br/> <span data-ttu-id="fa72d-153">**Windows server 2008 R2 et Windows server 2008 :** Récupère si le groupe local ordinateurs Terminal Server existe sur le serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="fa72d-153">**Windows Server 2008 R2 and Windows Server 2008:** Retrieves whether the Terminal Server Computers local group exists on the Remote Desktop license server.</span></span><br/>                              |
| [<span data-ttu-id="fa72d-154">**IsTSinTSCGroup**</span><span class="sxs-lookup"><span data-stu-id="fa72d-154">**IsTSinTSCGroup**</span></span>](istsintscgroup-win32-tslicenseserver.md)                           | <span data-ttu-id="fa72d-155">Récupère une valeur qui détermine si un serveur hôte de session Bureau à distance est membre du groupe local ordinateurs Terminal Server sur le serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="fa72d-155">Retrieves whether an RD Session Host server is a member of the Terminal Server Computers local group on the Remote Desktop license server.</span></span><br/>                                                                                         |
| [<span data-ttu-id="fa72d-156">**PublishLS**</span><span class="sxs-lookup"><span data-stu-id="fa72d-156">**PublishLS**</span></span>](publishls-win32-tslicenseserver.md)                                     | <span data-ttu-id="fa72d-157">Publie le serveur de licences Bureau à distance dans AD DS.</span><span class="sxs-lookup"><span data-stu-id="fa72d-157">Publishes the Remote Desktop license server in AD DS.</span></span><br/>                                                                                                                                                                              |
| [<span data-ttu-id="fa72d-158">**ReactivateServer**</span><span class="sxs-lookup"><span data-stu-id="fa72d-158">**ReactivateServer**</span></span>](reactivateserver-win32-tslicenseserver.md)                       | <span data-ttu-id="fa72d-159">Réactive le serveur de licences Bureau à distance à l’aide d’un nouvel ID de serveur de licences Bureau à distance qui est obtenu sur le téléphone ou sur Internet.</span><span class="sxs-lookup"><span data-stu-id="fa72d-159">Reactivates the Remote Desktop license server by using a new Remote Desktop license server ID that is obtained over the phone or the Internet.</span></span><br/>                                                                                     |
| [<span data-ttu-id="fa72d-160">**ReactivateServerAutomatic**</span><span class="sxs-lookup"><span data-stu-id="fa72d-160">**ReactivateServerAutomatic**</span></span>](reactivateserverautomatic-win32-tslicenseserver.md)     | <span data-ttu-id="fa72d-161">Réactive le serveur de licences Bureau à distance via Internet.</span><span class="sxs-lookup"><span data-stu-id="fa72d-161">Reactivates the Remote Desktop license server over the Internet.</span></span> <span data-ttu-id="fa72d-162">Les propriétés **FirstName** et **LastName** ne doivent pas être vides lorsque cette méthode est appelée, sinon la méthode échoue.</span><span class="sxs-lookup"><span data-stu-id="fa72d-162">The **FirstName** and **LastName** properties must not be empty when this method is called, or the method will fail.</span></span><br/>                                              |
| [<span data-ttu-id="fa72d-163">**RegisterLSToSCP**</span><span class="sxs-lookup"><span data-stu-id="fa72d-163">**RegisterLSToSCP**</span></span>](win32-tslicenseserver-registerlstoscp.md)                         | <span data-ttu-id="fa72d-164">Inscrit le serveur de licences Bureau à distance en tant que point de connexion de service dans Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="fa72d-164">Registers the Remote Desktop license server as a service connection point in Active Directory Domain Services.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="fa72d-165">**RemoveLSfromTSLSGroup**</span><span class="sxs-lookup"><span data-stu-id="fa72d-165">**RemoveLSfromTSLSGroup**</span></span>](removelsfromtslsgroup-win32-tslicenseserver.md)             | <span data-ttu-id="fa72d-166">Supprime le Bureau à distance serveur de licences du groupe serveurs de licences Bureau à distance sur un contrôleur de domaine dans le même domaine que le serveur de licences.</span><span class="sxs-lookup"><span data-stu-id="fa72d-166">Removes the Remote Desktop license server from the Remote Desktop License Servers group on a domain controller in the same domain as the license server.</span></span><br/>                                                                           |
| [<span data-ttu-id="fa72d-167">**RemoveTSCGroup**</span><span class="sxs-lookup"><span data-stu-id="fa72d-167">**RemoveTSCGroup**</span></span>](removetscgroup-win32-tslicenseserver.md)                           | <span data-ttu-id="fa72d-168">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="fa72d-168">This method is not supported.</span></span><br/> <span data-ttu-id="fa72d-169">**Windows server 2008 R2 et Windows server 2008 :** Supprime le Terminal Server groupe local ordinateurs du serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="fa72d-169">**Windows Server 2008 R2 and Windows Server 2008:** Removes the Terminal Server Computers local group from the Remote Desktop license server.</span></span><br/>                                             |
| [<span data-ttu-id="fa72d-170">**UnpublishLS**</span><span class="sxs-lookup"><span data-stu-id="fa72d-170">**UnpublishLS**</span></span>](unpublishls-win32-tslicenseserver.md)                                 | <span data-ttu-id="fa72d-171">Annule la publication d’un serveur de licences Bureau à distance à partir de AD DS.</span><span class="sxs-lookup"><span data-stu-id="fa72d-171">Unpublishes a Remote Desktop license server from AD DS.</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="fa72d-172">**UnRegisterLSFromSCP**</span><span class="sxs-lookup"><span data-stu-id="fa72d-172">**UnRegisterLSFromSCP**</span></span>](win32-tslicenseserver-unregisterlsfromscp.md)                 | <span data-ttu-id="fa72d-173">Supprime le serveur de licences Bureau à distance comme point de connexion de service dans Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="fa72d-173">Removes the Remote Desktop license server as a service connection point in Active Directory Domain Services.</span></span><br/>                                                                                                                       |



 

### <a name="properties"></a><span data-ttu-id="fa72d-174">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fa72d-174">Properties</span></span>

<span data-ttu-id="fa72d-175">La classe **Win32 \_ TSLicenseServer** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="fa72d-175">The **Win32\_TSLicenseServer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fa72d-176">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="fa72d-176">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa72d-177">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fa72d-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa72d-178">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fa72d-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fa72d-179">Adresse du contact pour le gestionnaire de licences des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="fa72d-179">Street address of the contact for RD Licensing.</span></span> <span data-ttu-id="fa72d-180">Cette propriété est utilisée lorsque la méthode [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) est appelée.</span><span class="sxs-lookup"><span data-stu-id="fa72d-180">This property is used when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) method is called.</span></span> <span data-ttu-id="fa72d-181">(Cette propriété est facultative lors de l’utilisation de la méthode **ActivateServerAutomatic** .)</span><span class="sxs-lookup"><span data-stu-id="fa72d-181">(This property is optional when using the **ActivateServerAutomatic** method.)</span></span>

</dd> <dt>

<span data-ttu-id="fa72d-182">**Ville**</span><span class="sxs-lookup"><span data-stu-id="fa72d-182">**City**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa72d-183">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fa72d-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa72d-184">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fa72d-184">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fa72d-185">Ville du contact pour les licences des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="fa72d-185">City of the contact for RD Licensing.</span></span> <span data-ttu-id="fa72d-186">Cette propriété est utilisée lorsque la méthode [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) est appelée.</span><span class="sxs-lookup"><span data-stu-id="fa72d-186">This property is used when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) method is called.</span></span> <span data-ttu-id="fa72d-187">(Cette propriété est facultative lors de l’utilisation de la méthode **ActivateServerAutomatic** .)</span><span class="sxs-lookup"><span data-stu-id="fa72d-187">(This property is optional when using the **ActivateServerAutomatic** method.)</span></span>

</dd> <dt>

<span data-ttu-id="fa72d-188">**Société**</span><span class="sxs-lookup"><span data-stu-id="fa72d-188">**Company**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa72d-189">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fa72d-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa72d-190">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fa72d-190">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fa72d-191">Société du contact pour les licences des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="fa72d-191">Company of the contact for RD Licensing.</span></span> <span data-ttu-id="fa72d-192">Cette propriété est utilisée (et obligatoire) lorsque la méthode [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) est appelée.</span><span class="sxs-lookup"><span data-stu-id="fa72d-192">This property is used (and required) when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) method is called.</span></span>

</dd> <dt>

<span data-ttu-id="fa72d-193">**Pays**</span><span class="sxs-lookup"><span data-stu-id="fa72d-193">**CountryRegion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa72d-194">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fa72d-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa72d-195">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fa72d-195">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fa72d-196">Pays/région du contact pour les licences des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="fa72d-196">Country/region of the contact for RD Licensing.</span></span> <span data-ttu-id="fa72d-197">Cette propriété est utilisée (et obligatoire) lorsque la méthode [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) est appelée.</span><span class="sxs-lookup"><span data-stu-id="fa72d-197">This property is used (and required) when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) method is called.</span></span>

</dd> <dt>

<span data-ttu-id="fa72d-198">**DatabasePath**</span><span class="sxs-lookup"><span data-stu-id="fa72d-198">**DatabasePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa72d-199">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fa72d-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa72d-200">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fa72d-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa72d-201">Chemin d’accès de la base de données des licences des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="fa72d-201">Path of the RDS Licensing database.</span></span>

</dd> <dt>

<span data-ttu-id="fa72d-202">**Messagerie**</span><span class="sxs-lookup"><span data-stu-id="fa72d-202">**eMail**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa72d-203">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fa72d-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa72d-204">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fa72d-204">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fa72d-205">Adresse de messagerie du contact pour les licences des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="fa72d-205">Email address of the contact for RD Licensing.</span></span> <span data-ttu-id="fa72d-206">Cette propriété est utilisée lorsque les méthodes [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)ou [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) sont appelées.</span><span class="sxs-lookup"><span data-stu-id="fa72d-206">This property is used when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md), or [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) methods are called.</span></span> <span data-ttu-id="fa72d-207">(Cette propriété est facultative pour ces appels de méthode.)</span><span class="sxs-lookup"><span data-stu-id="fa72d-207">(This property is optional for these method calls.)</span></span>

</dd> <dt>

<span data-ttu-id="fa72d-208">**FirstName**</span><span class="sxs-lookup"><span data-stu-id="fa72d-208">**FirstName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa72d-209">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fa72d-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa72d-210">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fa72d-210">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fa72d-211">Prénom du contact pour les licences des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="fa72d-211">First name of the contact for RD Licensing.</span></span> <span data-ttu-id="fa72d-212">Cette propriété est utilisée (et obligatoire) lorsque les méthodes [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)ou [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) sont appelées.</span><span class="sxs-lookup"><span data-stu-id="fa72d-212">This property is used (and required) when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md), or [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) methods are called.</span></span>

</dd> <dt>

<span data-ttu-id="fa72d-213">**LastName**</span><span class="sxs-lookup"><span data-stu-id="fa72d-213">**LastName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa72d-214">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fa72d-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa72d-215">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fa72d-215">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fa72d-216">Nom du contact pour le gestionnaire de licences des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="fa72d-216">Last name of the contact for RD Licensing.</span></span> <span data-ttu-id="fa72d-217">Cette propriété est utilisée (et obligatoire) lorsque les méthodes [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)ou [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) sont appelées.</span><span class="sxs-lookup"><span data-stu-id="fa72d-217">This property is used (and required) when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md), or [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) methods are called.</span></span>

</dd> <dt>

<span data-ttu-id="fa72d-218">**OrgUnit**</span><span class="sxs-lookup"><span data-stu-id="fa72d-218">**OrgUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa72d-219">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fa72d-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa72d-220">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fa72d-220">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fa72d-221">Unité d’organisation du contact pour les licences des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="fa72d-221">Organizational unit of the contact for RD Licensing.</span></span> <span data-ttu-id="fa72d-222">Cette propriété est utilisée lorsque le [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) est appelé.</span><span class="sxs-lookup"><span data-stu-id="fa72d-222">This property is used when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) is called.</span></span> <span data-ttu-id="fa72d-223">(Cette propriété est facultative lors de l’utilisation de la méthode **ActivateServerAutomatic** .)</span><span class="sxs-lookup"><span data-stu-id="fa72d-223">(This property is optional when using the **ActivateServerAutomatic** method.)</span></span>

</dd> <dt>

<span data-ttu-id="fa72d-224">**PostalCode**</span><span class="sxs-lookup"><span data-stu-id="fa72d-224">**PostalCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa72d-225">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fa72d-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa72d-226">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fa72d-226">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fa72d-227">Code postal du contact pour les licences des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="fa72d-227">Postal code of the contact for RD Licensing.</span></span> <span data-ttu-id="fa72d-228">Cette propriété est utilisée lorsque la méthode [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) est appelée.</span><span class="sxs-lookup"><span data-stu-id="fa72d-228">This property is used when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) method is called.</span></span> <span data-ttu-id="fa72d-229">(Cette propriété est facultative lors de l’utilisation de la méthode **ActivateServerAutomatic** .)</span><span class="sxs-lookup"><span data-stu-id="fa72d-229">(This property is optional when using the **ActivateServerAutomatic** method.)</span></span>

</dd> <dt>

<span data-ttu-id="fa72d-230">**ProductId**</span><span class="sxs-lookup"><span data-stu-id="fa72d-230">**ProductId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa72d-231">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fa72d-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa72d-232">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fa72d-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa72d-233">ID de produit du serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="fa72d-233">Product ID of the Remote Desktop license server.</span></span>

</dd> <dt>

<span data-ttu-id="fa72d-234">**ServerRole**</span><span class="sxs-lookup"><span data-stu-id="fa72d-234">**ServerRole**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa72d-235">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fa72d-235">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fa72d-236">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fa72d-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa72d-237">Décrit l’étendue de la gestion de licences pour le Bureau à distance serveur de licences au sein de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="fa72d-237">Describes the licensing scope for the Remote Desktop license server within the organization.</span></span>

<dt>

<span data-ttu-id="fa72d-238">0</span><span class="sxs-lookup"><span data-stu-id="fa72d-238">0</span></span>
</dt> <dd>

<span data-ttu-id="fa72d-239">Les serveurs hôtes de session Bureau à distance dans le même groupe de travail peuvent découvrir le serveur de licences.</span><span class="sxs-lookup"><span data-stu-id="fa72d-239">RD Session Host servers in the same workgroup can discover the license server.</span></span>

</dd> <dt>

<span data-ttu-id="fa72d-240">1</span><span class="sxs-lookup"><span data-stu-id="fa72d-240">1</span></span>
</dt> <dd>

<span data-ttu-id="fa72d-241">Les serveurs hôtes de session Bureau à distance dans le même domaine peuvent découvrir le serveur de licences.</span><span class="sxs-lookup"><span data-stu-id="fa72d-241">RD Session Host servers in the same domain can discover the license server.</span></span>

</dd> <dt>

<span data-ttu-id="fa72d-242">2</span><span class="sxs-lookup"><span data-stu-id="fa72d-242">2</span></span>
</dt> <dd>

<span data-ttu-id="fa72d-243">Les serveurs hôtes de session Bureau à distance de plusieurs domaines de la même forêt peuvent découvrir le serveur de licences.</span><span class="sxs-lookup"><span data-stu-id="fa72d-243">RD Session Host servers from multiple domains in the same forest can discover the license server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fa72d-244">**State**</span><span class="sxs-lookup"><span data-stu-id="fa72d-244">**State**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa72d-245">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fa72d-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa72d-246">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fa72d-246">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fa72d-247">État du contact pour le gestionnaire de licences des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="fa72d-247">State of the contact for RD Licensing.</span></span> <span data-ttu-id="fa72d-248">Cette propriété est utilisée lorsque la méthode [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) est appelée.</span><span class="sxs-lookup"><span data-stu-id="fa72d-248">This property is used when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) method is called.</span></span> <span data-ttu-id="fa72d-249">(Cette propriété est facultative lors de l’utilisation de la méthode **ActivateServerAutomatic** .)</span><span class="sxs-lookup"><span data-stu-id="fa72d-249">(This property is optional when using the **ActivateServerAutomatic** method.)</span></span>

</dd> <dt>

<span data-ttu-id="fa72d-250">**Version**</span><span class="sxs-lookup"><span data-stu-id="fa72d-250">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa72d-251">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fa72d-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa72d-252">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fa72d-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa72d-253">Version du serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="fa72d-253">Version of the Remote Desktop license server.</span></span>

</dd> <dt>

<span data-ttu-id="fa72d-254">**NuméroVersion**</span><span class="sxs-lookup"><span data-stu-id="fa72d-254">**VersionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa72d-255">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fa72d-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa72d-256">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fa72d-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa72d-257">Numéro de version du serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="fa72d-257">Version number of the Remote Desktop license server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fa72d-258">Notes</span><span class="sxs-lookup"><span data-stu-id="fa72d-258">Remarks</span></span>

<span data-ttu-id="fa72d-259">Cette classe est une classe [Singleton](/windows/desktop/WmiSdk/standard-wmi-qualifiers) et ne peut avoir qu’une seule instance.</span><span class="sxs-lookup"><span data-stu-id="fa72d-259">This class is a [singleton](/windows/desktop/WmiSdk/standard-wmi-qualifiers) class and can have only one instance.</span></span> <span data-ttu-id="fa72d-260">Toutes les méthodes contenues dans cette classe sont statiques.</span><span class="sxs-lookup"><span data-stu-id="fa72d-260">All of the methods contained within this class are static.</span></span>

<span data-ttu-id="fa72d-261">Pour utiliser cette classe, vous devez être membre du groupe administrateurs.</span><span class="sxs-lookup"><span data-stu-id="fa72d-261">You must be a member of the Administrators group to use this class.</span></span> <span data-ttu-id="fa72d-262">Si l’appelant n’est pas membre du groupe administrateurs, les propriétés retournées sont vides.</span><span class="sxs-lookup"><span data-stu-id="fa72d-262">If the caller is not a member of the Administrators group, the properties returned will be empty.</span></span>

<span data-ttu-id="fa72d-263">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="fa72d-263">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="fa72d-264">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="fa72d-264">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="fa72d-265">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="fa72d-265">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="fa72d-266">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="fa72d-266">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="fa72d-267">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fa72d-267">Requirements</span></span>



| <span data-ttu-id="fa72d-268">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fa72d-268">Requirement</span></span> | <span data-ttu-id="fa72d-269">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa72d-269">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa72d-270">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa72d-270">Minimum supported client</span></span><br/> | <span data-ttu-id="fa72d-271">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa72d-271">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="fa72d-272">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa72d-272">Minimum supported server</span></span><br/> | <span data-ttu-id="fa72d-273">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fa72d-273">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="fa72d-274">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fa72d-274">Namespace</span></span><br/>                | <span data-ttu-id="fa72d-275">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="fa72d-275">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="fa72d-276">MOF</span><span class="sxs-lookup"><span data-stu-id="fa72d-276">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fa72d-277"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fa72d-277"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="fa72d-278">DLL</span><span class="sxs-lookup"><span data-stu-id="fa72d-278">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa72d-279"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa72d-279"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa72d-280">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa72d-280">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa72d-281">**\_TSIssuedLicense Win32**</span><span class="sxs-lookup"><span data-stu-id="fa72d-281">**Win32\_TSIssuedLicense**</span></span>](win32-tsissuedlicense.md)
</dt> <dt>

[<span data-ttu-id="fa72d-282">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="fa72d-282">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> <dt>

[<span data-ttu-id="fa72d-283">**\_TSLicenseReport Win32**</span><span class="sxs-lookup"><span data-stu-id="fa72d-283">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="fa72d-284">**\_TSLicenseReportEntry Win32**</span><span class="sxs-lookup"><span data-stu-id="fa72d-284">**Win32\_TSLicenseReportEntry**</span></span>](win32-tslicensereportentry.md)
</dt> </dl>

 

