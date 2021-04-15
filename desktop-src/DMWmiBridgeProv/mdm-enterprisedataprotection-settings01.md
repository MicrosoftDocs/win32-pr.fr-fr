---
title: Classe MDM_EnterpriseDataProtection_Settings01
description: La \_ classe EnterpriseDataProtection \_ Settings01 MDM est utilisée pour configurer les paramètres spécifiques de Windows information protection (WIP) (anciennement appelé protection des données d’entreprise).
ms.assetid: 7537f548-85fb-46b4-ab94-c9dcf2bf1447
keywords:
- Classe MDM_EnterpriseDataProtection_Settings01
- Classe MDM_EnterpriseDataProtection_Settings01, Description
topic_type:
- apiref
api_name:
- MDM_EnterpriseDataProtection_Settings01
- MDM_EnterpriseDataProtection_Settings01.InstanceID
- MDM_EnterpriseDataProtection_Settings01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e6ef063a1a8d72666dc44a2276bcecfb7d420c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466207"
---
# <a name="mdm_enterprisedataprotection_settings01-class"></a><span data-ttu-id="ac1bd-105">\_ \_ Classe SETTINGS01 EnterpriseDataProtection MDM</span><span class="sxs-lookup"><span data-stu-id="ac1bd-105">MDM\_EnterpriseDataProtection\_Settings01 class</span></span>

<span data-ttu-id="ac1bd-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="ac1bd-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ac1bd-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="ac1bd-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ac1bd-108">La **classe \_ EnterpriseDataProtection \_ Settings01 MDM** est utilisée pour configurer les paramètres spécifiques de Windows information protection (WIP) (anciennement appelé protection des données d’entreprise).</span><span class="sxs-lookup"><span data-stu-id="ac1bd-108">The **MDM\_EnterpriseDataProtection\_Settings01** class is used to configure Windows Information Protection (WIP) (formerly known as Enterprise Data Protection) specific settings.</span></span> <span data-ttu-id="ac1bd-109">Pour plus d’informations sur les travaux en cours, consultez [protéger vos données d’entreprise à l’aide de la protection des données d’entreprise (EDP)](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip).</span><span class="sxs-lookup"><span data-stu-id="ac1bd-109">For more information about WIP, see [Protect your enterprise data using enterprise data protection (EDP)](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip).</span></span>

