---
title: Classe MDM_ActiveSync_User_Options03
description: La \_ \_ classe Options03 de l’utilisateur MDM ActiveSync \_ définit les options qui sont définies pour chaque compte ActiveSync.
ms.assetid: b325f676-9b83-4212-a228-e2d774515be6
keywords:
- Classe MDM_ActiveSync_User_Options03
- Classe MDM_ActiveSync_User_Options03, Description
topic_type:
- apiref
api_name:
- MDM_ActiveSync_User_Options03
- MDM_ActiveSync_User_Options03.InstanceID
- MDM_ActiveSync_User_Options03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c459e20b519801c622a091060fd6a87ced2807c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103457"
---
# <a name="mdm_activesync_user_options03-class"></a><span data-ttu-id="b75b4-105">\_ \_ Classe OPTIONS03 utilisateur MDM ActiveSync \_</span><span class="sxs-lookup"><span data-stu-id="b75b4-105">MDM\_ActiveSync\_User\_Options03 class</span></span>

<span data-ttu-id="b75b4-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="b75b4-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b75b4-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="b75b4-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b75b4-108">La classe Options03 de l' **\_ \_ utilisateur \_ MDM ActiveSync** définit les options qui sont définies pour chaque compte ActiveSync.</span><span class="sxs-lookup"><span data-stu-id="b75b4-108">The **MDM\_ActiveSync\_User\_Options03** class defines the options that are set for each ActiveSync account.</span></span>

<span data-ttu-id="b75b4-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="b75b4-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b75b4-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b75b4-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ActiveSync_User_Options03
{
  string InstanceID;
  string ParentID;
  string UseSSL;
  string Schedule;
  string MailAgeFilter;
  string Logging;
};
```

## <a name="members"></a><span data-ttu-id="b75b4-111">Membres</span><span class="sxs-lookup"><span data-stu-id="b75b4-111">Members</span></span>

<span data-ttu-id="b75b4-112">La classe Options03 de l' **\_ \_ utilisateur \_ MDM ActiveSync** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b75b4-112">The **MDM\_ActiveSync\_User\_Options03** class has these types of members:</span></span>

-   [<span data-ttu-id="b75b4-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b75b4-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b75b4-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b75b4-114">Properties</span></span>

<span data-ttu-id="b75b4-115">La classe Options03 de l' **\_ \_ utilisateur \_ MDM ActiveSync** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="b75b4-115">The **MDM\_ActiveSync\_User\_Options03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b75b4-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b75b4-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b75b4-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b75b4-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b75b4-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b75b4-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b75b4-119">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b75b4-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b75b4-120">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="b75b4-120">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="b75b4-121">Logging</span><span class="sxs-lookup"><span data-stu-id="b75b4-121">Logging</span></span>](/windows/client-management/mdm/activesync-csp#options-logging)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b75b4-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b75b4-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b75b4-123">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b75b4-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b75b4-124">MailAgeFilter</span><span class="sxs-lookup"><span data-stu-id="b75b4-124">MailAgeFilter</span></span>](/windows/client-management/mdm/activesync-csp#options-mailagefilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b75b4-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b75b4-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b75b4-126">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b75b4-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b75b4-127">**ID**</span><span class="sxs-lookup"><span data-stu-id="b75b4-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b75b4-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b75b4-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b75b4-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b75b4-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b75b4-130">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b75b4-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b75b4-131">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="b75b4-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="b75b4-132">Pour cette classe, la chaîne est « ./Vendor/MSFT/ActiveSync/Accounts/*GUID*/ »</span><span class="sxs-lookup"><span data-stu-id="b75b4-132">For this class, the string is "./Vendor/MSFT/ActiveSync/Accounts/*GUID*/"</span></span>

</dd> <dt>

[<span data-ttu-id="b75b4-133">Planification</span><span class="sxs-lookup"><span data-stu-id="b75b4-133">Schedule</span></span>](/windows/client-management/mdm/activesync-csp#options-schedule)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b75b4-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b75b4-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b75b4-135">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b75b4-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b75b4-136">UseSSL</span><span class="sxs-lookup"><span data-stu-id="b75b4-136">UseSSL</span></span>](/windows/client-management/mdm/activesync-csp#options-usessl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b75b4-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b75b4-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b75b4-138">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b75b4-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b75b4-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b75b4-139">Requirements</span></span>



| <span data-ttu-id="b75b4-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b75b4-140">Requirement</span></span> | <span data-ttu-id="b75b4-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="b75b4-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b75b4-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b75b4-142">Minimum supported client</span></span><br/> | <span data-ttu-id="b75b4-143">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b75b4-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b75b4-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b75b4-144">Minimum supported server</span></span><br/> | <span data-ttu-id="b75b4-145">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b75b4-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b75b4-146">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b75b4-146">Namespace</span></span><br/>                | <span data-ttu-id="b75b4-147">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="b75b4-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="b75b4-148">MOF</span><span class="sxs-lookup"><span data-stu-id="b75b4-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b75b4-149"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b75b4-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b75b4-150">DLL</span><span class="sxs-lookup"><span data-stu-id="b75b4-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b75b4-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b75b4-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b75b4-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b75b4-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b75b4-153">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="b75b4-153">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

