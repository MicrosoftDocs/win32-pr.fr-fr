---
title: Classe MDM_ClientCertificateInstall_Install03
description: La \_ classe ClientCertificateInstall \_ Install03 MDM permet à l’entreprise de définir l’installation des certificats clients.
ms.assetid: 0083e54c-e621-47da-a20d-17c8bbf7dd3a
keywords:
- Classe MDM_ClientCertificateInstall_Install03
- Classe MDM_ClientCertificateInstall_Install03, Description
topic_type:
- apiref
api_name:
- MDM_ClientCertificateInstall_Install03
- MDM_ClientCertificateInstall_Install03.InstanceID
- MDM_ClientCertificateInstall_Install03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04ac690808551e05d6ceba4f3c84bcaa521d4d01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105019"
---
# <a name="mdm_clientcertificateinstall_install03-class"></a><span data-ttu-id="035cd-105">\_ \_ Classe INSTALL03 ClientCertificateInstall MDM</span><span class="sxs-lookup"><span data-stu-id="035cd-105">MDM\_ClientCertificateInstall\_Install03 class</span></span>

<span data-ttu-id="035cd-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="035cd-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="035cd-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="035cd-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="035cd-108">La **classe \_ ClientCertificateInstall \_ Install03 MDM** permet à l’entreprise de définir l’installation des certificats clients. Obligatoire pour l’inscription de certificats SCEP.</span><span class="sxs-lookup"><span data-stu-id="035cd-108">The **MDM\_ClientCertificateInstall\_Install03** class enables the enterprise to set the installation of client certificates.Required for SCEP certificate enrollment.</span></span> <span data-ttu-id="035cd-109">Nœud parent pour grouper le certificat SCEP demande d’installation associée.</span><span class="sxs-lookup"><span data-stu-id="035cd-109">Parent node to group SCEP cert install related request.</span></span>

> [!Note]  
> <span data-ttu-id="035cd-110">Bien que les nœuds enfants sous install prennent en charge les commandes de remplacement, après l’envoi de la commande exec à l’appareil, ce dernier prend les valeurs définies lorsque la commande exec est acceptée.</span><span class="sxs-lookup"><span data-stu-id="035cd-110">Even though the child nodes under Install support Replace commands, after the Exec command is sent to the device, the device will take the values which are set when the Exec command is accepted.</span></span> <span data-ttu-id="035cd-111">Le serveur ne doit pas s’attendre à ce que la valeur du nœud change après que la commande exec a été acceptée aura un impact sur l’inscription actuelle.</span><span class="sxs-lookup"><span data-stu-id="035cd-111">The server should not expect the node value change after Exec command is accepted will impact the current undergoing enrollment.</span></span> <span data-ttu-id="035cd-112">Le serveur doit vérifier la valeur du nœud État et vérifier que l’appareil n’est pas à l’étape inconnue avant de modifier les valeurs du nœud enfant.</span><span class="sxs-lookup"><span data-stu-id="035cd-112">The server should check the Status node value and make sure the device is not at unknown stage before changing child node values.</span></span>

 

