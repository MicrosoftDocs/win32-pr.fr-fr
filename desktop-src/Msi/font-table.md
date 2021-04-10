---
description: La table de polices contient les informations relatives à l’inscription des fichiers de polices dans le système.
ms.assetid: 5ddff430-a6f8-473b-8006-ac0124469a99
title: Tableau des polices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c10208c7b9a14ca7f311aff71653a53a3da9ed0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952303"
---
# <a name="font-table"></a><span data-ttu-id="aa995-103">Tableau des polices</span><span class="sxs-lookup"><span data-stu-id="aa995-103">Font Table</span></span>

<span data-ttu-id="aa995-104">La table de polices contient les informations relatives à l’inscription des fichiers de polices dans le système.</span><span class="sxs-lookup"><span data-stu-id="aa995-104">The Font table contains the information for registering font files with the system.</span></span>

<span data-ttu-id="aa995-105">La table de polices contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="aa995-105">The Font table has the following columns.</span></span>



| <span data-ttu-id="aa995-106">Colonne</span><span class="sxs-lookup"><span data-stu-id="aa995-106">Column</span></span>    | <span data-ttu-id="aa995-107">Type</span><span class="sxs-lookup"><span data-stu-id="aa995-107">Type</span></span>                         | <span data-ttu-id="aa995-108">Clé</span><span class="sxs-lookup"><span data-stu-id="aa995-108">Key</span></span> | <span data-ttu-id="aa995-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="aa995-109">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="aa995-110">fichier\_</span><span class="sxs-lookup"><span data-stu-id="aa995-110">File\_</span></span>    | [<span data-ttu-id="aa995-111">Identificateur</span><span class="sxs-lookup"><span data-stu-id="aa995-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="aa995-112">O</span><span class="sxs-lookup"><span data-stu-id="aa995-112">Y</span></span>   | <span data-ttu-id="aa995-113">N</span><span class="sxs-lookup"><span data-stu-id="aa995-113">N</span></span>        |
| <span data-ttu-id="aa995-114">FontTitle</span><span class="sxs-lookup"><span data-stu-id="aa995-114">FontTitle</span></span> | [<span data-ttu-id="aa995-115">Text</span><span class="sxs-lookup"><span data-stu-id="aa995-115">Text</span></span>](text.md)             | <span data-ttu-id="aa995-116">N</span><span class="sxs-lookup"><span data-stu-id="aa995-116">N</span></span>   | <span data-ttu-id="aa995-117">O</span><span class="sxs-lookup"><span data-stu-id="aa995-117">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="aa995-118">Colonnes</span><span class="sxs-lookup"><span data-stu-id="aa995-118">Columns</span></span>

<dl> <dt>

