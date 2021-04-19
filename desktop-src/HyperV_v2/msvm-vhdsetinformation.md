---
description: Fournit des informations sur un fichier de définition de disque dur virtuel.
ms.assetid: a975c131-d3f3-4be3-bc69-e277e3ce4d28
title: Classe Msvm_VHDSetInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VHDSetInformation
- Msvm_VHDSetInformation.Path
- Msvm_VHDSetInformation.SnapshotIdList
- Msvm_VHDSetInformation.AllPaths
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 51f1371baea902627160c2c7a1fb31d156be8951
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544722"
---
# <a name="msvm_vhdsetinformation-class"></a><span data-ttu-id="65216-103">MSVM \_ VHDSetInformation, classe</span><span class="sxs-lookup"><span data-stu-id="65216-103">Msvm\_VHDSetInformation class</span></span>

<span data-ttu-id="65216-104">Fournit des informations sur un fichier de définition de disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="65216-104">Provides information about a VHD Set file.</span></span>

<span data-ttu-id="65216-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="65216-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="65216-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65216-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VHDSetInformation
{
  string Path;
  string SnapshotIdList[];
  string AllPaths[];
};
```

## <a name="members"></a><span data-ttu-id="65216-107">Membres</span><span class="sxs-lookup"><span data-stu-id="65216-107">Members</span></span>

<span data-ttu-id="65216-108">La classe **MSVM \_ VHDSetInformation** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="65216-108">The **Msvm\_VHDSetInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="65216-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="65216-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="65216-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="65216-110">Properties</span></span>

<span data-ttu-id="65216-111">La classe **MSVM \_ VHDSetInformation** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="65216-111">The **Msvm\_VHDSetInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="65216-112">**AllPaths**</span><span class="sxs-lookup"><span data-stu-id="65216-112">**AllPaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65216-113">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="65216-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="65216-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="65216-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65216-115">Liste de tous les fichiers contenus dans le fichier de définition de disque dur virtuel, y compris les fichiers non référencés et les parents du disque dur virtuel racine.</span><span class="sxs-lookup"><span data-stu-id="65216-115">A list of all files encompassed by the VHD Set file, including any unreferenced files and any parents of the root virtual hard disk.</span></span> <span data-ttu-id="65216-116">Tous les fichiers répertoriés après le disque dur virtuel racine ne sont pas gérés par ce fichier de définition de VHD.</span><span class="sxs-lookup"><span data-stu-id="65216-116">All files listed after the root virtual hard disk are unmanaged by this VHD Set file.</span></span> <span data-ttu-id="65216-117">Ce champ peut être vide si ces informations ne sont pas spécifiquement demandées.</span><span class="sxs-lookup"><span data-stu-id="65216-117">This field may be empty if this information was not specifically requested.</span></span>

</dd> <dt>

<span data-ttu-id="65216-118">**Chemin d’accès**</span><span class="sxs-lookup"><span data-stu-id="65216-118">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65216-119">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="65216-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65216-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="65216-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65216-121">Chemin d’accès du fichier de définition de disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="65216-121">The path of the VHD Set file.</span></span>

</dd> <dt>

<span data-ttu-id="65216-122">**SnapshotIdList**</span><span class="sxs-lookup"><span data-stu-id="65216-122">**SnapshotIdList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65216-123">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="65216-123">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="65216-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="65216-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65216-125">Liste de GUID représentant tous les instantanés contenus dans ce fichier de définition de disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="65216-125">A list of GUIDs representing all of the snapshots contained by this VHD Set file.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="65216-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65216-126">Requirements</span></span>



| <span data-ttu-id="65216-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65216-127">Requirement</span></span> | <span data-ttu-id="65216-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="65216-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65216-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65216-129">Minimum supported client</span></span><br/> | <span data-ttu-id="65216-130">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="65216-130">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="65216-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65216-131">Minimum supported server</span></span><br/> | <span data-ttu-id="65216-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="65216-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="65216-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="65216-133">Namespace</span></span><br/>                | <span data-ttu-id="65216-134">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="65216-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="65216-135">MOF</span><span class="sxs-lookup"><span data-stu-id="65216-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="65216-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="65216-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="65216-137">DLL</span><span class="sxs-lookup"><span data-stu-id="65216-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65216-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="65216-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 




