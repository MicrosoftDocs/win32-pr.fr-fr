---
description: Fournit un lien entre l’instance des fonctions et les paramètres minimal, maximal, incrémentiel et par défaut d’une ressource.
ms.assetid: 3B09ED8A-D4D0-41E2-B807-96AD8E990773
title: Classe Msvm_SettingsDefineCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SettingsDefineCapabilities
- Msvm_SettingsDefineCapabilities.SupportStatement
- Msvm_SettingsDefineCapabilities.GroupComponent
- Msvm_SettingsDefineCapabilities.PartComponent
- Msvm_SettingsDefineCapabilities.PropertyPolicy
- Msvm_SettingsDefineCapabilities.ValueRole
- Msvm_SettingsDefineCapabilities.ValueRange
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7a312d3453b783c3d72f909ec6cb0b37d83feb9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524909"
---
# <a name="msvm_settingsdefinecapabilities-class"></a><span data-ttu-id="9beb4-103">MSVM \_ SettingsDefineCapabilities, classe</span><span class="sxs-lookup"><span data-stu-id="9beb4-103">Msvm\_SettingsDefineCapabilities class</span></span>

<span data-ttu-id="9beb4-104">Fournit un lien entre l’instance des fonctions et les paramètres minimal, maximal, incrémentiel et par défaut d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="9beb4-104">Provides a link between the capabilities instance and the minimum, maximum, incremental, and default settings for a resource.</span></span>

