---
description: Une boîte de dialogue Parcourir permet à l’utilisateur de sélectionner un répertoire. Le répertoire n’a pas besoin d’exister et peut être créé à l’aide de ce contrôle.
ms.assetid: 35b991b8-d291-44ef-b1c0-8128bed3c3c8
title: Boîte de dialogue Parcourir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3f6d3c3d95caec7e9a439621f6741b0dceb0c83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393608"
---
# <a name="browse-dialog"></a><span data-ttu-id="41a73-104">Boîte de dialogue Parcourir</span><span class="sxs-lookup"><span data-stu-id="41a73-104">Browse Dialog</span></span>

<span data-ttu-id="41a73-105">Une boîte de dialogue Parcourir permet à l’utilisateur de sélectionner un répertoire.</span><span class="sxs-lookup"><span data-stu-id="41a73-105">A Browse dialog box enables the user to select a directory.</span></span> <span data-ttu-id="41a73-106">Le répertoire n’a pas besoin d’exister et peut être créé à l’aide de ce contrôle.</span><span class="sxs-lookup"><span data-stu-id="41a73-106">The directory does not have to exist and may be created by using this control.</span></span>

<span data-ttu-id="41a73-107">Ce type de boîte de dialogue contient généralement les trois contrôles suivants.</span><span class="sxs-lookup"><span data-stu-id="41a73-107">This type of dialog box commonly contains the following three controls.</span></span> <span data-ttu-id="41a73-108">Ces contrôles sont connectés à la même propriété.</span><span class="sxs-lookup"><span data-stu-id="41a73-108">These controls are connected to the same property.</span></span> <span data-ttu-id="41a73-109">Cette propriété est le chemin d’accès sélectionné.</span><span class="sxs-lookup"><span data-stu-id="41a73-109">That property is the path being selected.</span></span>

-   <span data-ttu-id="41a73-110">[Contrôle PathEdit](pathedit-control.md) pour sélectionner la section de fin du chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="41a73-110">A [PathEdit control](pathedit-control.md) to select the tail section of the path.</span></span> <span data-ttu-id="41a73-111">Ce contrôle ne peut pas perdre le focus si la fin entrée n’est pas valide sur le volume présent.</span><span class="sxs-lookup"><span data-stu-id="41a73-111">This control cannot lose focus if the entered tail is not valid on the present volume.</span></span>
-   <span data-ttu-id="41a73-112">[Contrôle DirectoryCombo](directorycombo-control.md) pour afficher le chemin d’accès actuellement sélectionné qui est affiché par le contrôle PathEdit.</span><span class="sxs-lookup"><span data-stu-id="41a73-112">A [DirectoryCombo control](directorycombo-control.md) to show the presently selected path that is displayed by the PathEdit control.</span></span> <span data-ttu-id="41a73-113">Ce contrôle n’affiche pas le dernier segment du chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="41a73-113">This control does not show the last segment of the path.</span></span>
-   <span data-ttu-id="41a73-114">[Contrôle DirectoryList](directorylist-control.md) pour afficher les dossiers situés sous le répertoire actuellement affiché par le DirectoryCombo.</span><span class="sxs-lookup"><span data-stu-id="41a73-114">A [DirectoryList control](directorylist-control.md) to show the folders below the directory currently displayed by the DirectoryCombo.</span></span> <span data-ttu-id="41a73-115">Cela peut également indiquer un dossier qui n’a pas encore été créé.</span><span class="sxs-lookup"><span data-stu-id="41a73-115">This can also show a folder that is not yet created.</span></span>

<span data-ttu-id="41a73-116">Une boîte de dialogue de navigation contient généralement un [contrôle DirectoryCombo](directorycombo-control.md) qui spécifie les types de volumes à afficher.</span><span class="sxs-lookup"><span data-stu-id="41a73-116">A Browse dialog box also usually contains a [DirectoryCombo control](directorycombo-control.md) that specifies the volume types to display.</span></span> <span data-ttu-id="41a73-117">Il est courant que tous les types de volumes s’affichent dans une boîte de dialogue de navigation.</span><span class="sxs-lookup"><span data-stu-id="41a73-117">It is common for all volume types to be displayed on a Browse dialog box.</span></span>