<span data-ttu-id="aa995-119"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Txt\_</span><span class="sxs-lookup"><span data-stu-id="aa995-119"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="aa995-120">Clé externe dans l’entrée de [table de fichiers](file-table.md) pour le fichier de police.</span><span class="sxs-lookup"><span data-stu-id="aa995-120">External key into the [File table](file-table.md) entry for the font file.</span></span> <span data-ttu-id="aa995-121">Il est recommandé que le composant contenant le fichier de police ait le FontsFolder spécifié dans la \_ colonne répertoire de la [table des composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="aa995-121">It is recommended that the component containing the font file have the FontsFolder specified in the Directory\_ column of the [Component table](component-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa995-122"><span id="FontTitle"></span><span id="fonttitle"></span><span id="FONTTITLE"></span>FontTitle</span><span class="sxs-lookup"><span data-stu-id="aa995-122"><span id="FontTitle"></span><span id="fonttitle"></span><span id="FONTTITLE"></span>FontTitle</span></span>
</dt> <dd>

<span data-ttu-id="aa995-123">Nom de la police.</span><span class="sxs-lookup"><span data-stu-id="aa995-123">Font name.</span></span> <span data-ttu-id="aa995-124">Il est recommandé de conserver cette colonne null pour les polices TrueType et les collections TrueType, car le programme d’installation peut inscrire la police après avoir lu le titre de police correct à partir du fichier de police.</span><span class="sxs-lookup"><span data-stu-id="aa995-124">It is recommended that you leave this column null for TrueType Fonts and TrueType Collections because the installer can register the font after reading the correct font title from the font file.</span></span> <span data-ttu-id="aa995-125">Si le nom de la police est entré, il doit être identique au titre de police du fichier de police.</span><span class="sxs-lookup"><span data-stu-id="aa995-125">If the font name is entered, it must be identical to font title from the font file.</span></span> <span data-ttu-id="aa995-126">Vous devez spécifier un titre pour les polices qui n’ont pas de noms incorporés, tels que les fichiers. fon.</span><span class="sxs-lookup"><span data-stu-id="aa995-126">You must specify a title for fonts that do not have embedded names, such as .fon files.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aa995-127">Notes</span><span class="sxs-lookup"><span data-stu-id="aa995-127">Remarks</span></span>

<span data-ttu-id="aa995-128">Cette table est référencée lorsque l' [action RegisterFonts](registerfonts-action.md) ou l' [action UnregisterFonts](unregisterfonts-action.md) est exécutée.</span><span class="sxs-lookup"><span data-stu-id="aa995-128">This table is referred to when the [RegisterFonts action](registerfonts-action.md) or the [UnregisterFonts action](unregisterfonts-action.md) is executed.</span></span>

<span data-ttu-id="aa995-129">Si le champ FontTitle est laissé null, le nom de la police est lu directement à partir du fichier de police spécifié.</span><span class="sxs-lookup"><span data-stu-id="aa995-129">If the FontTitle field is left Null, the Font name is read directly from the font file specified.</span></span> <span data-ttu-id="aa995-130">Si le nom de police enregistré dans le champ FontTitle diffère du nom de police interne enregistré dans le fichier de police, la police est inscrite deux fois par l' [action RegisterFonts](registerfonts-action.md).</span><span class="sxs-lookup"><span data-stu-id="aa995-130">If the font name recorded into the FontTitle field differs from the internal font name recorded in the font file, the font is registered twice by the [RegisterFonts action](registerfonts-action.md).</span></span>

<span data-ttu-id="aa995-131">Les fichiers de polices ne doivent pas être créés avec un ID de langue, car les polices n’ont pas de ressource d’ID de langue incorporée. Par conséquent, la colonne Language de la [table file](file-table.md) doit être laissée null pour les fichiers de police.</span><span class="sxs-lookup"><span data-stu-id="aa995-131">Font files should not be authored with a language ID, as fonts do not have an embedded language ID resource.Thus the Language column of the [File table](file-table.md) should be left null for font files.</span></span>

<span data-ttu-id="aa995-132">Étant donné que le programme d’installation ne prend pas en compte les fichiers de polices par défaut, les fichiers de polices préexistants peuvent être supprimés avec leur composant lors de la désinstallation d’une application.</span><span class="sxs-lookup"><span data-stu-id="aa995-132">Because the installer does not refcount font files by default, preexisting font files may be removed with their component when uninstalling an application.</span></span> <span data-ttu-id="aa995-133">Pour vous assurer qu’un fichier de polices n’est pas supprimé, les auteurs peuvent définir les indicateurs de bits **msidbComponentAttributesSharedDllRefCount** ou **msidbComponentAttributesPermanent** dans la colonne attributs de la table des composants MSI de la table des composants \_ \_ \_ pour le composant contenant le fichier de police.</span><span class="sxs-lookup"><span data-stu-id="aa995-133">To ensure that a font file is not removed, authors may set the **msidbComponentAttributesSharedDllRefCount** or **msidbComponentAttributesPermanent** bit flags in the Attributes column of the Component Table\_msi\_Component\_Table for the component containing the font file.</span></span>

## <a name="validation"></a><span data-ttu-id="aa995-134">Validation</span><span class="sxs-lookup"><span data-stu-id="aa995-134">Validation</span></span>

<dl>

[<span data-ttu-id="aa995-135">ICE03</span><span class="sxs-lookup"><span data-stu-id="aa995-135">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="aa995-136">ICE06</span><span class="sxs-lookup"><span data-stu-id="aa995-136">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="aa995-137">ICE07</span><span class="sxs-lookup"><span data-stu-id="aa995-137">ICE07</span></span>](ice07.md)  
[<span data-ttu-id="aa995-138">ICE32</span><span class="sxs-lookup"><span data-stu-id="aa995-138">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="aa995-139">ICE51</span><span class="sxs-lookup"><span data-stu-id="aa995-139">ICE51</span></span>](ice51.md)  
[<span data-ttu-id="aa995-140">ICE60</span><span class="sxs-lookup"><span data-stu-id="aa995-140">ICE60</span></span>](ice60.md)  
</dl>

 

 