<span data-ttu-id="9beb4-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="9beb4-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9beb4-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9beb4-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SettingsDefineCapabilities : CIM_SettingsDefineCapabilities
{
  uint16               SupportStatement;
  CIM_Capabilities REF GroupComponent;
  CIM_SettingData  REF PartComponent;
  uint16               PropertyPolicy = 0;
  uint16               ValueRole = 3;
  uint16               ValueRange = 0;
};
```

## <a name="members"></a><span data-ttu-id="9beb4-107">Membres</span><span class="sxs-lookup"><span data-stu-id="9beb4-107">Members</span></span>

<span data-ttu-id="9beb4-108">La classe **MSVM \_ SettingsDefineCapabilities** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9beb4-108">The **Msvm\_SettingsDefineCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="9beb4-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9beb4-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9beb4-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9beb4-110">Properties</span></span>

<span data-ttu-id="9beb4-111">La classe **MSVM \_ SettingsDefineCapabilities** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="9beb4-111">The **Msvm\_SettingsDefineCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9beb4-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="9beb4-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9beb4-113">Type de données : **[ **\_ fonctionnalités CIM**](/previous-versions//cc136806(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="9beb4-113">Data type: **[**CIM\_Capabilities**](/previous-versions//cc136806(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="9beb4-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9beb4-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9beb4-115">Instance des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="9beb4-115">The capabilities instance.</span></span> <span data-ttu-id="9beb4-116">Cette propriété est héritée de la [**\_ SettingsDefineCapabilities CIM**](/previous-versions//cc136913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9beb4-116">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9beb4-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="9beb4-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9beb4-118">Type de données : **[ **\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="9beb4-118">Data type: **[**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="9beb4-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9beb4-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9beb4-120">Paramètre utilisé pour définir l’instance des fonctions associées.</span><span class="sxs-lookup"><span data-stu-id="9beb4-120">A setting used to define the associated capabilities instance.</span></span> <span data-ttu-id="9beb4-121">Cette propriété est héritée de la [**\_ SettingsDefineCapabilities CIM**](/previous-versions//cc136913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9beb4-121">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9beb4-122">**PropertyPolicy**</span><span class="sxs-lookup"><span data-stu-id="9beb4-122">**PropertyPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9beb4-123">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9beb4-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9beb4-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9beb4-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9beb4-125">Indique si les propriétés non null, non-clé de l’instance de données de paramètre associée sont traitées indépendamment ou comme un ensemble corrélé.</span><span class="sxs-lookup"><span data-stu-id="9beb4-125">Indicates whether the non-null, non-key properties of the associated setting data instance are treated independently or as a correlated set.</span></span> <span data-ttu-id="9beb4-126">Cette propriété est héritée de [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)) et est toujours définie sur 0 (indépendant).</span><span class="sxs-lookup"><span data-stu-id="9beb4-126">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)) and it is always set to 0 (Independent).</span></span>

</dd> <dt>

<span data-ttu-id="9beb4-127">**SupportStatement**</span><span class="sxs-lookup"><span data-stu-id="9beb4-127">**SupportStatement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9beb4-128">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9beb4-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9beb4-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9beb4-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9beb4-130">Identifie l’instruction de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9beb4-130">Identifies the support statement.</span></span>

> [!Note]  
> <span data-ttu-id="9beb4-131">Cette propriété a été ajoutée dans Windows 10, version 1703.</span><span class="sxs-lookup"><span data-stu-id="9beb4-131">This property was added in Windows 10, version 1703.</span></span>

 

<dt>

<span id="Production"></span><span id="production"></span><span id="PRODUCTION"></span>

<span data-ttu-id="9beb4-132"><span id="Production"></span><span id="production"></span><span id="PRODUCTION"></span>**Production** (0)</span><span class="sxs-lookup"><span data-stu-id="9beb4-132"><span id="Production"></span><span id="production"></span><span id="PRODUCTION"></span>**Production** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Prerelease"></span><span id="prerelease"></span><span id="PRERELEASE"></span>

<span data-ttu-id="9beb4-133"><span id="Prerelease"></span><span id="prerelease"></span><span id="PRERELEASE"></span>**Version préliminaire** (1)</span><span class="sxs-lookup"><span data-stu-id="9beb4-133"><span id="Prerelease"></span><span id="prerelease"></span><span id="PRERELEASE"></span>**Prerelease** (1)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="9beb4-134">Was non- **production** dans Windows 10, version 1703.</span><span class="sxs-lookup"><span data-stu-id="9beb4-134">Was **NonProduction** in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="9beb4-135"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="9beb4-135"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9beb4-136">**ValueRange**</span><span class="sxs-lookup"><span data-stu-id="9beb4-136">**ValueRange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9beb4-137">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9beb4-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9beb4-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9beb4-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9beb4-139">Toute autre sémantique sur l’interprétation de toutes les propriétés non-null et non-clé des données de paramètre.</span><span class="sxs-lookup"><span data-stu-id="9beb4-139">Any further semantics on the interpretation of all non-null, non-key properties of the setting data.</span></span> <span data-ttu-id="9beb4-140">Cette propriété est héritée de la [**\_ SettingsDefineCapabilities CIM**](/previous-versions//cc136913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9beb4-140">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9beb4-141">**ValueRole**</span><span class="sxs-lookup"><span data-stu-id="9beb4-141">**ValueRole**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9beb4-142">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9beb4-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9beb4-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9beb4-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9beb4-144">Toute autre sémantique sur l’interprétation des propriétés non-null et non-clé des données de paramètre.</span><span class="sxs-lookup"><span data-stu-id="9beb4-144">Any further semantics on the interpretation of the non-null, non-key properties of the setting data.</span></span> <span data-ttu-id="9beb4-145">Cette propriété est héritée de la [**\_ SettingsDefineCapabilities CIM**](/previous-versions//cc136913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9beb4-145">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9beb4-146">Notes</span><span class="sxs-lookup"><span data-stu-id="9beb4-146">Remarks</span></span>

<span data-ttu-id="9beb4-147">Les valeurs des propriétés **ValueRole** et **ValueRange** sont utilisées dans les paires suivantes :</span><span class="sxs-lookup"><span data-stu-id="9beb4-147">The values for the **ValueRole** and **ValueRange** properties are used in the following pairs:</span></span>

-   <span data-ttu-id="9beb4-148">Point/valeur par défaut (0/0)</span><span class="sxs-lookup"><span data-stu-id="9beb4-148">Point/Default (0/0)</span></span>
-   <span data-ttu-id="9beb4-149">Minimums/pris en charge (1/3)</span><span class="sxs-lookup"><span data-stu-id="9beb4-149">Minimums/Supported (1/3)</span></span>
-   <span data-ttu-id="9beb4-150">Maximums/pris en charge (2/3)</span><span class="sxs-lookup"><span data-stu-id="9beb4-150">Maximums/Supported (2/3)</span></span>
-   <span data-ttu-id="9beb4-151">Incréments/pris en charge (3/3).</span><span class="sxs-lookup"><span data-stu-id="9beb4-151">Increments/Supported (3/3).</span></span>

<span data-ttu-id="9beb4-152">« Point » signifie que chacune des propriétés sur l’objet **PartComponent** représente la plateforme par défaut.</span><span class="sxs-lookup"><span data-stu-id="9beb4-152">"Point" means that each of the properties on the **PartComponent** object represents the platform default.</span></span>

<span data-ttu-id="9beb4-153">« Minimums » et « maximums » signifient que chacune des propriétés sur l’objet **PartComponent** représente les plus petites et les plus grandes valeurs possibles pour ces propriétés prises en charge par la plateforme en fonction de la configuration actuelle de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="9beb4-153">"Minimums" and "Maximums" mean that each of the properties on the **PartComponent** object represent the smallest and largest possible values for these properties that are supported by the platform based on your current machine configuration.</span></span>

<span data-ttu-id="9beb4-154">« Incréments » indique la granularité à laquelle vous pouvez augmenter ou diminuer les paramètres.</span><span class="sxs-lookup"><span data-stu-id="9beb4-154">"Increments" indicates the granularity at which you can increase or decrease the settings.</span></span>

<span data-ttu-id="9beb4-155">L’accès à la classe **MSVM \_ SettingsDefineCapabilities** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="9beb4-155">Access to the **Msvm\_SettingsDefineCapabilities** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="9beb4-156">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="9beb4-156">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="9beb4-157">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9beb4-157">Requirements</span></span>



| <span data-ttu-id="9beb4-158">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9beb4-158">Requirement</span></span> | <span data-ttu-id="9beb4-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="9beb4-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9beb4-160">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9beb4-160">Minimum supported client</span></span><br/> | <span data-ttu-id="9beb4-161">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9beb4-161">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9beb4-162">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9beb4-162">Minimum supported server</span></span><br/> | <span data-ttu-id="9beb4-163">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9beb4-163">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9beb4-164">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9beb4-164">Namespace</span></span><br/>                | <span data-ttu-id="9beb4-165">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="9beb4-165">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9beb4-166">MOF</span><span class="sxs-lookup"><span data-stu-id="9beb4-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9beb4-167"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9beb4-167"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9beb4-168">DLL</span><span class="sxs-lookup"><span data-stu-id="9beb4-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9beb4-169"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9beb4-169"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9beb4-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9beb4-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9beb4-171">**\_SETTINGSDEFINECAPABILITIES CIM**</span><span class="sxs-lookup"><span data-stu-id="9beb4-171">**CIM\_SettingsDefineCapabilities**</span></span>](cim-settingsdefinecapabilities.md)
</dt> <dt>

<span data-ttu-id="9beb4-172">[**\_SETTINGSDEFINECAPABILITIES CIM**](/previous-versions//cc136913(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9beb4-172">[**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="9beb4-173">**MSVM \_ SettingsDefineCapabilities (v1)**</span><span class="sxs-lookup"><span data-stu-id="9beb4-173">**Msvm\_SettingsDefineCapabilities (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-settingsdefinecapabilities)
</dt> <dt>

[<span data-ttu-id="9beb4-174">Classes de gestion des ressources</span><span class="sxs-lookup"><span data-stu-id="9beb4-174">Resource Management Classes</span></span>](resource-management-classes.md)
</dt> </dl>

 

