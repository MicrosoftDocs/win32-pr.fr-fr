---
title: Classe MDM_Policy_Result01_TextInput02
description: La \_ classe TextInput02 de la stratégie MDM \_ Result01 \_ représente les stratégies d’entrée de texte disponibles.
ms.assetid: d0ab2d69-6d43-410e-936a-cb87a521d5f3
keywords:
- Classe MDM_Policy_Result01_TextInput02
- Classe MDM_Policy_Result01_TextInput02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_TextInput02
- MDM_Policy_Result01_TextInput02.InstanceID
- MDM_Policy_Result01_TextInput02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a0c02c2afe70f3e7122de0c3d888c42ac179317
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465006"
---
# <a name="mdm_policy_result01_textinput02-class"></a><span data-ttu-id="bf656-105">\_Classe TextInput02 de la stratégie MDM \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="bf656-105">MDM\_Policy\_Result01\_TextInput02 class</span></span>

<span data-ttu-id="bf656-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="bf656-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="bf656-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="bf656-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="bf656-108">La classe TextInput02 de la **\_ stratégie MDM \_ Result01 \_** représente les stratégies d’entrée de texte disponibles.</span><span class="sxs-lookup"><span data-stu-id="bf656-108">The **MDM\_Policy\_Result01\_TextInput02** class represents the text input policies available.</span></span>

