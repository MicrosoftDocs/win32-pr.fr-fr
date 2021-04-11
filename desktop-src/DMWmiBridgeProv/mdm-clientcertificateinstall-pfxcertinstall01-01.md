---
title: Classe MDM_ClientCertificateInstall_PFXCertInstall01_01
description: La \_ classe MDM ClientCertificateInstall \_ PFXCertInstall01 \_ 01 permet à l’entreprise d’utiliser des ID uniques pour différencier les demandes d’installation de certificat différentes.
ms.assetid: 13b4d646-b49e-4a9d-b644-b52279249063
keywords:
- Classe MDM_ClientCertificateInstall_PFXCertInstall01_01
- Classe MDM_ClientCertificateInstall_PFXCertInstall01_01, Description
topic_type:
- apiref
api_name:
- MDM_ClientCertificateInstall_PFXCertInstall01_01
- MDM_ClientCertificateInstall_PFXCertInstall01_01.InstanceID
- MDM_ClientCertificateInstall_PFXCertInstall01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aed0bbbfad0e61a95fa8130921e639de1772233d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105016"
---
# <a name="mdm_clientcertificateinstall_pfxcertinstall01_01-class"></a><span data-ttu-id="e6983-105">\_Classe ClientCertificateInstall \_ PFXCERTINSTALL01 \_ 01 MDM</span><span class="sxs-lookup"><span data-stu-id="e6983-105">MDM\_ClientCertificateInstall\_PFXCertInstall01\_01 class</span></span>

<span data-ttu-id="e6983-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="e6983-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e6983-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="e6983-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e6983-108">La classe **MDM \_ ClientCertificateInstall \_ PFXCertInstall01 \_ 01** permet à l’entreprise d’utiliser des ID uniques pour différencier les demandes d’installation de certificat différentes.</span><span class="sxs-lookup"><span data-stu-id="e6983-108">The **MDM\_ClientCertificateInstall\_PFXCertInstall01\_01** class enables the enterprise to use unique IDs to differentiate different certificate install requests.</span></span>

<span data-ttu-id="e6983-109">Requis pour l’installation du certificat PFX.</span><span class="sxs-lookup"><span data-stu-id="e6983-109">Required for PFX certificate installation.</span></span> <span data-ttu-id="e6983-110">L’appel de Delete sur le nœud This doit supprimer les certificats et les clés qui ont été installés par l’objet BLOB PFX correspondant.</span><span class="sxs-lookup"><span data-stu-id="e6983-110">Calling Delete on the this node, should delete the certificates and the keys that were installed by the corresponding PFX blob.</span></span>

