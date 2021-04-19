---
title: Classe Win32_TSVmMetadataAssociation
description: Représente une association entre un Bureau à distance ordinateur virtuel et ses propriétés de métadonnées.
ms.assetid: 374b1a29-78de-45fd-97b3-c5a5b724e66b
ms.tgt_platform: multiple
keywords:
- Win32_TSVmMetadataAssociation de la classe Services Bureau à distance
- Win32_TSVmMetadataAssociation de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSVmMetadataAssociation
- Win32_TSVmMetadataAssociation.TSVm
- Win32_TSVmMetadataAssociation.MetadataItem
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db3a68c20553eaf52903471d19df9df169ecde21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106542856"
---
# <a name="win32_tsvmmetadataassociation-class"></a><span data-ttu-id="2784f-105">\_Classe TSVmMetadataAssociation Win32</span><span class="sxs-lookup"><span data-stu-id="2784f-105">Win32\_TSVmMetadataAssociation class</span></span>

<span data-ttu-id="2784f-106">Représente une association entre un Bureau à distance ordinateur virtuel et ses propriétés de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="2784f-106">Represents an association between a Remote Desktop virtual machine and its metadata properties.</span></span>

<span data-ttu-id="2784f-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="2784f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2784f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2784f-108">Syntax</span></span>

``` syntax
[dynamic, Association, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_TSVmMetadataAssociation
{
  Win32_TSVm             REF TSVm;
  Win32_TSVmMetadataItem REF MetadataItem;
};
```

## <a name="members"></a><span data-ttu-id="2784f-109">Membres</span><span class="sxs-lookup"><span data-stu-id="2784f-109">Members</span></span>

<span data-ttu-id="2784f-110">La classe **Win32 \_ TSVmMetadataAssociation** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2784f-110">The **Win32\_TSVmMetadataAssociation** class has these types of members:</span></span>

-   [<span data-ttu-id="2784f-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2784f-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2784f-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2784f-112">Properties</span></span>

<span data-ttu-id="2784f-113">La classe **Win32 \_ TSVmMetadataAssociation** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="2784f-113">The **Win32\_TSVmMetadataAssociation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2784f-114">**MetadataItem**</span><span class="sxs-lookup"><span data-stu-id="2784f-114">**MetadataItem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2784f-115">Type de données : **[ **Win32 \_ TSVmMetadataItem**](win32-tsvmmetadataitem.md)**</span><span class="sxs-lookup"><span data-stu-id="2784f-115">Data type: **[**Win32\_TSVmMetadataItem**](win32-tsvmmetadataitem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="2784f-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2784f-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2784f-117">Instance de la classe [**\_ TSVmMetadataItem Win32**](win32-tsvmmetadataitem.md) qui représente les métadonnées de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="2784f-117">An instance of the [**Win32\_TSVmMetadataItem**](win32-tsvmmetadataitem.md) class that represents the metadata for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="2784f-118">**TSVm**</span><span class="sxs-lookup"><span data-stu-id="2784f-118">**TSVm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2784f-119">Type de données : **[ **Win32 \_ TSVm**](win32-tsvm.md)**</span><span class="sxs-lookup"><span data-stu-id="2784f-119">Data type: **[**Win32\_TSVm**](win32-tsvm.md)**</span></span>
</dt> <dt>

<span data-ttu-id="2784f-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2784f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2784f-121">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2784f-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2784f-122">Instance de la classe [**\_ TSVm Win32**](win32-tsvm.md) qui représente l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="2784f-122">An instance of the [**Win32\_TSVm**](win32-tsvm.md) class that represents the virtual machine.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2784f-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2784f-123">Requirements</span></span>



| <span data-ttu-id="2784f-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2784f-124">Requirement</span></span> | <span data-ttu-id="2784f-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="2784f-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="2784f-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2784f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2784f-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2784f-127">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="2784f-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2784f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2784f-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2784f-129">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="2784f-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2784f-130">Namespace</span></span><br/>                | <span data-ttu-id="2784f-131">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="2784f-131">Root\\CIMV2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="2784f-132">MOF</span><span class="sxs-lookup"><span data-stu-id="2784f-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2784f-133"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2784f-133"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="2784f-134">DLL</span><span class="sxs-lookup"><span data-stu-id="2784f-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2784f-135"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2784f-135"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



 