<span data-ttu-id="bf656-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="bf656-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf656-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bf656-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_TextInput02
{
  string InstanceID;
  string ParentID;
  sint32 AllowIMENetworkAccess;
  sint32 AllowIMELogging;
  sint32 AllowJapaneseNonPublishingStandardGlyph;
  sint32 AllowJapaneseIVSCharacters;
  sint32 AllowJapaneseUserDictionary;
  sint32 AllowKeyboardTextSuggestions;
  sint32 AllowJapaneseIMESurrogatePairCharacters;
  sint32 ExcludeJapaneseIMEExceptShiftJIS;
  sint32 ExcludeJapaneseIMEExceptJIS0208;
  sint32 ExcludeJapaneseIMEExceptJIS0208andEUDC;
  sint32 AllowLanguageFeaturesUninstall;
  sint32 AllowInputPanel;
};
```

## <a name="members"></a><span data-ttu-id="bf656-111">Membres</span><span class="sxs-lookup"><span data-stu-id="bf656-111">Members</span></span>

<span data-ttu-id="bf656-112">La **classe \_ \_ Result01 \_ TextInput02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="bf656-112">The **MDM\_Policy\_Result01\_TextInput02** class has these types of members:</span></span>

-   [<span data-ttu-id="bf656-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bf656-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bf656-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bf656-114">Properties</span></span>

<span data-ttu-id="bf656-115">La **classe \_ \_ Result01 \_ TextInput02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="bf656-115">The **MDM\_Policy\_Result01\_TextInput02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="bf656-116">AllowIMELogging</span><span class="sxs-lookup"><span data-stu-id="bf656-116">AllowIMELogging</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowimelogging)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf656-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="bf656-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf656-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bf656-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bf656-119">Paramètre allowimenetworkaccess activé</span><span class="sxs-lookup"><span data-stu-id="bf656-119">AllowIMENetworkAccess</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowimenetworkaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf656-120">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="bf656-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf656-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bf656-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bf656-122">Paramètre allowinputpanel activé</span><span class="sxs-lookup"><span data-stu-id="bf656-122">AllowInputPanel</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowinputpanel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf656-123">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="bf656-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf656-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bf656-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bf656-125">Paramètre allowjapaneseimesurrogatepaircharacters activé</span><span class="sxs-lookup"><span data-stu-id="bf656-125">AllowJapaneseIMESurrogatePairCharacters</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowjapaneseimesurrogatepaircharacters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf656-126">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="bf656-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf656-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bf656-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bf656-128">Paramètre allowjapaneseivscharacters activé</span><span class="sxs-lookup"><span data-stu-id="bf656-128">AllowJapaneseIVSCharacters</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowjapaneseivscharacters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf656-129">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="bf656-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf656-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bf656-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bf656-131">Paramètre allowjapanesenonpublishingstandardglyph activé</span><span class="sxs-lookup"><span data-stu-id="bf656-131">AllowJapaneseNonPublishingStandardGlyph</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowjapanesenonpublishingstandardglyph)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf656-132">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="bf656-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf656-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bf656-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bf656-134">Paramètre allowjapaneseuserdictionary activé</span><span class="sxs-lookup"><span data-stu-id="bf656-134">AllowJapaneseUserDictionary</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowjapaneseuserdictionary)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf656-135">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="bf656-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf656-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bf656-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bf656-137">Paramètre allowkeyboardtextsuggestions activé</span><span class="sxs-lookup"><span data-stu-id="bf656-137">AllowKeyboardTextSuggestions</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowkeyboardtextsuggestions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf656-138">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="bf656-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf656-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bf656-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bf656-140">Paramètre allowlanguagefeaturesuninstall activé</span><span class="sxs-lookup"><span data-stu-id="bf656-140">AllowLanguageFeaturesUninstall</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowlanguagefeaturesuninstall)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf656-141">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="bf656-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf656-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bf656-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bf656-143">Paramètre excludejapaneseimeexceptjis0208 activé</span><span class="sxs-lookup"><span data-stu-id="bf656-143">ExcludeJapaneseIMEExceptJIS0208</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-excludejapaneseimeexceptjis0208)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf656-144">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="bf656-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf656-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bf656-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bf656-146">Paramètre excludejapaneseimeexceptjis0208andeudc activé</span><span class="sxs-lookup"><span data-stu-id="bf656-146">ExcludeJapaneseIMEExceptJIS0208andEUDC</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-excludejapaneseimeexceptjis0208andeudc)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf656-147">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="bf656-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf656-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bf656-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bf656-149">ExcludeJapaneseIMEExceptShiftJIS</span><span class="sxs-lookup"><span data-stu-id="bf656-149">ExcludeJapaneseIMEExceptShiftJIS</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-excludejapaneseimeexceptshiftjis)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf656-150">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="bf656-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf656-151">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bf656-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bf656-152">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="bf656-152">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf656-153">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bf656-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf656-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bf656-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf656-155">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bf656-155">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bf656-156">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="bf656-156">Identifies the name of the parent node.</span></span> <span data-ttu-id="bf656-157">Pour cette classe, la chaîne est « TextInput ».</span><span class="sxs-lookup"><span data-stu-id="bf656-157">For this class, the string is "TextInput"</span></span>

</dd> <dt>

<span data-ttu-id="bf656-158">**ID**</span><span class="sxs-lookup"><span data-stu-id="bf656-158">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf656-159">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bf656-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf656-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bf656-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf656-161">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bf656-161">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bf656-162">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="bf656-162">Describes the full path to the parent node.</span></span> <span data-ttu-id="bf656-163">Pour cette classe, la chaîne est « ./Vendor/MSFT/Policy/Result »</span><span class="sxs-lookup"><span data-stu-id="bf656-163">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bf656-164">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf656-164">Requirements</span></span>



| <span data-ttu-id="bf656-165">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bf656-165">Requirement</span></span> | <span data-ttu-id="bf656-166">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf656-166">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf656-167">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf656-167">Minimum supported client</span></span><br/> | <span data-ttu-id="bf656-168">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bf656-168">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bf656-169">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf656-169">Minimum supported server</span></span><br/> | <span data-ttu-id="bf656-170">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf656-170">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="bf656-171">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="bf656-171">Namespace</span></span><br/>                | <span data-ttu-id="bf656-172">Racine DMMap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="bf656-172">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="bf656-173">MOF</span><span class="sxs-lookup"><span data-stu-id="bf656-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bf656-174"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bf656-174"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="bf656-175">DLL</span><span class="sxs-lookup"><span data-stu-id="bf656-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf656-176"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf656-176"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf656-177">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf656-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf656-178">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="bf656-178">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