<span data-ttu-id="e6983-111">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="e6983-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6983-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e6983-112">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ClientCertificateInstall_PFXCertInstall01_01
{
  string  InstanceID;
  string  ParentID;
  sint32  KeyLocation;
  string  ContainerName;
  string  PFXCertBlob;
  string  PFXCertPassword;
  sint32  PFXCertPasswordEncryptionType;
  boolean PFXKeyExportable;
  string  Thumbprint;
  sint32  Status;
  string  PFXCertPasswordEncryptionStore;
};
```

## <a name="members"></a><span data-ttu-id="e6983-113">Membres</span><span class="sxs-lookup"><span data-stu-id="e6983-113">Members</span></span>

<span data-ttu-id="e6983-114">La classe **MDM \_ ClientCertificateInstall \_ PFXCertInstall01 \_ 01** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e6983-114">The **MDM\_ClientCertificateInstall\_PFXCertInstall01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="e6983-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e6983-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e6983-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e6983-116">Properties</span></span>

<span data-ttu-id="e6983-117">La classe **MDM \_ ClientCertificateInstall \_ PFXCertInstall01 \_ 01** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="e6983-117">The **MDM\_ClientCertificateInstall\_PFXCertInstall01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="e6983-118">ContainerName</span><span class="sxs-lookup"><span data-stu-id="e6983-118">ContainerName</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-containername)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6983-119">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e6983-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6983-120">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e6983-120">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e6983-121">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e6983-121">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6983-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e6983-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6983-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e6983-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6983-124">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e6983-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e6983-125">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="e6983-125">Identifies the name of the parent node.</span></span> <span data-ttu-id="e6983-126">Pour cette classe, ID unique permettant de différencier les différentes demandes d’installation de certificat.</span><span class="sxs-lookup"><span data-stu-id="e6983-126">For this class, a unique ID to differentiate different certificate install requests.</span></span>

</dd> <dt>

[<span data-ttu-id="e6983-127">Emplacement des keyposition</span><span class="sxs-lookup"><span data-stu-id="e6983-127">KeyLocation</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-keylocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6983-128">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="e6983-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e6983-129">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e6983-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e6983-130">**ID**</span><span class="sxs-lookup"><span data-stu-id="e6983-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6983-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e6983-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6983-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e6983-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6983-133">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e6983-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e6983-134">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="e6983-134">Describes the full path to the parent node.</span></span>

<span data-ttu-id="e6983-135">La chaîne est « ./Vendor/MSFT/ClientCertificateInstall/PFXCertInstall »</span><span class="sxs-lookup"><span data-stu-id="e6983-135">The string is "./Vendor/MSFT/ClientCertificateInstall/PFXCertInstall"</span></span>

</dd> <dt>

[<span data-ttu-id="e6983-136">PFXCertBlob</span><span class="sxs-lookup"><span data-stu-id="e6983-136">PFXCertBlob</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-pfxcertblob)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6983-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e6983-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6983-138">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e6983-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e6983-139">Qualificateurs : **Octetstring**</span><span class="sxs-lookup"><span data-stu-id="e6983-139">Qualifiers: **Octetstring**</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e6983-140">PFXCertPassword</span><span class="sxs-lookup"><span data-stu-id="e6983-140">PFXCertPassword</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-pfxcertpassword)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6983-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e6983-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6983-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e6983-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e6983-143">PFXCertPasswordEncryptionStore</span><span class="sxs-lookup"><span data-stu-id="e6983-143">PFXCertPasswordEncryptionStore</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-pfxcertpasswordencryptionstore)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6983-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e6983-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6983-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e6983-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e6983-146">PFXCertPasswordEncryptionType</span><span class="sxs-lookup"><span data-stu-id="e6983-146">PFXCertPasswordEncryptionType</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-pfxcertpasswordencryptiontype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6983-147">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="e6983-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e6983-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e6983-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e6983-149">PFXKeyExportable</span><span class="sxs-lookup"><span data-stu-id="e6983-149">PFXKeyExportable</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-pfxkeyexportable)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6983-150">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e6983-150">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e6983-151">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e6983-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e6983-152">État</span><span class="sxs-lookup"><span data-stu-id="e6983-152">Status</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6983-153">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="e6983-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e6983-154">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e6983-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e6983-155">Empreinte</span><span class="sxs-lookup"><span data-stu-id="e6983-155">Thumbprint</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-thumbprint)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6983-156">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e6983-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6983-157">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e6983-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e6983-158">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6983-158">Requirements</span></span>



| <span data-ttu-id="e6983-159">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e6983-159">Requirement</span></span> | <span data-ttu-id="e6983-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6983-160">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6983-161">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6983-161">Minimum supported client</span></span><br/> | <span data-ttu-id="e6983-162">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e6983-162">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e6983-163">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6983-163">Minimum supported server</span></span><br/> | <span data-ttu-id="e6983-164">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6983-164">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e6983-165">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e6983-165">Namespace</span></span><br/>                | <span data-ttu-id="e6983-166">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="e6983-166">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="e6983-167">MOF</span><span class="sxs-lookup"><span data-stu-id="e6983-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e6983-168"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e6983-168"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e6983-169">DLL</span><span class="sxs-lookup"><span data-stu-id="e6983-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6983-170"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6983-170"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6983-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6983-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6983-172">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="e6983-172">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

