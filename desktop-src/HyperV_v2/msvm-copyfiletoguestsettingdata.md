---
description: Représente les paramètres de copie d’un fichier à partir de l’hôte dans l’invité.
ms.assetid: 255F4132-C212-4A3B-A9B8-3F531E7D1CF9
title: Classe Msvm_CopyFileToGuestSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestSettingData
- Msvm_CopyFileToGuestSettingData.Description
- Msvm_CopyFileToGuestSettingData.Caption
- Msvm_CopyFileToGuestSettingData.InstanceID
- Msvm_CopyFileToGuestSettingData.ElementName
- Msvm_CopyFileToGuestSettingData.OverwriteExisting
- Msvm_CopyFileToGuestSettingData.CreateFullPath
- Msvm_CopyFileToGuestSettingData.SourcePath
- Msvm_CopyFileToGuestSettingData.DestinationPath
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 05e27340acc9dd341bec7857c164f50344abc36f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520132"
---
# <a name="msvm_copyfiletoguestsettingdata-class"></a><span data-ttu-id="90b73-103">MSVM \_ CopyFileToGuestSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="90b73-103">Msvm\_CopyFileToGuestSettingData class</span></span>

<span data-ttu-id="90b73-104">Représente les paramètres de copie d’un fichier à partir de l’hôte dans l’invité.</span><span class="sxs-lookup"><span data-stu-id="90b73-104">Represents the parameters for copying a file from the host into the guest.</span></span> <span data-ttu-id="90b73-105">Cette classe dérive de [**la \_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="90b73-105">This class derives from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

<span data-ttu-id="90b73-106">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="90b73-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="90b73-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="90b73-107">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_CopyFileToGuestSettingData : CIM_SettingData
{
  string  Description;
  string  Caption;
  string  InstanceID;
  string  ElementName;
  boolean OverwriteExisting;
  boolean CreateFullPath;
  string  SourcePath;
  string  DestinationPath;
};
```

## <a name="members"></a><span data-ttu-id="90b73-108">Membres</span><span class="sxs-lookup"><span data-stu-id="90b73-108">Members</span></span>

<span data-ttu-id="90b73-109">La classe **MSVM \_ CopyFileToGuestSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="90b73-109">The **Msvm\_CopyFileToGuestSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="90b73-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="90b73-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="90b73-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="90b73-111">Properties</span></span>

<span data-ttu-id="90b73-112">La classe **MSVM \_ CopyFileToGuestSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="90b73-112">The **Msvm\_CopyFileToGuestSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="90b73-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="90b73-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90b73-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="90b73-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90b73-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="90b73-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90b73-116">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="90b73-116">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="90b73-117">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="90b73-117">A short textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="90b73-118">**CreateFullPath**</span><span class="sxs-lookup"><span data-stu-id="90b73-118">**CreateFullPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90b73-119">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="90b73-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="90b73-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="90b73-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90b73-121">Indique si des répertoires absents dans le chemin d’accès du fichier de destination doivent être créés avant de copier le fichier.</span><span class="sxs-lookup"><span data-stu-id="90b73-121">Indicates whether missing directories in the destination file's path must be created before copying the file.</span></span>

</dd> <dt>

<span data-ttu-id="90b73-122">**Description**</span><span class="sxs-lookup"><span data-stu-id="90b73-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90b73-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="90b73-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90b73-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="90b73-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90b73-125">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="90b73-125">A textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="90b73-126">**DestinationPath**</span><span class="sxs-lookup"><span data-stu-id="90b73-126">**DestinationPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90b73-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="90b73-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90b73-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="90b73-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90b73-129">Chemin d’accès complet du fichier de destination à copier.</span><span class="sxs-lookup"><span data-stu-id="90b73-129">The complete path of the destination file to be copied.</span></span> <span data-ttu-id="90b73-130">Ce fichier de destination doit être accessible à l’invité et peut contenir des variables d’environnement qui sont développées par l’invité.</span><span class="sxs-lookup"><span data-stu-id="90b73-130">This destination file must be accessible to the guest and can contain environment variables, which are expanded by the guest.</span></span> <span data-ttu-id="90b73-131">Si le chemin d’accès spécifié est un répertoire existant dans l’invité, le fichier de destination est créé dans ce répertoire.</span><span class="sxs-lookup"><span data-stu-id="90b73-131">If the path specified is an existing directory in the guest, the destination file is created in this directory.</span></span> <span data-ttu-id="90b73-132">Dans ce cas, le nom de fichier de **SourcePath** est utilisé comme nom de fichier de destination.</span><span class="sxs-lookup"><span data-stu-id="90b73-132">In this case, the file name from **SourcePath** is used as the destination file name.</span></span>

</dd> <dt>

<span data-ttu-id="90b73-133">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="90b73-133">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90b73-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="90b73-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90b73-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="90b73-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90b73-136">Nom complet de cette instance de SettingData.</span><span class="sxs-lookup"><span data-stu-id="90b73-136">The display name for this instance of SettingData.</span></span> <span data-ttu-id="90b73-137">En outre, le nom complet peut être utilisé comme propriété d’index pour une recherche ou une requête.</span><span class="sxs-lookup"><span data-stu-id="90b73-137">In addition, the display name can be used as an index property for a search or query.</span></span> <span data-ttu-id="90b73-138">(Remarque : il n’est pas nécessaire que le nom soit unique au sein d’un espace de noms.)</span><span class="sxs-lookup"><span data-stu-id="90b73-138">(Note: The name does not have to be unique within a namespace.)</span></span>

</dd> <dt>

<span data-ttu-id="90b73-139">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="90b73-139">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90b73-140">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="90b73-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90b73-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="90b73-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90b73-142">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="90b73-142">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="90b73-143">Dans l’étendue de l’espace de noms d’instanciation, InstanceID identifie de façon opaque et unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="90b73-143">Within the scope of the instantiating Namespace, InstanceID opaquely and uniquely identifies an instance of this class.</span></span> <span data-ttu-id="90b73-144">Pour garantir l’unicité dans l’espace de noms, la valeur d’InstanceID doit être construite à l’aide de l’algorithme « préféré » suivant : *identifiant OrgID*:*LocalID* où *identifiant OrgID* et *LocalID* sont séparés par un signe deux-points ( :), et où *identifiant OrgID* doit inclure un nom de droits d’auteur, de marque déposée ou autre que celui qui est détenu par l’entité commerciale qui crée ou définit l’InstanceId ou qui est un ID inscrit affecté à l’entité métier</span><span class="sxs-lookup"><span data-stu-id="90b73-144">To ensure uniqueness within the NameSpace, the value of InstanceID should be constructed using the following "preferred" algorithm: *OrgID*:*LocalID* Where *OrgID* and *LocalID* are separated by a colon (:), and where *OrgID* must include a copyrighted, trademarked, or otherwise unique name that is owned by the business entity that is creating or defining the InstanceID or that is a registered ID assigned to the business entity by a recognized global authority.</span></span> <span data-ttu-id="90b73-145">(Cette spécification est semblable à celle de *SchemaName* \_ Structure *className* des noms de classes de schéma.) En outre, pour garantir l’unicité, *identifiant OrgID* ne doit pas contenir de deux-points ( :).</span><span class="sxs-lookup"><span data-stu-id="90b73-145">(This requirement is similar to the *SchemaName*\_*ClassName* structure of Schema class names.) In addition, to ensure uniqueness, *OrgID* must not contain a colon (:).</span></span> <span data-ttu-id="90b73-146">Lors de l’utilisation de cet algorithme, le premier signe deux-points devant apparaître dans InstanceID doit apparaître entre *identifiant OrgID* et *LocalID*.</span><span class="sxs-lookup"><span data-stu-id="90b73-146">When using this algorithm, the first colon to appear in InstanceID must appear between *OrgID* and *LocalID*.</span></span> <span data-ttu-id="90b73-147">*LocalID* est choisi par l’entité métier et ne doit pas être réutilisé pour identifier les différents éléments sous-jacents (réels).</span><span class="sxs-lookup"><span data-stu-id="90b73-147">*LocalID* is chosen by the business entity and should not be reused to identify different underlying (real-world) elements.</span></span> <span data-ttu-id="90b73-148">Si l’algorithme par défaut ci-dessus n’est pas utilisé, l’entité de définition doit s’assurer que l’InstanceID qui en résulte n’est pas réutilisé dans les InstanceIDs produits par ce ou d’autres fournisseurs pour l’espace de noms de cette instance.</span><span class="sxs-lookup"><span data-stu-id="90b73-148">If the above preferred algorithm is not used, the defining entity must assure that the resulting InstanceID is not reused across any InstanceIDs produced by this or other providers for the NameSpace of this instance.</span></span> <span data-ttu-id="90b73-149">Pour les instances définies par DMTF, l’algorithme « préféré » doit être utilisé avec le *identifiant OrgID* défini sur CIM.</span><span class="sxs-lookup"><span data-stu-id="90b73-149">For DMTF-defined instances, the "preferred" algorithm must be used with the *OrgID* set to CIM.</span></span>

</dd> <dt>

<span data-ttu-id="90b73-150">**OverwriteExisting**</span><span class="sxs-lookup"><span data-stu-id="90b73-150">**OverwriteExisting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90b73-151">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="90b73-151">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="90b73-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="90b73-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90b73-153">Indique si un fichier de destination existant doit être remplacé.</span><span class="sxs-lookup"><span data-stu-id="90b73-153">Indicates whether an existing destination file must be overwritten.</span></span>

</dd> <dt>

<span data-ttu-id="90b73-154">**SourcePath**</span><span class="sxs-lookup"><span data-stu-id="90b73-154">**SourcePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90b73-155">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="90b73-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90b73-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="90b73-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90b73-157">Chemin d’accès complet du fichier source à copier.</span><span class="sxs-lookup"><span data-stu-id="90b73-157">The complete path of the source file to be copied.</span></span> <span data-ttu-id="90b73-158">Ce fichier source doit être accessible à l’hôte Hyper-V et peut contenir des variables d’environnement qui sont développées par l’hôte Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="90b73-158">This source file must be accessible to the Hyper-V host and can contain environment variables, which are expanded by the Hyper-V host.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="90b73-159">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="90b73-159">Requirements</span></span>



| <span data-ttu-id="90b73-160">Condition requise</span><span class="sxs-lookup"><span data-stu-id="90b73-160">Requirement</span></span> | <span data-ttu-id="90b73-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="90b73-161">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90b73-162">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="90b73-162">Minimum supported client</span></span><br/> | <span data-ttu-id="90b73-163">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="90b73-163">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="90b73-164">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="90b73-164">Minimum supported server</span></span><br/> | <span data-ttu-id="90b73-165">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="90b73-165">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="90b73-166">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="90b73-166">Namespace</span></span><br/>                | <span data-ttu-id="90b73-167">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="90b73-167">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="90b73-168">MOF</span><span class="sxs-lookup"><span data-stu-id="90b73-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="90b73-169"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="90b73-169"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="90b73-170">DLL</span><span class="sxs-lookup"><span data-stu-id="90b73-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90b73-171"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="90b73-171"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="90b73-172">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90b73-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90b73-173">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="90b73-173">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

<span data-ttu-id="90b73-174">[**\_SETTINGDATA CIM**](/previous-versions//cc136911(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="90b73-174">[**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85))</span></span>
</dt> </dl>

 

