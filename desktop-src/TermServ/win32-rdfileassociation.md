---
title: Classe Win32_RDFileAssociation
description: Représente une association de types de fichiers pour un RemoteApp.
ms.assetid: 9ecf6fa5-36f0-4b37-9d59-781b41c1d90c
ms.tgt_platform: multiple
keywords:
- Win32_RDFileAssociation de la classe Services Bureau à distance
- Win32_RDFileAssociation de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_RDFileAssociation
- Win32_RDFileAssociation.ExtName
- Win32_RDFileAssociation.ProgIdHint
- Win32_RDFileAssociation.IconPath
- Win32_RDFileAssociation.IconIndex
- Win32_RDFileAssociation.IconContents
- Win32_RDFileAssociation.PrimaryHandler
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac64cd38bdad748c64fe6f52cb7a6da8d8220cba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941991"
---
# <a name="win32_rdfileassociation-class"></a><span data-ttu-id="fd688-105">\_Classe RDFileAssociation Win32</span><span class="sxs-lookup"><span data-stu-id="fd688-105">Win32\_RDFileAssociation class</span></span>

<span data-ttu-id="fd688-106">Représente une association de types de fichiers pour un RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="fd688-106">Represents a file type association for a RemoteApp.</span></span>

<span data-ttu-id="fd688-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="fd688-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd688-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd688-108">Syntax</span></span>

``` syntax
class Win32_RDFileAssociation
{
  string  ExtName;
  string  ProgIdHint;
  string  IconPath;
  sint32  IconIndex;
  uint8   IconContents[];
  boolean PrimaryHandler;
};
```

## <a name="members"></a><span data-ttu-id="fd688-109">Membres</span><span class="sxs-lookup"><span data-stu-id="fd688-109">Members</span></span>

<span data-ttu-id="fd688-110">La classe **Win32 \_ RDFileAssociation** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fd688-110">The **Win32\_RDFileAssociation** class has these types of members:</span></span>

-   [<span data-ttu-id="fd688-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fd688-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fd688-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fd688-112">Properties</span></span>

<span data-ttu-id="fd688-113">La classe **Win32 \_ RDFileAssociation** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="fd688-113">The **Win32\_RDFileAssociation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fd688-114">**ExtName**</span><span class="sxs-lookup"><span data-stu-id="fd688-114">**ExtName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd688-115">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fd688-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd688-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd688-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd688-117">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="fd688-117">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="fd688-118">Nom de l’extension de nom de fichier, par exemple. txt.</span><span class="sxs-lookup"><span data-stu-id="fd688-118">The name of the file name extension, for example .txt.</span></span>

</dd> <dt>

<span data-ttu-id="fd688-119">**IconContents**</span><span class="sxs-lookup"><span data-stu-id="fd688-119">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd688-120">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="fd688-120">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="fd688-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd688-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd688-122">Contenu de l’icône pour cette association de fichiers.</span><span class="sxs-lookup"><span data-stu-id="fd688-122">The contents of the icon for this file association.</span></span>

</dd> <dt>

<span data-ttu-id="fd688-123">**IndexIcône**</span><span class="sxs-lookup"><span data-stu-id="fd688-123">**IconIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd688-124">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="fd688-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd688-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd688-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd688-126">Index de l’icône dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="fd688-126">The index of the icon in the file.</span></span>

</dd> <dt>

<span data-ttu-id="fd688-127">**IconPath**</span><span class="sxs-lookup"><span data-stu-id="fd688-127">**IconPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd688-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fd688-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd688-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd688-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd688-130">Chemin d’accès de fichier à l’icône pour cette association de fichiers.</span><span class="sxs-lookup"><span data-stu-id="fd688-130">The file path to the icon for this file association.</span></span>

</dd> <dt>

<span data-ttu-id="fd688-131">**PrimaryHandler**</span><span class="sxs-lookup"><span data-stu-id="fd688-131">**PrimaryHandler**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd688-132">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="fd688-132">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fd688-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd688-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd688-134">Indique si cette association concerne un gestionnaire principal.</span><span class="sxs-lookup"><span data-stu-id="fd688-134">Indicates whether this association is for a primary handler.</span></span>

</dd> <dt>

<span data-ttu-id="fd688-135">**ProgIdHint**</span><span class="sxs-lookup"><span data-stu-id="fd688-135">**ProgIdHint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd688-136">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fd688-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd688-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd688-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd688-138">Indicateur permettant d’ouvrir des documents avec cette association de fichiers.</span><span class="sxs-lookup"><span data-stu-id="fd688-138">The Hint to help open documents with this file association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fd688-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd688-139">Requirements</span></span>



| <span data-ttu-id="fd688-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd688-140">Requirement</span></span> | <span data-ttu-id="fd688-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd688-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd688-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd688-142">Minimum supported client</span></span><br/> | <span data-ttu-id="fd688-143">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd688-143">None supported</span></span><br/>                                                               |
| <span data-ttu-id="fd688-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd688-144">Minimum supported server</span></span><br/> | <span data-ttu-id="fd688-145">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fd688-145">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="fd688-146">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fd688-146">Namespace</span></span><br/>                | <span data-ttu-id="fd688-147">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="fd688-147">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="fd688-148">MOF</span><span class="sxs-lookup"><span data-stu-id="fd688-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fd688-149"><dt>TsAllow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fd688-149"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="fd688-150">DLL</span><span class="sxs-lookup"><span data-stu-id="fd688-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd688-151"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd688-151"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

 





