---
title: Classe MDM_Policy_Config01_TextInput02
description: La \_ classe TextInput02 de la stratégie MDM \_ Config01 \_ représente les stratégies d’entrée de texte disponibles.
ms.assetid: e5a8d331-40ec-49f2-aedd-5941fe59092f
keywords:
- Classe MDM_Policy_Config01_TextInput02
- Classe MDM_Policy_Config01_TextInput02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_TextInput02
- MDM_Policy_Config01_TextInput02.InstanceID
- MDM_Policy_Config01_TextInput02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f79d750973edf501ca292d042e04bf4dc27ef42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465443"
---
# <a name="mdm_policy_config01_textinput02-class"></a><span data-ttu-id="d48f3-105">\_Classe TextInput02 de la stratégie MDM \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="d48f3-105">MDM\_Policy\_Config01\_TextInput02 class</span></span>

<span data-ttu-id="d48f3-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="d48f3-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d48f3-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="d48f3-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d48f3-108">La classe TextInput02 de la **\_ stratégie MDM \_ Config01 \_** représente les stratégies d’entrée de texte disponibles.</span><span class="sxs-lookup"><span data-stu-id="d48f3-108">The **MDM\_Policy\_Config01\_TextInput02** class represents the text input policies available.</span></span>

<span data-ttu-id="d48f3-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="d48f3-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d48f3-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d48f3-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_TextInput02
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

## <a name="members"></a><span data-ttu-id="d48f3-111">Membres</span><span class="sxs-lookup"><span data-stu-id="d48f3-111">Members</span></span>

<span data-ttu-id="d48f3-112">La **classe \_ \_ Config01 \_ TextInput02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d48f3-112">The **MDM\_Policy\_Config01\_TextInput02** class has these types of members:</span></span>

-   [<span data-ttu-id="d48f3-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d48f3-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d48f3-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d48f3-114">Properties</span></span>

<span data-ttu-id="d48f3-115">La **classe \_ \_ Config01 \_ TextInput02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="d48f3-115">The **MDM\_Policy\_Config01\_TextInput02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="d48f3-116">AllowIMELogging</span><span class="sxs-lookup"><span data-stu-id="d48f3-116">AllowIMELogging</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowimelogging)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d48f3-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d48f3-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d48f3-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d48f3-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d48f3-119">Paramètre allowimenetworkaccess activé</span><span class="sxs-lookup"><span data-stu-id="d48f3-119">AllowIMENetworkAccess</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowimenetworkaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d48f3-120">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d48f3-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d48f3-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d48f3-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d48f3-122">Paramètre allowinputpanel activé</span><span class="sxs-lookup"><span data-stu-id="d48f3-122">AllowInputPanel</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowinputpanel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d48f3-123">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d48f3-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d48f3-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d48f3-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d48f3-125">Paramètre allowjapaneseimesurrogatepaircharacters activé</span><span class="sxs-lookup"><span data-stu-id="d48f3-125">AllowJapaneseIMESurrogatePairCharacters</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowjapaneseimesurrogatepaircharacters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d48f3-126">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d48f3-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d48f3-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d48f3-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d48f3-128">Paramètre allowjapaneseivscharacters activé</span><span class="sxs-lookup"><span data-stu-id="d48f3-128">AllowJapaneseIVSCharacters</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowjapaneseivscharacters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d48f3-129">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d48f3-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d48f3-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d48f3-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d48f3-131">Paramètre allowjapanesenonpublishingstandardglyph activé</span><span class="sxs-lookup"><span data-stu-id="d48f3-131">AllowJapaneseNonPublishingStandardGlyph</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowjapanesenonpublishingstandardglyph)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d48f3-132">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d48f3-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d48f3-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d48f3-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d48f3-134">Paramètre allowjapaneseuserdictionary activé</span><span class="sxs-lookup"><span data-stu-id="d48f3-134">AllowJapaneseUserDictionary</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowjapaneseuserdictionary)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d48f3-135">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d48f3-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d48f3-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d48f3-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d48f3-137">Paramètre allowkeyboardtextsuggestions activé</span><span class="sxs-lookup"><span data-stu-id="d48f3-137">AllowKeyboardTextSuggestions</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowkeyboardtextsuggestions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d48f3-138">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d48f3-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d48f3-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d48f3-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d48f3-140">Paramètre allowlanguagefeaturesuninstall activé</span><span class="sxs-lookup"><span data-stu-id="d48f3-140">AllowLanguageFeaturesUninstall</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowlanguagefeaturesuninstall)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d48f3-141">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d48f3-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d48f3-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d48f3-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d48f3-143">Paramètre excludejapaneseimeexceptjis0208 activé</span><span class="sxs-lookup"><span data-stu-id="d48f3-143">ExcludeJapaneseIMEExceptJIS0208</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-excludejapaneseimeexceptjis0208)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d48f3-144">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d48f3-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d48f3-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d48f3-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d48f3-146">Paramètre excludejapaneseimeexceptjis0208andeudc activé</span><span class="sxs-lookup"><span data-stu-id="d48f3-146">ExcludeJapaneseIMEExceptJIS0208andEUDC</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-excludejapaneseimeexceptjis0208andeudc)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d48f3-147">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d48f3-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d48f3-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d48f3-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d48f3-149">ExcludeJapaneseIMEExceptShiftJIS</span><span class="sxs-lookup"><span data-stu-id="d48f3-149">ExcludeJapaneseIMEExceptShiftJIS</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-excludejapaneseimeexceptshiftjis)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d48f3-150">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d48f3-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d48f3-151">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d48f3-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d48f3-152">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d48f3-152">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d48f3-153">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d48f3-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d48f3-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d48f3-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d48f3-155">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d48f3-155">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d48f3-156">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="d48f3-156">Identifies the name of the parent node.</span></span> <span data-ttu-id="d48f3-157">Pour cette classe, la chaîne est « TextInput ».</span><span class="sxs-lookup"><span data-stu-id="d48f3-157">For this class, the string is "TextInput"</span></span>

</dd> <dt>

<span data-ttu-id="d48f3-158">**ID**</span><span class="sxs-lookup"><span data-stu-id="d48f3-158">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d48f3-159">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d48f3-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d48f3-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d48f3-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d48f3-161">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d48f3-161">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d48f3-162">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="d48f3-162">Describes the full path to the parent node.</span></span> <span data-ttu-id="d48f3-163">Pour cette classe, la chaîne est « ./Vendor/MSFT/Policy/Config »</span><span class="sxs-lookup"><span data-stu-id="d48f3-163">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d48f3-164">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d48f3-164">Requirements</span></span>



| <span data-ttu-id="d48f3-165">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d48f3-165">Requirement</span></span> | <span data-ttu-id="d48f3-166">Valeur</span><span class="sxs-lookup"><span data-stu-id="d48f3-166">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d48f3-167">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d48f3-167">Minimum supported client</span></span><br/> | <span data-ttu-id="d48f3-168">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d48f3-168">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d48f3-169">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d48f3-169">Minimum supported server</span></span><br/> | <span data-ttu-id="d48f3-170">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d48f3-170">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="d48f3-171">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d48f3-171">Namespace</span></span><br/>                | <span data-ttu-id="d48f3-172">Racine DMMap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="d48f3-172">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="d48f3-173">MOF</span><span class="sxs-lookup"><span data-stu-id="d48f3-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d48f3-174"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d48f3-174"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d48f3-175">DLL</span><span class="sxs-lookup"><span data-stu-id="d48f3-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d48f3-176"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d48f3-176"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d48f3-177">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d48f3-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d48f3-178">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="d48f3-178">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

