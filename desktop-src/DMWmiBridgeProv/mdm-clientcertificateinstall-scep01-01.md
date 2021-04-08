---
title: Classe MDM_ClientCertificateInstall_SCEP01_01
description: La \_ classe MDM ClientCertificateInstall \_ SCEP01 \_ 01 permet d’accéder au nœud pour l’installation du certificat SCEP, en utilisant des ID uniques pour différencier les différentes demandes d’installation de certificat.
ms.assetid: 273e6ef7-fd00-4049-bb8b-b9900b3d250b
keywords:
- Classe MDM_ClientCertificateInstall_SCEP01_01
- Classe MDM_ClientCertificateInstall_SCEP01_01, Description
topic_type:
- apiref
api_name:
- MDM_ClientCertificateInstall_SCEP01_01
- MDM_ClientCertificateInstall_SCEP01_01.InstanceID
- MDM_ClientCertificateInstall_SCEP01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5f8db7decb2e3ae0674381b2f17df10f82ee38d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843974"
---
# <a name="mdm_clientcertificateinstall_scep01_01-class"></a><span data-ttu-id="c97f5-105">\_Classe ClientCertificateInstall \_ SCEP01 \_ 01 MDM</span><span class="sxs-lookup"><span data-stu-id="c97f5-105">MDM\_ClientCertificateInstall\_SCEP01\_01 class</span></span>

<span data-ttu-id="c97f5-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="c97f5-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c97f5-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="c97f5-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c97f5-108">La classe **MDM \_ ClientCertificateInstall \_ SCEP01 \_ 01** permet d’accéder au nœud pour l’installation du certificat SCEP, en utilisant des ID uniques pour différencier les différentes demandes d’installation de certificat.</span><span class="sxs-lookup"><span data-stu-id="c97f5-108">The **MDM\_ClientCertificateInstall\_SCEP01\_01** class enables access to the node for SCEP certificate installation, using unique IDs to differentiate different certificate install requests.</span></span>

<span data-ttu-id="c97f5-109">Requis pour l’installation du certificat SCEP.</span><span class="sxs-lookup"><span data-stu-id="c97f5-109">Required for SCEP certificate installation.</span></span>

<span data-ttu-id="c97f5-110">Les opérations prises en charge sont les opérations d’extraction, d’ajout et de suppression.</span><span class="sxs-lookup"><span data-stu-id="c97f5-110">Supported operations are Get, Add and Delete.</span></span>

<span data-ttu-id="c97f5-111">L’appel de Delete sur le nœud This doit supprimer le certificat SCEP correspondant.</span><span class="sxs-lookup"><span data-stu-id="c97f5-111">Calling Delete on the this node should delete the corresponding SCEP certificate.</span></span>

<span data-ttu-id="c97f5-112">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="c97f5-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c97f5-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c97f5-113">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ClientCertificateInstall_SCEP01_01
{
  string InstanceID;
  string ParentID;
  string CertThumbprint;
  sint32 Status;
  sint32 ErrorCode;
  string RespondentServerUrl;
};
```

## <a name="members"></a><span data-ttu-id="c97f5-114">Membres</span><span class="sxs-lookup"><span data-stu-id="c97f5-114">Members</span></span>

<span data-ttu-id="c97f5-115">La classe **MDM \_ ClientCertificateInstall \_ SCEP01 \_ 01** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c97f5-115">The **MDM\_ClientCertificateInstall\_SCEP01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="c97f5-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c97f5-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c97f5-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c97f5-117">Properties</span></span>

<span data-ttu-id="c97f5-118">La classe **MDM \_ ClientCertificateInstall \_ SCEP01 \_ 01** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="c97f5-118">The **MDM\_ClientCertificateInstall\_SCEP01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="c97f5-119">CertThumbprint</span><span class="sxs-lookup"><span data-stu-id="c97f5-119">CertThumbprint</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-certthumbprint)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c97f5-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c97f5-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c97f5-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c97f5-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c97f5-122">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="c97f5-122">ErrorCode</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-errorcode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c97f5-123">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c97f5-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c97f5-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c97f5-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c97f5-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c97f5-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c97f5-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c97f5-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c97f5-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c97f5-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c97f5-128">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c97f5-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c97f5-129">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="c97f5-129">Identifies the name of the parent node.</span></span> <span data-ttu-id="c97f5-130">Pour cette classe, ID unique permettant de différencier les différentes demandes d’installation de certificat.</span><span class="sxs-lookup"><span data-stu-id="c97f5-130">For this class, a unique ID to differentiate different certificate install requests.</span></span>

</dd> <dt>

<span data-ttu-id="c97f5-131">**ID**</span><span class="sxs-lookup"><span data-stu-id="c97f5-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c97f5-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c97f5-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c97f5-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c97f5-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c97f5-134">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c97f5-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c97f5-135">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="c97f5-135">Describes the full path to the parent node.</span></span>

<span data-ttu-id="c97f5-136">La chaîne est « ./Vendor/MSFT/ClientCertificateInstall/SCEP »</span><span class="sxs-lookup"><span data-stu-id="c97f5-136">The string is "./Vendor/MSFT/ClientCertificateInstall/SCEP"</span></span>

</dd> <dt>

[<span data-ttu-id="c97f5-137">RespondentServerUrl</span><span class="sxs-lookup"><span data-stu-id="c97f5-137">RespondentServerUrl</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-respondentserverurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c97f5-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c97f5-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c97f5-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c97f5-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c97f5-140">État</span><span class="sxs-lookup"><span data-stu-id="c97f5-140">Status</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c97f5-141">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c97f5-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c97f5-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c97f5-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c97f5-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c97f5-143">Requirements</span></span>



| <span data-ttu-id="c97f5-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c97f5-144">Requirement</span></span> | <span data-ttu-id="c97f5-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="c97f5-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c97f5-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c97f5-146">Minimum supported client</span></span><br/> | <span data-ttu-id="c97f5-147">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c97f5-147">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c97f5-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c97f5-148">Minimum supported server</span></span><br/> | <span data-ttu-id="c97f5-149">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c97f5-149">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c97f5-150">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c97f5-150">Namespace</span></span><br/>                | <span data-ttu-id="c97f5-151">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="c97f5-151">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="c97f5-152">MOF</span><span class="sxs-lookup"><span data-stu-id="c97f5-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c97f5-153"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c97f5-153"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c97f5-154">DLL</span><span class="sxs-lookup"><span data-stu-id="c97f5-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c97f5-155"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c97f5-155"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c97f5-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c97f5-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c97f5-157">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="c97f5-157">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

