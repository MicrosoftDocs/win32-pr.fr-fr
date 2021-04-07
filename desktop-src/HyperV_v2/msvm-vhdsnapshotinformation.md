---
description: Fournit des informations sur un instantané dans un fichier de définition de VHD.
ms.assetid: 922bf0b8-523d-488e-9a41-1a27594e2e44
title: Classe Msvm_VHDSnapshotInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VHDSnapshotInformation
- Msvm_VHDSnapshotInformation.FilePath
- Msvm_VHDSnapshotInformation.SnapshotId
- Msvm_VHDSnapshotInformation.SnapshotPath
- Msvm_VHDSnapshotInformation.ParentPathsList
- Msvm_VHDSnapshotInformation.CreationTime
- Msvm_VHDSnapshotInformation.ResilientChangeTrackingId
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1a1e2a573546d62d79170f15abddd8d5c17e30f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863286"
---
# <a name="msvm_vhdsnapshotinformation-class"></a><span data-ttu-id="26a80-103">MSVM \_ VHDSnapshotInformation, classe</span><span class="sxs-lookup"><span data-stu-id="26a80-103">Msvm\_VHDSnapshotInformation class</span></span>

<span data-ttu-id="26a80-104">Fournit des informations sur un instantané dans un fichier de définition de VHD</span><span class="sxs-lookup"><span data-stu-id="26a80-104">Provides information about a snapshot within a VHD Set file</span></span>

<span data-ttu-id="26a80-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="26a80-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="26a80-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26a80-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VHDSnapshotInformation
{
  string   FilePath;
  string   SnapshotId;
  string   SnapshotPath;
  string   ParentPathsList[];
  DATETIME CreationTime;
  string   ResilientChangeTrackingId;
};
```

## <a name="members"></a><span data-ttu-id="26a80-107">Membres</span><span class="sxs-lookup"><span data-stu-id="26a80-107">Members</span></span>

<span data-ttu-id="26a80-108">La classe **MSVM \_ VHDSnapshotInformation** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="26a80-108">The **Msvm\_VHDSnapshotInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="26a80-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="26a80-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="26a80-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="26a80-110">Properties</span></span>

<span data-ttu-id="26a80-111">La classe **MSVM \_ VHDSnapshotInformation** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="26a80-111">The **Msvm\_VHDSnapshotInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="26a80-112">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="26a80-112">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26a80-113">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="26a80-113">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="26a80-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26a80-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26a80-115">Date et heure de création de cet instantané.</span><span class="sxs-lookup"><span data-stu-id="26a80-115">The date and time of this snapshot's creation.</span></span>

</dd> <dt>

<span data-ttu-id="26a80-116">**FilePath**</span><span class="sxs-lookup"><span data-stu-id="26a80-116">**FilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26a80-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="26a80-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26a80-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26a80-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26a80-119">Chemin d’accès du fichier de définition de disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="26a80-119">The path of the VHD Set file.</span></span>

</dd> <dt>

<span data-ttu-id="26a80-120">**ParentPathsList**</span><span class="sxs-lookup"><span data-stu-id="26a80-120">**ParentPathsList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26a80-121">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="26a80-121">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="26a80-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26a80-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26a80-123">Liste des chemins d’accès de fichiers représentant tous les fichiers dont dépend cet instantané.</span><span class="sxs-lookup"><span data-stu-id="26a80-123">A list of file paths representing all of the files on which this snapshot depends.</span></span> <span data-ttu-id="26a80-124">Ce champ est vide, sauf demande spécifique.</span><span class="sxs-lookup"><span data-stu-id="26a80-124">This field will be empty unless specifically requested.</span></span> <span data-ttu-id="26a80-125">La première entrée est le parent immédiat du fichier, la dernière entrée étant la racine.</span><span class="sxs-lookup"><span data-stu-id="26a80-125">The first entry is the file's immediate parent, with the last entry being the root.</span></span>

</dd> <dt>

<span data-ttu-id="26a80-126">**ResilientChangeTrackingId**</span><span class="sxs-lookup"><span data-stu-id="26a80-126">**ResilientChangeTrackingId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26a80-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="26a80-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26a80-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26a80-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26a80-129">ID de suivi des modifications résilient, le cas échéant, associé à cet instantané.</span><span class="sxs-lookup"><span data-stu-id="26a80-129">The resilient change tracking ID, if any, associated with this snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="26a80-130">**SnapshotId**</span><span class="sxs-lookup"><span data-stu-id="26a80-130">**SnapshotId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26a80-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="26a80-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26a80-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26a80-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26a80-133">GUID qui identifie de façon unique cet instantané dans le fichier de définition de disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="26a80-133">A GUID that uniquely identifies this snapshot within the VHD Set file.</span></span>

</dd> <dt>

<span data-ttu-id="26a80-134">**SnapshotPath**</span><span class="sxs-lookup"><span data-stu-id="26a80-134">**SnapshotPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26a80-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="26a80-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26a80-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26a80-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26a80-137">Chemin d’accès du fichier représenté par cet instantané.</span><span class="sxs-lookup"><span data-stu-id="26a80-137">The path of the file represented by this snapshot.</span></span> <span data-ttu-id="26a80-138">Ce champ peut être vide si aucun fichier n’est associé à cet instantané.</span><span class="sxs-lookup"><span data-stu-id="26a80-138">This field may be empty if there is no file associated with this snapshot.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="26a80-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26a80-139">Requirements</span></span>



| <span data-ttu-id="26a80-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26a80-140">Requirement</span></span> | <span data-ttu-id="26a80-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="26a80-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26a80-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26a80-142">Minimum supported client</span></span><br/> | <span data-ttu-id="26a80-143">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26a80-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="26a80-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26a80-144">Minimum supported server</span></span><br/> | <span data-ttu-id="26a80-145">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="26a80-145">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="26a80-146">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="26a80-146">Namespace</span></span><br/>                | <span data-ttu-id="26a80-147">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="26a80-147">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="26a80-148">MOF</span><span class="sxs-lookup"><span data-stu-id="26a80-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26a80-149"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="26a80-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="26a80-150">DLL</span><span class="sxs-lookup"><span data-stu-id="26a80-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26a80-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="26a80-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 




