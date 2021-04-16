---
title: Classe MDM_ActiveSync_User_Accounts01_01
description: La \_ \_ classe utilisateur Accounts01 01 de MDM ActiveSync \_ \_ définit tous les comptes ActiveSync disponibles.
ms.assetid: bcd1fdcb-675a-4833-9d3c-0509e68f7b00
keywords:
- Classe MDM_ActiveSync_User_Accounts01_01
- Classe MDM_ActiveSync_User_Accounts01_01, Description
topic_type:
- apiref
api_name:
- MDM_ActiveSync_User_Accounts01_01
- MDM_ActiveSync_User_Accounts01_01.InstanceID
- MDM_ActiveSync_User_Accounts01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a065fb3f33e69b636a35fc848e5d717898f1fa3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465022"
---
# <a name="mdm_activesync_user_accounts01_01-class"></a><span data-ttu-id="9860d-105">\_ \_ \_ \_ Classe Accounts01 01 de l’utilisateur MDM ActiveSync</span><span class="sxs-lookup"><span data-stu-id="9860d-105">MDM\_ActiveSync\_User\_Accounts01\_01 class</span></span>

<span data-ttu-id="9860d-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="9860d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9860d-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="9860d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9860d-108">La **classe \_ \_ utilisateur \_ Accounts01 \_ 01 de MDM ActiveSync** définit tous les comptes ActiveSync disponibles.</span><span class="sxs-lookup"><span data-stu-id="9860d-108">The **MDM\_ActiveSync\_User\_Accounts01\_01** class defines all available ActiveSync accounts.</span></span>

<span data-ttu-id="9860d-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="9860d-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9860d-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9860d-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ActiveSync_User_Accounts01_01
{
  string InstanceID;
  string ParentID;
  string EmailAddress;
  string Domain;
  string AccountIcon;
  string AccountType;
  string AccountName;
  string Password;
  string ServerName;
  string UserName;
};
```

## <a name="members"></a><span data-ttu-id="9860d-111">Membres</span><span class="sxs-lookup"><span data-stu-id="9860d-111">Members</span></span>

<span data-ttu-id="9860d-112">La **classe \_ \_ utilisateur \_ Accounts01 \_ 01 de MDM ActiveSync** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9860d-112">The **MDM\_ActiveSync\_User\_Accounts01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="9860d-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9860d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9860d-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9860d-114">Properties</span></span>

<span data-ttu-id="9860d-115">La **classe \_ \_ utilisateur \_ Accounts01 \_ 01 de MDM ActiveSync** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="9860d-115">The **MDM\_ActiveSync\_User\_Accounts01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="9860d-116">AccountIcon</span><span class="sxs-lookup"><span data-stu-id="9860d-116">AccountIcon</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-accounticon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9860d-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9860d-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9860d-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="9860d-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9860d-119">AccountName</span><span class="sxs-lookup"><span data-stu-id="9860d-119">AccountName</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-accountname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9860d-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9860d-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9860d-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="9860d-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9860d-122">AccountType</span><span class="sxs-lookup"><span data-stu-id="9860d-122">AccountType</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-accounttype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9860d-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9860d-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9860d-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="9860d-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9860d-125">Domaine</span><span class="sxs-lookup"><span data-stu-id="9860d-125">Domain</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-domain)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9860d-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9860d-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9860d-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="9860d-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9860d-128">EmailAddress</span><span class="sxs-lookup"><span data-stu-id="9860d-128">EmailAddress</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-emailaddress)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9860d-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9860d-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9860d-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="9860d-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9860d-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9860d-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9860d-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9860d-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9860d-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9860d-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9860d-134">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9860d-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9860d-135">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="9860d-135">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="9860d-136">**ID**</span><span class="sxs-lookup"><span data-stu-id="9860d-136">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9860d-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9860d-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9860d-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9860d-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9860d-139">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9860d-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9860d-140">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="9860d-140">Describes the full path to the parent node.</span></span> <span data-ttu-id="9860d-141">Pour cette classe, la chaîne est « ./Vendor/MSFT/ActiveSync/ »</span><span class="sxs-lookup"><span data-stu-id="9860d-141">For this class, the string is "./Vendor/MSFT/ActiveSync/"</span></span>

</dd> <dt>

[<span data-ttu-id="9860d-142">Mot de passe</span><span class="sxs-lookup"><span data-stu-id="9860d-142">Password</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-password)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9860d-143">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9860d-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9860d-144">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="9860d-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9860d-145">ServerName</span><span class="sxs-lookup"><span data-stu-id="9860d-145">ServerName</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-servername)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9860d-146">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9860d-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9860d-147">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="9860d-147">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9860d-148">UserName</span><span class="sxs-lookup"><span data-stu-id="9860d-148">UserName</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-username)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9860d-149">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9860d-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9860d-150">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="9860d-150">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9860d-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9860d-151">Requirements</span></span>



| <span data-ttu-id="9860d-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9860d-152">Requirement</span></span> | <span data-ttu-id="9860d-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="9860d-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9860d-154">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9860d-154">Minimum supported client</span></span><br/> | <span data-ttu-id="9860d-155">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9860d-155">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9860d-156">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9860d-156">Minimum supported server</span></span><br/> | <span data-ttu-id="9860d-157">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="9860d-157">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="9860d-158">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9860d-158">Namespace</span></span><br/>                | <span data-ttu-id="9860d-159">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="9860d-159">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="9860d-160">MOF</span><span class="sxs-lookup"><span data-stu-id="9860d-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9860d-161"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9860d-161"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9860d-162">DLL</span><span class="sxs-lookup"><span data-stu-id="9860d-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9860d-163"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9860d-163"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9860d-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9860d-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9860d-165">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="9860d-165">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

