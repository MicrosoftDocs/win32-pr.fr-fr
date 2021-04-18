---
description: ICE51 vérifie qu’un titre a été fourni pour les fichiers de ressources de police.
ms.assetid: 5a57ba6e-d1fe-44ab-b72d-52b1f212c322
title: ICE51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38082d754564eead6d60a62e3b4cdcf9b1f0f94f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204191"
---
# <a name="ice51"></a><span data-ttu-id="dedb0-103">ICE51</span><span class="sxs-lookup"><span data-stu-id="dedb0-103">ICE51</span></span>

<span data-ttu-id="dedb0-104">ICE51 vérifie qu’un titre a été fourni pour les fichiers de ressources de police.</span><span class="sxs-lookup"><span data-stu-id="dedb0-104">ICE51 checks that a title has been provided for font resource files.</span></span>

<span data-ttu-id="dedb0-105">Vous devez fournir un titre pour une ressource de police qui n’a pas de nom incorporé.</span><span class="sxs-lookup"><span data-stu-id="dedb0-105">You must provide a title for a font resource that does not have an embedded name.</span></span> <span data-ttu-id="dedb0-106">Seuls les fichiers de ressources de polices. TTC,. ttf et. otf ne nécessitent pas de titre, car ces fichiers contiennent un nom incorporé.</span><span class="sxs-lookup"><span data-stu-id="dedb0-106">Only .ttc, .ttf, and .otf font resource files do not require a title, because these files contain an embedded name.</span></span> <span data-ttu-id="dedb0-107">Ne fournissez pas de titre pour une ressource de police qui contient un nom incorporé, car le système enregistre ensuite la police à deux reprises.</span><span class="sxs-lookup"><span data-stu-id="dedb0-107">Do not provide a title for a font resource that contains an embedded name because the system then registers the font twice.</span></span>

<span data-ttu-id="dedb0-108">**[Windows Installer 4,5 et versions antérieures](not-supported-in-windows-installer-4-5.md):** ICE51 ne vérifie pas les fichiers de ressources de police. otf.</span><span class="sxs-lookup"><span data-stu-id="dedb0-108">**[Windows Installer 4.5 and earlier](not-supported-in-windows-installer-4-5.md):** ICE51 does not check .otf font resource files.</span></span>

## <a name="result"></a><span data-ttu-id="dedb0-109">Résultats</span><span class="sxs-lookup"><span data-stu-id="dedb0-109">Result</span></span>

<span data-ttu-id="dedb0-110">ICE51 publie une erreur s’il existe des fichiers de ressources de police. TTC,. ttf et. OTF avec des titres.</span><span class="sxs-lookup"><span data-stu-id="dedb0-110">ICE51 posts an error if there are any .ttc, .ttf, and .otf font resource files with titles.</span></span> <span data-ttu-id="dedb0-111">ICE51 publie un avertissement s’il existe d’autres fichiers de ressources de police sans titre.</span><span class="sxs-lookup"><span data-stu-id="dedb0-111">ICE51 posts a warning if there are any other font resource files without a title.</span></span>

## <a name="example"></a><span data-ttu-id="dedb0-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="dedb0-112">Example</span></span>

<span data-ttu-id="dedb0-113">ICE51 signale l’avertissement suivant pour l’exemple indiqué.</span><span class="sxs-lookup"><span data-stu-id="dedb0-113">ICE51 would report the following warning for the example shown.</span></span>

``` syntax
Font 'Font1' is a TTC\TTF\OTF font, but also has a title.
```

<span data-ttu-id="dedb0-114">ICE51 signale le message d’erreur suivant pour l’exemple indiqué.</span><span class="sxs-lookup"><span data-stu-id="dedb0-114">ICE51 would report the following error message for the example shown.</span></span>

``` syntax
Font 'Font2' does not have a title. Only TTC\TTF\OTF fonts do not need titles.
```

<span data-ttu-id="dedb0-115">[Table de fichiers](file-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="dedb0-115">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="dedb0-116">Fichier</span><span class="sxs-lookup"><span data-stu-id="dedb0-116">File</span></span>  | <span data-ttu-id="dedb0-117">FileName</span><span class="sxs-lookup"><span data-stu-id="dedb0-117">FileName</span></span>  |
|-------|-----------|
| <span data-ttu-id="dedb0-118">Font1</span><span class="sxs-lookup"><span data-stu-id="dedb0-118">Font1</span></span> | <span data-ttu-id="dedb0-119">font1. ttf</span><span class="sxs-lookup"><span data-stu-id="dedb0-119">font1.ttf</span></span> |
| <span data-ttu-id="dedb0-120">Font2</span><span class="sxs-lookup"><span data-stu-id="dedb0-120">Font2</span></span> | <span data-ttu-id="dedb0-121">Font2. fon</span><span class="sxs-lookup"><span data-stu-id="dedb0-121">font2.fon</span></span> |



 

[<span data-ttu-id="dedb0-122">Tableau des polices</span><span class="sxs-lookup"><span data-stu-id="dedb0-122">Font Table</span></span>](font-table.md)



| <span data-ttu-id="dedb0-123">fichier\_</span><span class="sxs-lookup"><span data-stu-id="dedb0-123">File\_</span></span> | <span data-ttu-id="dedb0-124">FontTitle</span><span class="sxs-lookup"><span data-stu-id="dedb0-124">FontTitle</span></span>          |
|--------|--------------------|
| <span data-ttu-id="dedb0-125">Font1</span><span class="sxs-lookup"><span data-stu-id="dedb0-125">Font1</span></span>  | <span data-ttu-id="dedb0-126">Police vraiment cool</span><span class="sxs-lookup"><span data-stu-id="dedb0-126">A Really Cool Font</span></span> |
| <span data-ttu-id="dedb0-127">Font2</span><span class="sxs-lookup"><span data-stu-id="dedb0-127">Font2</span></span>  |                    |



 

## <a name="related-topics"></a><span data-ttu-id="dedb0-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dedb0-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dedb0-129">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="dedb0-129">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



