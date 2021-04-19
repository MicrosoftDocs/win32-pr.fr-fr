---
description: La table FileSFPCatalog associe les fichiers spécifiés aux fichiers de catalogue utilisés par la protection des fichiers système.
ms.assetid: 70c8b64a-cf15-411c-8388-4a7e3051f45c
title: Table FileSFPCatalog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2300b73cc1639d8a54e206ea609043cf657c91f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536773"
---
# <a name="filesfpcatalog-table"></a><span data-ttu-id="c9615-103">Table FileSFPCatalog</span><span class="sxs-lookup"><span data-stu-id="c9615-103">FileSFPCatalog Table</span></span>

<span data-ttu-id="c9615-104">La table FileSFPCatalog associe les fichiers spécifiés aux fichiers de catalogue utilisés par la protection des fichiers système.</span><span class="sxs-lookup"><span data-stu-id="c9615-104">The FileSFPCatalog table associates specified files with the catalog files used by system file protection.</span></span>

<span data-ttu-id="c9615-105">**Windows Vista, Windows Server 2003 et Windows XP :** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c9615-105">**Windows Vista, Windows Server 2003 and Windows XP:** Not supported.</span></span>

<span data-ttu-id="c9615-106">La table FileSFPCatalog contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="c9615-106">The FileSFPCatalog table has the following columns.</span></span>



| <span data-ttu-id="c9615-107">Colonne</span><span class="sxs-lookup"><span data-stu-id="c9615-107">Column</span></span>       | <span data-ttu-id="c9615-108">Type</span><span class="sxs-lookup"><span data-stu-id="c9615-108">Type</span></span>                         | <span data-ttu-id="c9615-109">Clé</span><span class="sxs-lookup"><span data-stu-id="c9615-109">Key</span></span> | <span data-ttu-id="c9615-110">Nullable</span><span class="sxs-lookup"><span data-stu-id="c9615-110">Nullable</span></span> |
|--------------|------------------------------|-----|----------|
| <span data-ttu-id="c9615-111">fichier\_</span><span class="sxs-lookup"><span data-stu-id="c9615-111">File\_</span></span>       | [<span data-ttu-id="c9615-112">Identificateur</span><span class="sxs-lookup"><span data-stu-id="c9615-112">Identifier</span></span>](identifier.md) | <span data-ttu-id="c9615-113">O</span><span class="sxs-lookup"><span data-stu-id="c9615-113">Y</span></span>   | <span data-ttu-id="c9615-114">N</span><span class="sxs-lookup"><span data-stu-id="c9615-114">N</span></span>        |
| <span data-ttu-id="c9615-115">SFPCatalog\_</span><span class="sxs-lookup"><span data-stu-id="c9615-115">SFPCatalog\_</span></span> | [<span data-ttu-id="c9615-116">Nom du fichier</span><span class="sxs-lookup"><span data-stu-id="c9615-116">Filename</span></span>](filename.md)     | <span data-ttu-id="c9615-117">O</span><span class="sxs-lookup"><span data-stu-id="c9615-117">Y</span></span>   | <span data-ttu-id="c9615-118">N</span><span class="sxs-lookup"><span data-stu-id="c9615-118">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="c9615-119">Colonnes</span><span class="sxs-lookup"><span data-stu-id="c9615-119">Columns</span></span>

<dl> <dt>

<span data-ttu-id="c9615-120"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Txt\_</span><span class="sxs-lookup"><span data-stu-id="c9615-120"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="c9615-121">Clé étrangère vers la [table de fichiers](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="c9615-121">Foreign key to the [File table](file-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="c9615-122"><span id="SFPCatalog_"></span><span id="sfpcatalog_"></span><span id="SFPCATALOG_"></span>SFPCatalog\_</span><span class="sxs-lookup"><span data-stu-id="c9615-122"><span id="SFPCatalog_"></span><span id="sfpcatalog_"></span><span id="SFPCATALOG_"></span>SFPCatalog\_</span></span>
</dt> <dd>

<span data-ttu-id="c9615-123">Clé étrangère vers la [table SFPCatalog](sfpcatalog-table.md).</span><span class="sxs-lookup"><span data-stu-id="c9615-123">Foreign key to the [SFPCatalog table](sfpcatalog-table.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c9615-124">Notes</span><span class="sxs-lookup"><span data-stu-id="c9615-124">Remarks</span></span>

<span data-ttu-id="c9615-125">L' [action InstallSFPCatalogFile](installsfpcatalogfile-action.md) interroge la table de [composants](component-table.md), la [table de fichiers](file-table.md), la table FileSFPCatalog et la [table SFPCatalog](sfpcatalog-table.md).</span><span class="sxs-lookup"><span data-stu-id="c9615-125">The [InstallSFPCatalogFile action](installsfpcatalogfile-action.md) queries the [Component table](component-table.md), [File table](file-table.md), FileSFPCatalog table and [SFPCatalog table](sfpcatalog-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="c9615-126">Validation</span><span class="sxs-lookup"><span data-stu-id="c9615-126">Validation</span></span>

<dl>

[<span data-ttu-id="c9615-127">ICE03</span><span class="sxs-lookup"><span data-stu-id="c9615-127">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="c9615-128">ICE06</span><span class="sxs-lookup"><span data-stu-id="c9615-128">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="c9615-129">ICE32</span><span class="sxs-lookup"><span data-stu-id="c9615-129">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="c9615-130">ICE66</span><span class="sxs-lookup"><span data-stu-id="c9615-130">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="c9615-131">ICE76</span><span class="sxs-lookup"><span data-stu-id="c9615-131">ICE76</span></span>](ice76.md)  
</dl>

 

 



