---
title: Classe Win32_RDCentralPublishedFileAssociation
description: Info pour une extension de fichier associée à une application.
ms.assetid: ba12d933-572c-48d3-bf0f-1c99de61457d
ms.tgt_platform: multiple
keywords:
- Win32_RDCentralPublishedFileAssociation de la classe Services Bureau à distance
- Win32_RDCentralPublishedFileAssociation de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_RDCentralPublishedFileAssociation
- Win32_RDCentralPublishedFileAssociation.ExtName
- Win32_RDCentralPublishedFileAssociation.AppAlias
- Win32_RDCentralPublishedFileAssociation.FarmAlias
- Win32_RDCentralPublishedFileAssociation.ProgIdHint
- Win32_RDCentralPublishedFileAssociation.IconContents
- Win32_RDCentralPublishedFileAssociation.PrimaryHandler
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65a0f1c9bf7905504ee3aa2ba6fff7e9804f4747
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466730"
---
# <a name="win32_rdcentralpublishedfileassociation-class"></a><span data-ttu-id="dd296-105">\_Classe RDCentralPublishedFileAssociation Win32</span><span class="sxs-lookup"><span data-stu-id="dd296-105">Win32\_RDCentralPublishedFileAssociation class</span></span>

<span data-ttu-id="dd296-106">Informations pour une extension de fichier associée à une application</span><span class="sxs-lookup"><span data-stu-id="dd296-106">Info for a file extension associated with an application</span></span>

<span data-ttu-id="dd296-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="dd296-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd296-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dd296-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSCentralPublisher_Prov")]
class Win32_RDCentralPublishedFileAssociation
{
  string  ExtName;
  string  AppAlias;
  string  FarmAlias;
  string  ProgIdHint;
  uint8   IconContents[];
  boolean PrimaryHandler;
};
```

## <a name="members"></a><span data-ttu-id="dd296-109">Membres</span><span class="sxs-lookup"><span data-stu-id="dd296-109">Members</span></span>

<span data-ttu-id="dd296-110">La classe **Win32 \_ RDCentralPublishedFileAssociation** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="dd296-110">The **Win32\_RDCentralPublishedFileAssociation** class has these types of members:</span></span>

-   [<span data-ttu-id="dd296-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="dd296-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dd296-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="dd296-112">Properties</span></span>

<span data-ttu-id="dd296-113">La classe **Win32 \_ RDCentralPublishedFileAssociation** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="dd296-113">The **Win32\_RDCentralPublishedFileAssociation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dd296-114">**AppAlias**</span><span class="sxs-lookup"><span data-stu-id="dd296-114">**AppAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd296-115">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dd296-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd296-116">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="dd296-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dd296-117">Alias du RemoteApp de l’Association de fichiers.</span><span class="sxs-lookup"><span data-stu-id="dd296-117">Alias of the file association's RemoteApp.</span></span>

</dd> <dt>

<span data-ttu-id="dd296-118">**ExtName**</span><span class="sxs-lookup"><span data-stu-id="dd296-118">**ExtName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd296-119">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dd296-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd296-120">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="dd296-120">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dd296-121">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dd296-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="dd296-122">Nom de l’extension (par exemple. txt).</span><span class="sxs-lookup"><span data-stu-id="dd296-122">Name of the extension (e.g. .txt).</span></span>

</dd> <dt>

<span data-ttu-id="dd296-123">**FarmAlias**</span><span class="sxs-lookup"><span data-stu-id="dd296-123">**FarmAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd296-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dd296-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd296-125">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="dd296-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dd296-126">Alias de la batterie RemoteApp’s de l’Association de fichiers</span><span class="sxs-lookup"><span data-stu-id="dd296-126">Alias of the file association's RemoteApp's Farm</span></span>

</dd> <dt>

<span data-ttu-id="dd296-127">**IconContents**</span><span class="sxs-lookup"><span data-stu-id="dd296-127">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd296-128">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="dd296-128">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="dd296-129">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="dd296-129">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dd296-130">Contenu de l’icône pour cette association de fichiers.</span><span class="sxs-lookup"><span data-stu-id="dd296-130">Contents of the icon for this file association.</span></span>

</dd> <dt>

<span data-ttu-id="dd296-131">**PrimaryHandler**</span><span class="sxs-lookup"><span data-stu-id="dd296-131">**PrimaryHandler**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd296-132">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="dd296-132">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dd296-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dd296-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd296-134">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="dd296-134">Reserved for future use.</span></span> <span data-ttu-id="dd296-135">Aura toujours la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="dd296-135">Will always be **true**.</span></span>

</dd> <dt>

<span data-ttu-id="dd296-136">**ProgIdHint**</span><span class="sxs-lookup"><span data-stu-id="dd296-136">**ProgIdHint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd296-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dd296-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd296-138">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="dd296-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dd296-139">Conseil permettant d’ouvrir des documents avec cette association de fichiers.</span><span class="sxs-lookup"><span data-stu-id="dd296-139">Hint to help open documents with this file association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dd296-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd296-140">Requirements</span></span>



| <span data-ttu-id="dd296-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dd296-141">Requirement</span></span> | <span data-ttu-id="dd296-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd296-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd296-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd296-143">Minimum supported client</span></span><br/> | <span data-ttu-id="dd296-144">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd296-144">None supported</span></span><br/>                                                                |
| <span data-ttu-id="dd296-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd296-145">Minimum supported server</span></span><br/> | <span data-ttu-id="dd296-146">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dd296-146">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="dd296-147">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="dd296-147">Namespace</span></span><br/>                | <span data-ttu-id="dd296-148">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="dd296-148">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="dd296-149">MOF</span><span class="sxs-lookup"><span data-stu-id="dd296-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd296-150"><dt>Tscpub. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dd296-150"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="dd296-151">DLL</span><span class="sxs-lookup"><span data-stu-id="dd296-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd296-152"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd296-152"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