<span data-ttu-id="ac1bd-110">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ac1bd-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac1bd-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ac1bd-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_EnterpriseDataProtection_Settings01
{
  string InstanceID;
  string ParentID;
  sint32 EDPEnforcementLevel;
  string EnterpriseProtectedDomainNames;
  sint32 AllowUserDecryption;
  string DataRecoveryCertificate;
  sint32 RevokeOnUnenroll;
  string SMBAutoEncryptedFileExtensions;
  sint32 AllowAzureRMSForEDP;
  string RMSTemplateIDForEDP;
  sint32 EDPShowIcons;
};
```

## <a name="members"></a><span data-ttu-id="ac1bd-112">Membres</span><span class="sxs-lookup"><span data-stu-id="ac1bd-112">Members</span></span>

<span data-ttu-id="ac1bd-113">La **classe \_ EnterpriseDataProtection \_ Settings01 MDM** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ac1bd-113">The **MDM\_EnterpriseDataProtection\_Settings01** class has these types of members:</span></span>

-   [<span data-ttu-id="ac1bd-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ac1bd-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ac1bd-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ac1bd-115">Properties</span></span>

<span data-ttu-id="ac1bd-116">La **classe \_ EnterpriseDataProtection \_ Settings01 MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="ac1bd-116">The **MDM\_EnterpriseDataProtection\_Settings01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="ac1bd-117">AllowAzureRMSForEDP</span><span class="sxs-lookup"><span data-stu-id="ac1bd-117">AllowAzureRMSForEDP</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-allowazurermsforedp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1bd-118">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac1bd-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac1bd-119">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ac1bd-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac1bd-120">AllowUserDecryption</span><span class="sxs-lookup"><span data-stu-id="ac1bd-120">AllowUserDecryption</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-allowuserdecryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1bd-121">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac1bd-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac1bd-122">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ac1bd-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac1bd-123">DataRecoveryCertificate</span><span class="sxs-lookup"><span data-stu-id="ac1bd-123">DataRecoveryCertificate</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-datarecoverycertificate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1bd-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ac1bd-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac1bd-125">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ac1bd-125">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ac1bd-126">Qualificateurs : **Octetstring**</span><span class="sxs-lookup"><span data-stu-id="ac1bd-126">Qualifiers: **Octetstring**</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac1bd-127">EDPEnforcementLevel</span><span class="sxs-lookup"><span data-stu-id="ac1bd-127">EDPEnforcementLevel</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-edpenforcementlevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1bd-128">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac1bd-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac1bd-129">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ac1bd-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac1bd-130">EDPShowIcons</span><span class="sxs-lookup"><span data-stu-id="ac1bd-130">EDPShowIcons</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-edpshowicons)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1bd-131">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac1bd-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac1bd-132">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ac1bd-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac1bd-133">EnterpriseProtectedDomainNames</span><span class="sxs-lookup"><span data-stu-id="ac1bd-133">EnterpriseProtectedDomainNames</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-enterpriseprotecteddomainnames)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1bd-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ac1bd-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac1bd-135">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ac1bd-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ac1bd-136">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ac1bd-136">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1bd-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ac1bd-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac1bd-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ac1bd-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac1bd-139">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ac1bd-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ac1bd-140">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="ac1bd-140">Identifies the name of the parent node.</span></span> <span data-ttu-id="ac1bd-141">Pour cette classe, la chaîne est « Settings ».</span><span class="sxs-lookup"><span data-stu-id="ac1bd-141">For this class, the string is "Settings".</span></span>

</dd> <dt>

<span data-ttu-id="ac1bd-142">**ID**</span><span class="sxs-lookup"><span data-stu-id="ac1bd-142">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1bd-143">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ac1bd-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac1bd-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ac1bd-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac1bd-145">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ac1bd-145">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ac1bd-146">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="ac1bd-146">Describes the full path to the parent node.</span></span> <span data-ttu-id="ac1bd-147">Pour cette classe, la chaîne est « ./Vendor/MSFT/EnterpriseDataProtection »</span><span class="sxs-lookup"><span data-stu-id="ac1bd-147">For this class, the string is "./Vendor/MSFT/EnterpriseDataProtection"</span></span>

</dd> <dt>

[<span data-ttu-id="ac1bd-148">RevokeOnUnenroll</span><span class="sxs-lookup"><span data-stu-id="ac1bd-148">RevokeOnUnenroll</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-revokeonunenroll)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1bd-149">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac1bd-149">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac1bd-150">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ac1bd-150">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac1bd-151">RMSTemplateIDForEDP</span><span class="sxs-lookup"><span data-stu-id="ac1bd-151">RMSTemplateIDForEDP</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-rmstemplateidforedp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1bd-152">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ac1bd-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac1bd-153">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ac1bd-153">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac1bd-154">SMBAutoEncryptedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="ac1bd-154">SMBAutoEncryptedFileExtensions</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-smbautoencryptedfileextensions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1bd-155">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ac1bd-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac1bd-156">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ac1bd-156">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ac1bd-157">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ac1bd-157">Requirements</span></span>



| <span data-ttu-id="ac1bd-158">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ac1bd-158">Requirement</span></span> | <span data-ttu-id="ac1bd-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac1bd-159">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac1bd-160">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ac1bd-160">Minimum supported client</span></span><br/> | <span data-ttu-id="ac1bd-161">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ac1bd-161">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ac1bd-162">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ac1bd-162">Minimum supported server</span></span><br/> | <span data-ttu-id="ac1bd-163">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ac1bd-163">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="ac1bd-164">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ac1bd-164">Namespace</span></span><br/>                | <span data-ttu-id="ac1bd-165">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="ac1bd-165">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="ac1bd-166">MOF</span><span class="sxs-lookup"><span data-stu-id="ac1bd-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ac1bd-167"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ac1bd-167"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="ac1bd-168">DLL</span><span class="sxs-lookup"><span data-stu-id="ac1bd-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac1bd-169"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="ac1bd-169"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

