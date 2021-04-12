---
title: Classe Win32_RDAllowListFileAssociation
description: Décrit une association de type de fichier publiée avec un RemoteApp.
ms.assetid: 80cc8f5e-a7f0-458c-b05b-7822306f839a
ms.tgt_platform: multiple
keywords:
- Win32_RDAllowListFileAssociation de la classe Services Bureau à distance
- Win32_RDAllowListFileAssociation de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_RDAllowListFileAssociation
- Win32_RDAllowListFileAssociation.ExtName
- Win32_RDAllowListFileAssociation.AppAlias
- Win32_RDAllowListFileAssociation.ProgIdHint
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4acbc74b5b0dab228a5c625863b4fcd0574b5f96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465295"
---
# <a name="win32_rdallowlistfileassociation-class"></a><span data-ttu-id="c8bda-105">\_Classe RDAllowListFileAssociation Win32</span><span class="sxs-lookup"><span data-stu-id="c8bda-105">Win32\_RDAllowListFileAssociation class</span></span>

<span data-ttu-id="c8bda-106">Décrit une association de type de fichier publiée avec un RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="c8bda-106">Describes a published file type association with a RemoteApp.</span></span>

<span data-ttu-id="c8bda-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="c8bda-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8bda-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c8bda-108">Syntax</span></span>

``` syntax
class Win32_RDAllowListFileAssociation
{
  string ExtName;
  string AppAlias;
  string ProgIdHint;
};
```

## <a name="members"></a><span data-ttu-id="c8bda-109">Membres</span><span class="sxs-lookup"><span data-stu-id="c8bda-109">Members</span></span>

<span data-ttu-id="c8bda-110">La classe **Win32 \_ RDAllowListFileAssociation** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c8bda-110">The **Win32\_RDAllowListFileAssociation** class has these types of members:</span></span>

-   [<span data-ttu-id="c8bda-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c8bda-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c8bda-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c8bda-112">Properties</span></span>

<span data-ttu-id="c8bda-113">La classe **Win32 \_ RDAllowListFileAssociation** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="c8bda-113">The **Win32\_RDAllowListFileAssociation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c8bda-114">**AppAlias**</span><span class="sxs-lookup"><span data-stu-id="c8bda-114">**AppAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8bda-115">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c8bda-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8bda-116">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c8bda-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c8bda-117">Alias du RemoteApp associé à l’extension.</span><span class="sxs-lookup"><span data-stu-id="c8bda-117">Alias of the RemoteApp associated with the extension.</span></span>

</dd> <dt>

<span data-ttu-id="c8bda-118">**ExtName**</span><span class="sxs-lookup"><span data-stu-id="c8bda-118">**ExtName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8bda-119">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c8bda-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8bda-120">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c8bda-120">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c8bda-121">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="c8bda-121">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c8bda-122">Nom de l’extension, par exemple. txt.</span><span class="sxs-lookup"><span data-stu-id="c8bda-122">Name of the extension, for example .txt.</span></span>

</dd> <dt>

<span data-ttu-id="c8bda-123">**ProgIdHint**</span><span class="sxs-lookup"><span data-stu-id="c8bda-123">**ProgIdHint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8bda-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c8bda-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8bda-125">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c8bda-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c8bda-126">Conseil permettant d’ouvrir des documents avec cette association de fichiers</span><span class="sxs-lookup"><span data-stu-id="c8bda-126">Hint to help open documents with this file association</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c8bda-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c8bda-127">Requirements</span></span>



| <span data-ttu-id="c8bda-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c8bda-128">Requirement</span></span> | <span data-ttu-id="c8bda-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8bda-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8bda-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c8bda-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c8bda-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c8bda-131">None supported</span></span><br/>                                                               |
| <span data-ttu-id="c8bda-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c8bda-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c8bda-133">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c8bda-133">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="c8bda-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c8bda-134">Namespace</span></span><br/>                | <span data-ttu-id="c8bda-135">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="c8bda-135">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="c8bda-136">MOF</span><span class="sxs-lookup"><span data-stu-id="c8bda-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c8bda-137"><dt>TsAllow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c8bda-137"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="c8bda-138">DLL</span><span class="sxs-lookup"><span data-stu-id="c8bda-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8bda-139"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8bda-139"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

 





