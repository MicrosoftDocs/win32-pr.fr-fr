---
description: Représente les paramètres permettant de définir la source de démarrage d’un ordinateur virtuel.
ms.assetid: 21CD4B71-3D05-469E-89BB-DC2C65F5AB10
title: Classe Msvm_BootSourceSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BootSourceSettingData
- Msvm_BootSourceSettingData.Description
- Msvm_BootSourceSettingData.Caption
- Msvm_BootSourceSettingData.InstanceID
- Msvm_BootSourceSettingData.ElementName
- Msvm_BootSourceSettingData.BootSourceType
- Msvm_BootSourceSettingData.OtherLocation
- Msvm_BootSourceSettingData.FirmwareDevicePath
- Msvm_BootSourceSettingData.BootSourceDescription
- Msvm_BootSourceSettingData.OptionalData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0403846e10df4c9bd54146eea44e8e91c06d01c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521414"
---
# <a name="msvm_bootsourcesettingdata-class"></a><span data-ttu-id="2eef4-103">MSVM \_ BootSourceSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="2eef4-103">Msvm\_BootSourceSettingData class</span></span>

<span data-ttu-id="2eef4-104">Représente les paramètres permettant de définir la source de démarrage d’un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="2eef4-104">Represents the parameters to set the boot source of a virtual machine.</span></span> <span data-ttu-id="2eef4-105">Cette classe dérive de [**la \_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2eef4-105">This class derives from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

<span data-ttu-id="2eef4-106">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="2eef4-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2eef4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2eef4-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BootSourceSettingData : CIM_SettingData
{
  string Description;
  string Caption;
  string InstanceID;
  string ElementName;
  uint32 BootSourceType;
  string OtherLocation;
  string FirmwareDevicePath;
  string BootSourceDescription;
  uint8  OptionalData[];
};
```

## <a name="members"></a><span data-ttu-id="2eef4-108">Membres</span><span class="sxs-lookup"><span data-stu-id="2eef4-108">Members</span></span>

<span data-ttu-id="2eef4-109">La classe **MSVM \_ BootSourceSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2eef4-109">The **Msvm\_BootSourceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="2eef4-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2eef4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2eef4-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2eef4-111">Properties</span></span>

<span data-ttu-id="2eef4-112">La classe **MSVM \_ BootSourceSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="2eef4-112">The **Msvm\_BootSourceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2eef4-113">**BootSourceDescription**</span><span class="sxs-lookup"><span data-stu-id="2eef4-113">**BootSourceDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eef4-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2eef4-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2eef4-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2eef4-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2eef4-116">Description de la source de démarrage fournie par le microprogramme.</span><span class="sxs-lookup"><span data-stu-id="2eef4-116">The description of the boot source provided by the firmware.</span></span>

</dd> <dt>

<span data-ttu-id="2eef4-117">**BootSourceType**</span><span class="sxs-lookup"><span data-stu-id="2eef4-117">**BootSourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eef4-118">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2eef4-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2eef4-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2eef4-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2eef4-120">Valeur d’énumération qui spécifie le type de la source de démarrage.</span><span class="sxs-lookup"><span data-stu-id="2eef4-120">An enumeration value that specifies the type of the boot source.</span></span>

<span data-ttu-id="2eef4-121">Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="2eef4-121">These are valid values:</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2eef4-122">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="2eef4-122">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Drive"></span><span id="drive"></span><span id="DRIVE"></span>

<span data-ttu-id="2eef4-123">**Lecteur** (1)</span><span class="sxs-lookup"><span data-stu-id="2eef4-123">**Drive** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Network"></span><span id="network"></span><span id="NETWORK"></span>

<span data-ttu-id="2eef4-124">**Réseau** (2)</span><span class="sxs-lookup"><span data-stu-id="2eef4-124">**Network** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="File"></span><span id="file"></span><span id="FILE"></span>

<span data-ttu-id="2eef4-125">**Fichier** (3)</span><span class="sxs-lookup"><span data-stu-id="2eef4-125">**File** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2eef4-126">**Caption**</span><span class="sxs-lookup"><span data-stu-id="2eef4-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eef4-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2eef4-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2eef4-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2eef4-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eef4-129">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="2eef4-129">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="2eef4-130">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2eef4-130">A short textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="2eef4-131">**Description**</span><span class="sxs-lookup"><span data-stu-id="2eef4-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eef4-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2eef4-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2eef4-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2eef4-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2eef4-134">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2eef4-134">A textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="2eef4-135">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="2eef4-135">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eef4-136">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2eef4-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2eef4-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2eef4-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2eef4-138">Nom complet de cette instance de SettingData.</span><span class="sxs-lookup"><span data-stu-id="2eef4-138">The display name for this instance of SettingData.</span></span> <span data-ttu-id="2eef4-139">En outre, le nom complet peut être utilisé comme propriété d’index pour une recherche ou une requête.</span><span class="sxs-lookup"><span data-stu-id="2eef4-139">In addition, the display name can be used as an index property for a search or query.</span></span> <span data-ttu-id="2eef4-140">(Remarque : il n’est pas nécessaire que le nom soit unique au sein d’un espace de noms.)</span><span class="sxs-lookup"><span data-stu-id="2eef4-140">(Note: The name does not have to be unique within a namespace.)</span></span>

</dd> <dt>

<span data-ttu-id="2eef4-141">**FirmwareDevicePath**</span><span class="sxs-lookup"><span data-stu-id="2eef4-141">**FirmwareDevicePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eef4-142">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2eef4-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2eef4-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2eef4-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2eef4-144">Chemin d’accès natif utilisé par le microprogramme pour décrire l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2eef4-144">The native path that the firmware uses to describe the device.</span></span>

</dd> <dt>

<span data-ttu-id="2eef4-145">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2eef4-145">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eef4-146">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2eef4-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2eef4-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2eef4-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eef4-148">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="2eef4-148">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="2eef4-149">Dans l’étendue de l’espace de noms d’instanciation, InstanceID identifie de façon opaque et unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="2eef4-149">Within the scope of the instantiating Namespace, InstanceID opaquely and uniquely identifies an instance of this class.</span></span> <span data-ttu-id="2eef4-150">Pour garantir l’unicité dans l’espace de noms, la valeur d’InstanceID doit être construite à l’aide de l’algorithme « préféré » suivant : *identifiant OrgID*:*LocalID* où *identifiant OrgID* et *LocalID* sont séparés par un signe deux-points ( :), et où *identifiant OrgID* doit inclure un nom de droits d’auteur, de marque déposée ou autre que celui qui est détenu par l’entité commerciale qui crée ou définit l’InstanceId ou qui est un ID inscrit affecté à l’entité métier</span><span class="sxs-lookup"><span data-stu-id="2eef4-150">To ensure uniqueness within the NameSpace, the value of InstanceID should be constructed using the following "preferred" algorithm: *OrgID*:*LocalID* Where *OrgID* and *LocalID* are separated by a colon (:), and where *OrgID* must include a copyrighted, trademarked, or otherwise unique name that is owned by the business entity that is creating or defining the InstanceID or that is a registered ID assigned to the business entity by a recognized global authority.</span></span> <span data-ttu-id="2eef4-151">(Cette spécification est semblable à celle de *SchemaName* \_ Structure *className* des noms de classes de schéma.) En outre, pour garantir l’unicité, *identifiant OrgID* ne doit pas contenir de deux-points ( :).</span><span class="sxs-lookup"><span data-stu-id="2eef4-151">(This requirement is similar to the *SchemaName*\_*ClassName* structure of Schema class names.) In addition, to ensure uniqueness, *OrgID* must not contain a colon (:).</span></span> <span data-ttu-id="2eef4-152">Lors de l’utilisation de cet algorithme, le premier signe deux-points devant apparaître dans InstanceID doit apparaître entre *identifiant OrgID* et *LocalID*.</span><span class="sxs-lookup"><span data-stu-id="2eef4-152">When using this algorithm, the first colon to appear in InstanceID must appear between *OrgID* and *LocalID*.</span></span> <span data-ttu-id="2eef4-153">*LocalID* est choisi par l’entité métier et ne doit pas être réutilisé pour identifier les différents éléments sous-jacents (réels).</span><span class="sxs-lookup"><span data-stu-id="2eef4-153">*LocalID* is chosen by the business entity and should not be reused to identify different underlying (real-world) elements.</span></span> <span data-ttu-id="2eef4-154">Si l’algorithme par défaut ci-dessus n’est pas utilisé, l’entité de définition doit s’assurer que l’InstanceID qui en résulte n’est pas réutilisé dans les InstanceIDs produits par ce ou d’autres fournisseurs pour l’espace de noms de cette instance.</span><span class="sxs-lookup"><span data-stu-id="2eef4-154">If the above preferred algorithm is not used, the defining entity must assure that the resulting InstanceID is not reused across any InstanceIDs produced by this or other providers for the NameSpace of this instance.</span></span> <span data-ttu-id="2eef4-155">Pour les instances définies par DMTF, l’algorithme « préféré » doit être utilisé avec le *identifiant OrgID* défini sur CIM.</span><span class="sxs-lookup"><span data-stu-id="2eef4-155">For DMTF-defined instances, the "preferred" algorithm must be used with the *OrgID* set to CIM.</span></span>

</dd> <dt>

<span data-ttu-id="2eef4-156">**OptionalData**</span><span class="sxs-lookup"><span data-stu-id="2eef4-156">**OptionalData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eef4-157">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="2eef4-157">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="2eef4-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2eef4-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eef4-159">Qualificateurs : **OctetString**, [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")</span><span class="sxs-lookup"><span data-stu-id="2eef4-159">Qualifiers: **OctetString**, [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="2eef4-160">Données facultatives fournies par le microprogramme.</span><span class="sxs-lookup"><span data-stu-id="2eef4-160">Optional data provided by the firmware.</span></span>

> [!Note]  
> <span data-ttu-id="2eef4-161">Propriété ajoutée dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="2eef4-161">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="2eef4-162">**OtherLocation**</span><span class="sxs-lookup"><span data-stu-id="2eef4-162">**OtherLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eef4-163">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2eef4-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2eef4-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2eef4-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2eef4-165">Les autres informations d’emplacement, le cas échéant, que le microprogramme utilise pour identifier de manière unique la source de démarrage.</span><span class="sxs-lookup"><span data-stu-id="2eef4-165">The other location info, if any, that the firmware uses to further uniquely identify the boot source.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2eef4-166">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2eef4-166">Requirements</span></span>



| <span data-ttu-id="2eef4-167">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2eef4-167">Requirement</span></span> | <span data-ttu-id="2eef4-168">Valeur</span><span class="sxs-lookup"><span data-stu-id="2eef4-168">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2eef4-169">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2eef4-169">Minimum supported client</span></span><br/> | <span data-ttu-id="2eef4-170">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2eef4-170">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="2eef4-171">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2eef4-171">Minimum supported server</span></span><br/> | <span data-ttu-id="2eef4-172">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2eef4-172">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2eef4-173">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2eef4-173">Namespace</span></span><br/>                | <span data-ttu-id="2eef4-174">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="2eef4-174">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2eef4-175">MOF</span><span class="sxs-lookup"><span data-stu-id="2eef4-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2eef4-176"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2eef4-176"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2eef4-177">DLL</span><span class="sxs-lookup"><span data-stu-id="2eef4-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2eef4-178"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2eef4-178"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2eef4-179">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2eef4-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2eef4-180">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="2eef4-180">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

<span data-ttu-id="2eef4-181">[**\_SETTINGDATA CIM**](/previous-versions//cc136911(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2eef4-181">[**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85))</span></span>
</dt> </dl>

 