<span data-ttu-id="41a73-118">Les boîtes de dialogue de navigation contiennent généralement trois [contrôles PUSHBUTTON](pushbutton-control.md).</span><span class="sxs-lookup"><span data-stu-id="41a73-118">Browse dialog boxes commonly contain three [PushButton controls](pushbutton-control.md).</span></span> <span data-ttu-id="41a73-119">Ces boutons sont liés à leur ControlEvents respectif dans la [table ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="41a73-119">These buttons are linked to their respective ControlEvents in [ControlEvent table](controlevent-table.md).</span></span> <span data-ttu-id="41a73-120">Ces boutons sont utilisés pour activer les options de contrôle suivantes.</span><span class="sxs-lookup"><span data-stu-id="41a73-120">These buttons are used for activating the following control options.</span></span>



| <span data-ttu-id="41a73-121">Option de contrôle</span><span class="sxs-lookup"><span data-stu-id="41a73-121">Control option</span></span> | <span data-ttu-id="41a73-122">ControlEvent</span><span class="sxs-lookup"><span data-stu-id="41a73-122">ControlEvent</span></span>                                            |
|----------------|---------------------------------------------------------|
| <span data-ttu-id="41a73-123">Dossier parent</span><span class="sxs-lookup"><span data-stu-id="41a73-123">Up One Level</span></span>   | [<span data-ttu-id="41a73-124">DirectoryListUp</span><span class="sxs-lookup"><span data-stu-id="41a73-124">DirectoryListUp</span></span>](directorylistup-controlevent.md)     |
| <span data-ttu-id="41a73-125">Nouveau dossier</span><span class="sxs-lookup"><span data-stu-id="41a73-125">New Folder</span></span>     | [<span data-ttu-id="41a73-126">DirectoryListNew</span><span class="sxs-lookup"><span data-stu-id="41a73-126">DirectoryListNew</span></span>](directorylistnew-controlevent.md)   |
| <span data-ttu-id="41a73-127">Ouvrir</span><span class="sxs-lookup"><span data-stu-id="41a73-127">Open</span></span>           | [<span data-ttu-id="41a73-128">DirectoryListOpen</span><span class="sxs-lookup"><span data-stu-id="41a73-128">DirectoryListOpen</span></span>](directorylistopen-controlevent.md) |



 

<span data-ttu-id="41a73-129">Pour que l’option nouveau dossier fonctionne avec un nom de dossier autre que celui par défaut, le chemin d’accès du nouveau dossier doit être spécifié dans la [table UIText](uitext-table.md).</span><span class="sxs-lookup"><span data-stu-id="41a73-129">For the New Folder option to work with a non-default folder name, the new folder's path must be specified in the [UIText table](uitext-table.md).</span></span> <span data-ttu-id="41a73-130">La chaîne de chemin d’accès doit utiliser le \| format « nom de fichier long du nom de fichier long » pour le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="41a73-130">The path string should use the "short file name\|long file name" form for the file name.</span></span> <span data-ttu-id="41a73-131">Par exemple, utilisez un nom de fichier tel que « MyProd ~ 1 \| My merveilleuse Product ».</span><span class="sxs-lookup"><span data-stu-id="41a73-131">For example, use a file name such as "MyProd~1\|My Fabulous Product".</span></span> <span data-ttu-id="41a73-132">Pour plus d’informations sur le format de nom de fichier, consultez type de données de la colonne [filename](filename.md) .</span><span class="sxs-lookup"><span data-stu-id="41a73-132">See the [Filename](filename.md) column data type for more information about the file name format.</span></span> <span data-ttu-id="41a73-133">Si le chemin d’accès n’est pas présent dans la table UIText, ou s’il est défini sur une valeur non valide, la valeur par défaut est « FLDR \| New Folder ».</span><span class="sxs-lookup"><span data-stu-id="41a73-133">If the path is not present in the UIText table, or if it is set to an invalid value, then it is set to a value of "Fldr\|New Folder" by default.</span></span> <span data-ttu-id="41a73-134">Le bouton **nouveau dossier** peut être omis si la boîte de dialogue ne doit rechercher que des dossiers existants.</span><span class="sxs-lookup"><span data-stu-id="41a73-134">The **New Folder** button can be omitted if the dialog box only need to search for existing folders.</span></span>

 

 



