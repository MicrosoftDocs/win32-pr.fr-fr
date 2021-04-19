---
description: ICE07 valide le fait que le package d’installation spécifie que les polices doivent être installées dans le FontsFolder. Si une police est installée dans un dossier autre que le FontsFolder, le programme d’installation crée un raccourci plutôt que d’installer réellement la police.
ms.assetid: aa51b077-fb7b-4e09-9de1-ef1905144a94
title: ICE07
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80a79bcb681a57bb09ff235b35a5287492a4f39c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524301"
---
# <a name="ice07"></a><span data-ttu-id="a17c4-104">ICE07</span><span class="sxs-lookup"><span data-stu-id="a17c4-104">ICE07</span></span>

<span data-ttu-id="a17c4-105">ICE07 valide le fait que le package d’installation spécifie que les polices doivent être installées dans le FontsFolder.</span><span class="sxs-lookup"><span data-stu-id="a17c4-105">ICE07 validates that installation package specifies that fonts be installed into the FontsFolder.</span></span> <span data-ttu-id="a17c4-106">Si une police est installée dans un dossier autre que le FontsFolder, le programme d’installation crée un raccourci plutôt que d’installer réellement la police.</span><span class="sxs-lookup"><span data-stu-id="a17c4-106">If a font is installed to a folder other than the FontsFolder the installer creates a shortcut rather than actually installing the font.</span></span>

<span data-ttu-id="a17c4-107">L’action personnalisée ICE07 effectue les opérations suivantes pour chaque police de la [table de polices](font-table.md).</span><span class="sxs-lookup"><span data-stu-id="a17c4-107">The ICE07 custom action does the following for each font in the [Font table](font-table.md).</span></span>

1.  <span data-ttu-id="a17c4-108">Recherche le fichier de police auquel chaque titre de police appartient à l’aide de la [table de polices](font-table.md).</span><span class="sxs-lookup"><span data-stu-id="a17c4-108">Finds the font file to which each font title belongs using the [Font table](font-table.md).</span></span>
2.  <span data-ttu-id="a17c4-109">Interroge la \_ colonne de composant de la [table de fichiers](file-table.md) pour le composant qui contrôle chaque fichier.</span><span class="sxs-lookup"><span data-stu-id="a17c4-109">Queries the Component\_ column of the [File table](file-table.md) for the component that controls each file.</span></span>
3.  <span data-ttu-id="a17c4-110">Interroge la \_ colonne Directory de la [table Component](component-table.md) pour obtenir une clé dans la table de répertoires.</span><span class="sxs-lookup"><span data-stu-id="a17c4-110">Queries the Directory\_ column of the [Component table](component-table.md) to obtain a key into the Directory table.</span></span>
4.  <span data-ttu-id="a17c4-111">Résout la [table de répertoire](directory-table.md) pour déterminer le nom du dossier dans lequel le programme d’installation doit installer le fichier de police</span><span class="sxs-lookup"><span data-stu-id="a17c4-111">Resolves the [Directory table](directory-table.md) to determine the name of the folder into which the installer is to install the font file</span></span>
5.  <span data-ttu-id="a17c4-112">Publie une erreur si le fichier de police est en cours d’installation dans un dossier autre que FontsFolder.</span><span class="sxs-lookup"><span data-stu-id="a17c4-112">Posts an error if the font file is being installed into a folder other than the FontsFolder.</span></span>

## <a name="result"></a><span data-ttu-id="a17c4-113">Résultats</span><span class="sxs-lookup"><span data-stu-id="a17c4-113">Result</span></span>

<span data-ttu-id="a17c4-114">ICE07 publie une erreur s’il détecte que la base de données spécifie qu’un fichier de polices doit être installé dans un dossier autre que FontsFolder.</span><span class="sxs-lookup"><span data-stu-id="a17c4-114">ICE07 posts an error if it finds that the database specifies that a font file be installed into a folder other than the FontsFolder.</span></span>

## <a name="example"></a><span data-ttu-id="a17c4-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="a17c4-115">Example</span></span>

<span data-ttu-id="a17c4-116">IC07 publie le message d’erreur suivant pour l’exemple indiqué.</span><span class="sxs-lookup"><span data-stu-id="a17c4-116">IC07 would post the following error message for the example shown.</span></span>

``` syntax
'Tahoma' is a font and must be installed to the FontsFolder directory. Current Install Directory: 'Sandbar'.
```

