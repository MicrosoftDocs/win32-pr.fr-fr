---
description: Ce tableau contient les fichiers d’icône. Chaque icône de la table est copiée dans un fichier dans le cadre de la publication du produit à utiliser pour les raccourcis publiés et les serveurs OLE. Consultez Limitations OLE sur les flux.
ms.assetid: a59c552a-21c0-4dd4-9146-88a5f9a22962
title: Table d’icônes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8e8e38575dc6f6e6bda10b2c1047f3940f7559
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202539"
---
# <a name="icon-table"></a><span data-ttu-id="ddf87-105">Table d’icônes</span><span class="sxs-lookup"><span data-stu-id="ddf87-105">Icon Table</span></span>

<span data-ttu-id="ddf87-106">Ce tableau contient les fichiers d’icône.</span><span class="sxs-lookup"><span data-stu-id="ddf87-106">This table contains the icon files.</span></span> <span data-ttu-id="ddf87-107">Chaque icône de la table est copiée dans un fichier dans le cadre de la publication du produit à utiliser pour les raccourcis publiés et les serveurs OLE.</span><span class="sxs-lookup"><span data-stu-id="ddf87-107">Each icon from the table is copied to a file as a part of product advertisement to be used for advertised shortcuts and OLE servers.</span></span> <span data-ttu-id="ddf87-108">Consultez [limitations OLE sur les flux](ole-limitations-on-streams.md).</span><span class="sxs-lookup"><span data-stu-id="ddf87-108">See [OLE Limitations on Streams](ole-limitations-on-streams.md).</span></span>

<span data-ttu-id="ddf87-109">La table d’icônes contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="ddf87-109">The Icon table has the following columns.</span></span>



| <span data-ttu-id="ddf87-110">Colonne</span><span class="sxs-lookup"><span data-stu-id="ddf87-110">Column</span></span> | <span data-ttu-id="ddf87-111">Type</span><span class="sxs-lookup"><span data-stu-id="ddf87-111">Type</span></span>                         | <span data-ttu-id="ddf87-112">Clé</span><span class="sxs-lookup"><span data-stu-id="ddf87-112">Key</span></span> | <span data-ttu-id="ddf87-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="ddf87-113">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="ddf87-114">Nom</span><span class="sxs-lookup"><span data-stu-id="ddf87-114">Name</span></span>   | [<span data-ttu-id="ddf87-115">Identificateur</span><span class="sxs-lookup"><span data-stu-id="ddf87-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="ddf87-116">O</span><span class="sxs-lookup"><span data-stu-id="ddf87-116">Y</span></span>   | <span data-ttu-id="ddf87-117">N</span><span class="sxs-lookup"><span data-stu-id="ddf87-117">N</span></span>        |
| <span data-ttu-id="ddf87-118">Données</span><span class="sxs-lookup"><span data-stu-id="ddf87-118">Data</span></span>   | [<span data-ttu-id="ddf87-119">Binaire</span><span class="sxs-lookup"><span data-stu-id="ddf87-119">Binary</span></span>](binary.md)         | <span data-ttu-id="ddf87-120">N</span><span class="sxs-lookup"><span data-stu-id="ddf87-120">N</span></span>   | <span data-ttu-id="ddf87-121">N</span><span class="sxs-lookup"><span data-stu-id="ddf87-121">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="ddf87-122">Colonnes</span><span class="sxs-lookup"><span data-stu-id="ddf87-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="ddf87-123"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomme</span><span class="sxs-lookup"><span data-stu-id="ddf87-123"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="ddf87-124">Nom du fichier d’icône.</span><span class="sxs-lookup"><span data-stu-id="ddf87-124">Name of the icon file.</span></span>

</dd> <dt>

<span data-ttu-id="ddf87-125"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Métadonnée</span><span class="sxs-lookup"><span data-stu-id="ddf87-125"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span></span>
</dt> <dd>

<span data-ttu-id="ddf87-126">Les données de l’icône binaire dans le format PE (. dll ou. exe) ou icône (. ico).</span><span class="sxs-lookup"><span data-stu-id="ddf87-126">The binary icon data in PE (.dll or .exe) or icon (.ico) format.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ddf87-127">Notes</span><span class="sxs-lookup"><span data-stu-id="ddf87-127">Remarks</span></span>