<span data-ttu-id="035cd-113">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="035cd-113">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="035cd-114">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="035cd-114">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ClientCertificateInstall_Install03
{
  string InstanceID;
  string ParentID;
  string ServerURL;
  string Challenge;
  string EKUMapping;
  sint32 KeyUsage;
  string SubjectName;
  sint32 KeyProtection;
  sint32 RetryDelay;
  sint32 RetryCount;
  string TemplateName;
  sint32 KeyLength;
  string HashAlgorithm;
  string CAThumbprint;
  string SubjectAlternativeNames;
  string ValidPeriod;
  sint32 ValidPeriodUnits;
  string ContainerName;
  string CustomTextToShowInPrompt;
  string AADKeyIdentifierList;
};
```

## <a name="members"></a><span data-ttu-id="035cd-115">Membres</span><span class="sxs-lookup"><span data-stu-id="035cd-115">Members</span></span>

<span data-ttu-id="035cd-116">La **classe \_ ClientCertificateInstall \_ Install03 MDM** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="035cd-116">The **MDM\_ClientCertificateInstall\_Install03** class has these types of members:</span></span>

-   [<span data-ttu-id="035cd-117">Méthodes</span><span class="sxs-lookup"><span data-stu-id="035cd-117">Methods</span></span>](#methods)
-   [<span data-ttu-id="035cd-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="035cd-118">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="035cd-119">Méthodes</span><span class="sxs-lookup"><span data-stu-id="035cd-119">Methods</span></span>

<span data-ttu-id="035cd-120">La **classe \_ ClientCertificateInstall \_ Install03 MDM** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="035cd-120">The **MDM\_ClientCertificateInstall\_Install03** class has these methods.</span></span>



| <span data-ttu-id="035cd-121">Méthode</span><span class="sxs-lookup"><span data-stu-id="035cd-121">Method</span></span>                                                                      | <span data-ttu-id="035cd-122">Description</span><span class="sxs-lookup"><span data-stu-id="035cd-122">Description</span></span>                                                                   |
|:----------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="035cd-123">**EnrollMethod**</span><span class="sxs-lookup"><span data-stu-id="035cd-123">**EnrollMethod**</span></span>](mdm-clientcertificateinstall-install03-enrollmethod.md) | <span data-ttu-id="035cd-124">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="035cd-124">Required.</span></span> <span data-ttu-id="035cd-125">Déclenche le démarrage de l’inscription de certificat par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="035cd-125">Triggers the device to start the certificate enrollment.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="035cd-126">Propriétés</span><span class="sxs-lookup"><span data-stu-id="035cd-126">Properties</span></span>

<span data-ttu-id="035cd-127">La **classe \_ ClientCertificateInstall \_ Install03 MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="035cd-127">The **MDM\_ClientCertificateInstall\_Install03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="035cd-128">AADKeyIdentifierList</span><span class="sxs-lookup"><span data-stu-id="035cd-128">AADKeyIdentifierList</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-aadkeyidentifierlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="035cd-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="035cd-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="035cd-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="035cd-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="035cd-131">CAThumbprint</span><span class="sxs-lookup"><span data-stu-id="035cd-131">CAThumbprint</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-cathumbprint)
</dt> <dd> <dl> <dt>

<span data-ttu-id="035cd-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="035cd-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="035cd-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="035cd-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="035cd-134">Défi à relever</span><span class="sxs-lookup"><span data-stu-id="035cd-134">Challenge</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-challenge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="035cd-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="035cd-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="035cd-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="035cd-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="035cd-137">ContainerName</span><span class="sxs-lookup"><span data-stu-id="035cd-137">ContainerName</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-containername)
</dt> <dd> <dl> <dt>

<span data-ttu-id="035cd-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="035cd-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="035cd-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="035cd-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="035cd-140">CustomTextToShowInPrompt</span><span class="sxs-lookup"><span data-stu-id="035cd-140">CustomTextToShowInPrompt</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-customtexttoshowinprompt)
</dt> <dd> <dl> <dt>

<span data-ttu-id="035cd-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="035cd-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="035cd-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="035cd-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="035cd-143">EKUMapping</span><span class="sxs-lookup"><span data-stu-id="035cd-143">EKUMapping</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-ekumapping)
</dt> <dd> <dl> <dt>

<span data-ttu-id="035cd-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="035cd-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="035cd-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="035cd-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="035cd-146">HashAlgorithm</span><span class="sxs-lookup"><span data-stu-id="035cd-146">HashAlgorithm</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-hashalgorithm)
</dt> <dd> <dl> <dt>

<span data-ttu-id="035cd-147">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="035cd-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="035cd-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="035cd-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="035cd-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="035cd-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="035cd-150">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="035cd-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="035cd-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="035cd-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="035cd-152">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="035cd-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="035cd-153">Obligatoire pour l’inscription de certificats SCEP.</span><span class="sxs-lookup"><span data-stu-id="035cd-153">Required for SCEP certificate enrollment.</span></span> <span data-ttu-id="035cd-154">Nœud parent pour grouper le certificat SCEP demande d’installation associée.</span><span class="sxs-lookup"><span data-stu-id="035cd-154">Parent node to group SCEP cert install related request.</span></span>

<span data-ttu-id="035cd-155">Le format est node.</span><span class="sxs-lookup"><span data-stu-id="035cd-155">The Format is node.</span></span>

</dd> <dt>

[<span data-ttu-id="035cd-156">KeyLength</span><span class="sxs-lookup"><span data-stu-id="035cd-156">KeyLength</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-keylength)
</dt> <dd> <dl> <dt>

<span data-ttu-id="035cd-157">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="035cd-157">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="035cd-158">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="035cd-158">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="035cd-159">Keyprotection</span><span class="sxs-lookup"><span data-stu-id="035cd-159">KeyProtection</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-keyprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="035cd-160">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="035cd-160">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="035cd-161">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="035cd-161">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="035cd-162">Utilisation</span><span class="sxs-lookup"><span data-stu-id="035cd-162">KeyUsage</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="035cd-163">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="035cd-163">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="035cd-164">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="035cd-164">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="035cd-165">**ID**</span><span class="sxs-lookup"><span data-stu-id="035cd-165">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="035cd-166">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="035cd-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="035cd-167">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="035cd-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="035cd-168">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="035cd-168">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="035cd-169">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="035cd-169">Describes the full path to the parent node.</span></span>

<span data-ttu-id="035cd-170">La chaîne est « ./Vendor/MSFT/ClientCertificateInstall/PFXCertInstall/SCEP/*UniqueID*».</span><span class="sxs-lookup"><span data-stu-id="035cd-170">The string is "./Vendor/MSFT/ClientCertificateInstall/PFXCertInstall/SCEP/*UniqueID*"</span></span>

</dd> <dt>

[<span data-ttu-id="035cd-171">RetryCount</span><span class="sxs-lookup"><span data-stu-id="035cd-171">RetryCount</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-retrycount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="035cd-172">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="035cd-172">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="035cd-173">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="035cd-173">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="035cd-174">RetryDelay</span><span class="sxs-lookup"><span data-stu-id="035cd-174">RetryDelay</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-retrydelay)
</dt> <dd> <dl> <dt>

<span data-ttu-id="035cd-175">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="035cd-175">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="035cd-176">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="035cd-176">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="035cd-177">ServerURL</span><span class="sxs-lookup"><span data-stu-id="035cd-177">ServerURL</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-serverurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="035cd-178">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="035cd-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="035cd-179">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="035cd-179">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="035cd-180">SubjectAlternativeNames</span><span class="sxs-lookup"><span data-stu-id="035cd-180">SubjectAlternativeNames</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-subjectalternativenames)
</dt> <dd> <dl> <dt>

<span data-ttu-id="035cd-181">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="035cd-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="035cd-182">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="035cd-182">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="035cd-183">SubjectName</span><span class="sxs-lookup"><span data-stu-id="035cd-183">SubjectName</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-subjectname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="035cd-184">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="035cd-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="035cd-185">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="035cd-185">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="035cd-186">TemplateName</span><span class="sxs-lookup"><span data-stu-id="035cd-186">TemplateName</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-templatename)
</dt> <dd> <dl> <dt>

<span data-ttu-id="035cd-187">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="035cd-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="035cd-188">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="035cd-188">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="035cd-189">ValidPeriod</span><span class="sxs-lookup"><span data-stu-id="035cd-189">ValidPeriod</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-validperiod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="035cd-190">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="035cd-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="035cd-191">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="035cd-191">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="035cd-192">ValidPeriodUnits</span><span class="sxs-lookup"><span data-stu-id="035cd-192">ValidPeriodUnits</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-validperiodunits)
</dt> <dd> <dl> <dt>

<span data-ttu-id="035cd-193">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="035cd-193">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="035cd-194">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="035cd-194">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="035cd-195">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="035cd-195">Requirements</span></span>



| <span data-ttu-id="035cd-196">Condition requise</span><span class="sxs-lookup"><span data-stu-id="035cd-196">Requirement</span></span> | <span data-ttu-id="035cd-197">Valeur</span><span class="sxs-lookup"><span data-stu-id="035cd-197">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="035cd-198">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="035cd-198">Minimum supported client</span></span><br/> | <span data-ttu-id="035cd-199">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="035cd-199">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="035cd-200">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="035cd-200">Minimum supported server</span></span><br/> | <span data-ttu-id="035cd-201">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="035cd-201">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="035cd-202">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="035cd-202">Namespace</span></span><br/>                | <span data-ttu-id="035cd-203">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="035cd-203">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="035cd-204">MOF</span><span class="sxs-lookup"><span data-stu-id="035cd-204">MOF</span></span><br/>                      | <dl> <span data-ttu-id="035cd-205"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="035cd-205"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="035cd-206">DLL</span><span class="sxs-lookup"><span data-stu-id="035cd-206">DLL</span></span><br/>                      | <dl> <span data-ttu-id="035cd-207"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="035cd-207"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="035cd-208">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="035cd-208">See also</span></span>

<dl> <dt>

[<span data-ttu-id="035cd-209">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="035cd-209">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