[<span data-ttu-id="a17c4-117">Tableau des polices</span><span class="sxs-lookup"><span data-stu-id="a17c4-117">Font Table</span></span>](font-table.md)



| <span data-ttu-id="a17c4-118">fichier\_</span><span class="sxs-lookup"><span data-stu-id="a17c4-118">File\_</span></span> | <span data-ttu-id="a17c4-119">FontTitle</span><span class="sxs-lookup"><span data-stu-id="a17c4-119">FontTitle</span></span> |
|--------|-----------|
| <span data-ttu-id="a17c4-120">Myrtle</span><span class="sxs-lookup"><span data-stu-id="a17c4-120">Myrtle</span></span> | <span data-ttu-id="a17c4-121">Tahoma</span><span class="sxs-lookup"><span data-stu-id="a17c4-121">Tahoma</span></span>    |



 

<span data-ttu-id="a17c4-122">[Table de fichiers](file-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="a17c4-122">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="a17c4-123">Fichier</span><span class="sxs-lookup"><span data-stu-id="a17c4-123">File</span></span>   | <span data-ttu-id="a17c4-124">-\_</span><span class="sxs-lookup"><span data-stu-id="a17c4-124">Component\_</span></span>   |
|--------|---------------|
| <span data-ttu-id="a17c4-125">Myrtle</span><span class="sxs-lookup"><span data-stu-id="a17c4-125">Myrtle</span></span> | <span data-ttu-id="a17c4-126">Myrtle \_ Beach</span><span class="sxs-lookup"><span data-stu-id="a17c4-126">Myrtle\_Beach</span></span> |



 

<span data-ttu-id="a17c4-127">[Table des composants](component-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="a17c4-127">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="a17c4-128">Composant</span><span class="sxs-lookup"><span data-stu-id="a17c4-128">Component</span></span>     | <span data-ttu-id="a17c4-129">Répertoire\_</span><span class="sxs-lookup"><span data-stu-id="a17c4-129">Directory\_</span></span> |
|---------------|-------------|
| <span data-ttu-id="a17c4-130">Myrtle \_ Beach</span><span class="sxs-lookup"><span data-stu-id="a17c4-130">Myrtle\_Beach</span></span> | <span data-ttu-id="a17c4-131">SandBar</span><span class="sxs-lookup"><span data-stu-id="a17c4-131">SandBar</span></span>     |



 

<span data-ttu-id="a17c4-132">Dans cet exemple, la police Tahoma est mappée au fichier de polices Myrtle.</span><span class="sxs-lookup"><span data-stu-id="a17c4-132">In this example, the font Tahoma maps to the font file Myrtle.</span></span> <span data-ttu-id="a17c4-133">Le fichier Myrtle appartient au composant Myrtle \_ Beach.</span><span class="sxs-lookup"><span data-stu-id="a17c4-133">The file Myrtle belongs to the component Myrtle\_Beach.</span></span> <span data-ttu-id="a17c4-134">La résolution de la table d’annuaires indique que tous les fichiers appartenant à Myrtle \_ Beach doivent être installés dans le dossier Sandbar.</span><span class="sxs-lookup"><span data-stu-id="a17c4-134">Resolution of the Directory table shows that all the files belonging to Myrtle\_Beach are to be installed in the Sandbar folder.</span></span> <span data-ttu-id="a17c4-135">Comme il ne s’agit pas du FontsFolder, ICE07 publie un message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="a17c4-135">Because this is not the FontsFolder, ICE07 posts an error message.</span></span>

<span data-ttu-id="a17c4-136">Notez que si le composant Myrtle \_ Beach appartient dans le dossier Sandbar, et non dans le FontsFolder, la police Tahoma ne peut pas appartenir à Myrtle \_ Beach.</span><span class="sxs-lookup"><span data-stu-id="a17c4-136">Note that if the component Myrtle\_Beach really belongs in the Sandbar folder, and not the FontsFolder, then the font Tahoma may not belong in Myrtle\_Beach.</span></span> <span data-ttu-id="a17c4-137">Un correctif possible pour l’erreur consisterait à inclure Tahoma dans un autre composant qui est installé dans le répertoire FontsFolder.</span><span class="sxs-lookup"><span data-stu-id="a17c4-137">A possible fix for the error would be to include Tahoma in another component that does get installed in the FontsFolder directory.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a17c4-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a17c4-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a17c4-139">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="a17c4-139">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