<span data-ttu-id="ddf87-128">Cette table est référencée lorsque l' [action PublishProduct](publishproduct-action.md) est exécutée.</span><span class="sxs-lookup"><span data-stu-id="ddf87-128">This table is referred to when the [PublishProduct action](publishproduct-action.md) is executed.</span></span>

<span data-ttu-id="ddf87-129">Les icônes pour les raccourcis, les extensions de nom de fichier et les CLSID doivent être stockées dans des fichiers distincts du fichier cible lui-même.</span><span class="sxs-lookup"><span data-stu-id="ddf87-129">The icons for shortcuts, file name extensions, and CLSIDs must be stored in files that are separate from the target file itself.</span></span> <span data-ttu-id="ddf87-130">Cela est nécessaire, car le programme d’installation ne doit copier que les fichiers d’icône de petite taille sur l’ordinateur de l’utilisateur lors de la publication de la ressource.</span><span class="sxs-lookup"><span data-stu-id="ddf87-130">This is required because the installer should copy only the small icon files to the user's machine when advertising the resource.</span></span> <span data-ttu-id="ddf87-131">Le développeur d’un package d’installation doit donc créer des fichiers distincts contenant uniquement les icônes.</span><span class="sxs-lookup"><span data-stu-id="ddf87-131">A developer of an installation package therefore needs to author separate files containing only the icons.</span></span> <span data-ttu-id="ddf87-132">Ces fichiers icône sont ensuite stockés sous forme de données binaires dans la table icône.</span><span class="sxs-lookup"><span data-stu-id="ddf87-132">These icon files are then stored as binary data in the Icon table.</span></span>

<span data-ttu-id="ddf87-133">Les fichiers d’icône qui sont associés strictement à des extensions de nom de fichier ou à des CLSID peuvent avoir n’importe quelle extension, telle que. ico.</span><span class="sxs-lookup"><span data-stu-id="ddf87-133">Icon files that are associated strictly with file name extensions or CLSIDs can have any extension, such as .ico.</span></span> <span data-ttu-id="ddf87-134">Toutefois, les fichiers icône associés à des raccourcis doivent être au format binaire EXE et doivent être nommés de telle sorte que leur extension corresponde à l’extension de la cible.</span><span class="sxs-lookup"><span data-stu-id="ddf87-134">However, Icon files that are associated with shortcuts must be in the EXE binary format and must be named such that their extension matches the extension of the target.</span></span> <span data-ttu-id="ddf87-135">Le raccourci ne fonctionnera pas si cette règle n’est pas suivie.</span><span class="sxs-lookup"><span data-stu-id="ddf87-135">The shortcut will not work if this rule is not followed.</span></span> <span data-ttu-id="ddf87-136">Par exemple, si un raccourci doit pointer vers une ressource contenant le fichier de clé Red.bar, le fichier d’icône doit également avoir l’extension. bar.</span><span class="sxs-lookup"><span data-stu-id="ddf87-136">For example, if a shortcut is to point to a resource having the key file Red.bar, then the icon file must also have the extension .bar.</span></span> <span data-ttu-id="ddf87-137">Plusieurs icônes peuvent être insérées dans le même fichier d’icône, à condition que tous les fichiers cibles aient la même extension.</span><span class="sxs-lookup"><span data-stu-id="ddf87-137">Multiple icons can be stuffed into the same icon file as long as all of the target files have the same extension.</span></span>

## <a name="validation"></a><span data-ttu-id="ddf87-138">Validation</span><span class="sxs-lookup"><span data-stu-id="ddf87-138">Validation</span></span>

<dl>

[<span data-ttu-id="ddf87-139">ICE03</span><span class="sxs-lookup"><span data-stu-id="ddf87-139">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="ddf87-140">ICE06</span><span class="sxs-lookup"><span data-stu-id="ddf87-140">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="ddf87-141">ICE29</span><span class="sxs-lookup"><span data-stu-id="ddf87-141">ICE29</span></span>](ice29.md)  
[<span data-ttu-id="ddf87-142">ICE32</span><span class="sxs-lookup"><span data-stu-id="ddf87-142">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="ddf87-143">ICE36</span><span class="sxs-lookup"><span data-stu-id="ddf87-143">ICE36</span></span>](ice36.md)  
[<span data-ttu-id="ddf87-144">ICE50</span><span class="sxs-lookup"><span data-stu-id="ddf87-144">ICE50</span></span>](ice50.md)  
</dl>

 

 



