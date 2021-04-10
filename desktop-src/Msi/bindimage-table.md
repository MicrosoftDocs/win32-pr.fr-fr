---
description: La table BindImage contient des informations sur chaque fichier exécutable ou DLL qui doit être lié aux dll importées par celui-ci.
ms.assetid: 68bf064c-dd85-4796-8e08-6af307f94ad8
title: Table BindImage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f47b97efc8886d7748d0426a49ed76567810939c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951750"
---
# <a name="bindimage-table"></a><span data-ttu-id="44b22-103">Table BindImage</span><span class="sxs-lookup"><span data-stu-id="44b22-103">BindImage Table</span></span>

<span data-ttu-id="44b22-104">La table BindImage contient des informations sur chaque fichier exécutable ou DLL qui doit être lié aux dll importées par celui-ci.</span><span class="sxs-lookup"><span data-stu-id="44b22-104">The BindImage table contains information about each executable or DLL that needs to be bound to the DLLs imported by it.</span></span>

<span data-ttu-id="44b22-105">La table BindImage contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="44b22-105">The BindImage table has the following columns.</span></span>



| <span data-ttu-id="44b22-106">Colonne</span><span class="sxs-lookup"><span data-stu-id="44b22-106">Column</span></span> | <span data-ttu-id="44b22-107">Type</span><span class="sxs-lookup"><span data-stu-id="44b22-107">Type</span></span>                         | <span data-ttu-id="44b22-108">Clé</span><span class="sxs-lookup"><span data-stu-id="44b22-108">Key</span></span> | <span data-ttu-id="44b22-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="44b22-109">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="44b22-110">fichier\_</span><span class="sxs-lookup"><span data-stu-id="44b22-110">File\_</span></span> | [<span data-ttu-id="44b22-111">Identificateur</span><span class="sxs-lookup"><span data-stu-id="44b22-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="44b22-112">O</span><span class="sxs-lookup"><span data-stu-id="44b22-112">Y</span></span>   | <span data-ttu-id="44b22-113">N</span><span class="sxs-lookup"><span data-stu-id="44b22-113">N</span></span>        |
| <span data-ttu-id="44b22-114">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="44b22-114">Path</span></span>   | [<span data-ttu-id="44b22-115">Chemins d’accès</span><span class="sxs-lookup"><span data-stu-id="44b22-115">Paths</span></span>](paths.md)           | <span data-ttu-id="44b22-116">N</span><span class="sxs-lookup"><span data-stu-id="44b22-116">N</span></span>   | <span data-ttu-id="44b22-117">O</span><span class="sxs-lookup"><span data-stu-id="44b22-117">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="44b22-118">Colonnes</span><span class="sxs-lookup"><span data-stu-id="44b22-118">Columns</span></span>

<dl> <dt>

<span data-ttu-id="44b22-119"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Txt\_</span><span class="sxs-lookup"><span data-stu-id="44b22-119"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="44b22-120">Clé externe de la colonne de l’une des [tables de fichiers](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="44b22-120">An external key to column one of the [File table](file-table.md).</span></span> <span data-ttu-id="44b22-121">Il doit s’agir d’un fichier exécutable ou d’un fichier DLL.</span><span class="sxs-lookup"><span data-stu-id="44b22-121">This must be an executable file or a DLL file.</span></span>

</dd> <dt>

<span data-ttu-id="44b22-122"><span id="Path"></span><span id="path"></span><span id="PATH"></span>D</span><span class="sxs-lookup"><span data-stu-id="44b22-122"><span id="Path"></span><span id="path"></span><span id="PATH"></span>Path</span></span>
</dt> <dd>

<span data-ttu-id="44b22-123">Liste de chemins d’accès, séparés par des points-virgules, qui représentent les chemins d’accès dans lesquels rechercher les dll importées.</span><span class="sxs-lookup"><span data-stu-id="44b22-123">A list of paths, separated by semicolons, that represent the paths to be searched to find the imported DLLs.</span></span> <span data-ttu-id="44b22-124">La liste est généralement une liste de propriétés, chaque propriété étant placée entre crochets ( \[ \] ).</span><span class="sxs-lookup"><span data-stu-id="44b22-124">The list is usually a list of properties, with each property enclosed inside square brackets (\[ \]) .</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="44b22-125">Notes</span><span class="sxs-lookup"><span data-stu-id="44b22-125">Remarks</span></span>

<span data-ttu-id="44b22-126">Le programme d’installation calcule l’adresse virtuelle de chaque fonction importée à partir de toutes les dll, et l’adresse virtuelle calculée est ensuite enregistrée dans la table d’adresses d’importation (IAT) de l’image d’importation.</span><span class="sxs-lookup"><span data-stu-id="44b22-126">The installer computes the virtual address of each function that is imported from all DLLs, and the computed virtual address is then saved in the importing image's Import Address Table (IAT).</span></span>

<span data-ttu-id="44b22-127">Cette table est référencée lorsque l' [action BindImage](bindimage-action.md) est exécutée.</span><span class="sxs-lookup"><span data-stu-id="44b22-127">This table is referred to when the [BindImage action](bindimage-action.md) is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="44b22-128">Validation</span><span class="sxs-lookup"><span data-stu-id="44b22-128">Validation</span></span>

<dl>

[<span data-ttu-id="44b22-129">ICE03</span><span class="sxs-lookup"><span data-stu-id="44b22-129">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="44b22-130">ICE06</span><span class="sxs-lookup"><span data-stu-id="44b22-130">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="44b22-131">ICE32</span><span class="sxs-lookup"><span data-stu-id="44b22-131">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="44b22-132">ICE46</span><span class="sxs-lookup"><span data-stu-id="44b22-132">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="44b22-133">ICE76</span><span class="sxs-lookup"><span data-stu-id="44b22-133">ICE76</span></span>](ice76.md)  
</dl>

 

 



