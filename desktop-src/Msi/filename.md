---
description: Le type de données filename est une chaîne de texte contenant un nom de fichier ou un dossier.
ms.assetid: af59e1b8-0699-4031-895f-415752611e21
title: Nom de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fc049fa0808efc180afbd715e311a124bfdada9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528191"
---
# <a name="filename"></a><span data-ttu-id="04a99-103">Nom de fichier</span><span class="sxs-lookup"><span data-stu-id="04a99-103">Filename</span></span>

<span data-ttu-id="04a99-104">Le type de données filename est une chaîne de texte contenant un nom de fichier ou un dossier.</span><span class="sxs-lookup"><span data-stu-id="04a99-104">The Filename data type is a text string containing a file name or folder.</span></span> <span data-ttu-id="04a99-105">Par défaut, le nom de fichier est supposé utiliser la syntaxe de nom de fichier Short. c’est-à-dire, le nom de huit caractères, le point (.) et l’extension de 3 caractères.</span><span class="sxs-lookup"><span data-stu-id="04a99-105">By default, the file name is assumed to use short file name syntax; that is, eight-character name, period (.), and 3-character extension.</span></span> <span data-ttu-id="04a99-106">Un nom de fichier Short doit toujours être fourni, car la propriété [**SHORTFILENAMES**](shortfilenames.md) peut être définie ou le volume cible pour l’installation peut uniquement prendre en charge les noms de fichiers courts.</span><span class="sxs-lookup"><span data-stu-id="04a99-106">A short file name must always be provided because the [**SHORTFILENAMES**](shortfilenames.md) property may be set or the target volume for the installation may only support short file names.</span></span>

<span data-ttu-id="04a99-107">Pour inclure un nom de fichier long avec le nom de fichier Short, séparez-le du nom de fichier Short par une barre verticale ( \| ).</span><span class="sxs-lookup"><span data-stu-id="04a99-107">To include a long file name with the short file name, separate it from the short file name with a vertical bar (\|).</span></span>

<span data-ttu-id="04a99-108">Par exemple, les deux chaînes suivantes sont valides :</span><span class="sxs-lookup"><span data-stu-id="04a99-108">For example, the following two strings are valid:</span></span>

-   <span data-ttu-id="04a99-109">status.txt</span><span class="sxs-lookup"><span data-stu-id="04a99-109">status.txt</span></span>
-   <span data-ttu-id="04a99-110">Project ~1.txt\| Status.txt de projet</span><span class="sxs-lookup"><span data-stu-id="04a99-110">projec~1.txt\|Project Status.txt</span></span>

<span data-ttu-id="04a99-111">Les noms de fichiers courts et longs ne doivent pas contenir les caractères suivants :</span><span class="sxs-lookup"><span data-stu-id="04a99-111">Short and long file names must not contain the following characters:</span></span>

-   <span data-ttu-id="04a99-112">barre oblique (/) ou ( \\ )</span><span class="sxs-lookup"><span data-stu-id="04a99-112">slash (/) or (\\)</span></span>
-   <span data-ttu-id="04a99-113">point d’interrogation ( ?)</span><span class="sxs-lookup"><span data-stu-id="04a99-113">question mark (?)</span></span>
-   <span data-ttu-id="04a99-114">barre verticale ( \| )</span><span class="sxs-lookup"><span data-stu-id="04a99-114">vertical bar (\|)</span></span>
-   <span data-ttu-id="04a99-115">Chevron droit (>)</span><span class="sxs-lookup"><span data-stu-id="04a99-115">right angle bracket (>)</span></span>
-   <span data-ttu-id="04a99-116">Chevron gauche (<)</span><span class="sxs-lookup"><span data-stu-id="04a99-116">left angle bracket (<)</span></span>
-   <span data-ttu-id="04a99-117">deux-points ( :)</span><span class="sxs-lookup"><span data-stu-id="04a99-117">colon (:)</span></span>
-   <span data-ttu-id="04a99-118">astérisque ( \* )</span><span class="sxs-lookup"><span data-stu-id="04a99-118">asterisk (\*)</span></span>
-   <span data-ttu-id="04a99-119">guillemet (")</span><span class="sxs-lookup"><span data-stu-id="04a99-119">quotation mark (")</span></span>

<span data-ttu-id="04a99-120">En outre, les noms de fichiers courts ne doivent pas contenir les caractères suivants :</span><span class="sxs-lookup"><span data-stu-id="04a99-120">In addition, short file names must not contain the following characters:</span></span>

-   <span data-ttu-id="04a99-121">signe plus (+)</span><span class="sxs-lookup"><span data-stu-id="04a99-121">plus sign (+)</span></span>
-   <span data-ttu-id="04a99-122">virgule (,)</span><span class="sxs-lookup"><span data-stu-id="04a99-122">comma (,)</span></span>
-   <span data-ttu-id="04a99-123">point-virgule (;)</span><span class="sxs-lookup"><span data-stu-id="04a99-123">semicolon (;)</span></span>
-   <span data-ttu-id="04a99-124">signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="04a99-124">equals sign (=)</span></span>
-   <span data-ttu-id="04a99-125">crochet gauche ( \[ )</span><span class="sxs-lookup"><span data-stu-id="04a99-125">left square bracket (\[)</span></span>
-   <span data-ttu-id="04a99-126">crochet droit ( \] )</span><span class="sxs-lookup"><span data-stu-id="04a99-126">right square bracket (\])</span></span>

<span data-ttu-id="04a99-127">Aucun espace n’est autorisé avant le séparateur de barre verticale ( \| ) pour la syntaxe de nom de fichier ou de nom de fichier long.</span><span class="sxs-lookup"><span data-stu-id="04a99-127">No space is allowed preceding the vertical bar (\|) separator for the short file name/long file name syntax.</span></span> <span data-ttu-id="04a99-128">Les noms de fichiers courts ne peuvent pas inclure d’espace, bien qu’un nom de fichier long puisse l’être.</span><span class="sxs-lookup"><span data-stu-id="04a99-128">Short file names may not include a space, although a long file name may.</span></span> <span data-ttu-id="04a99-129">Un espace peut exister après le séparateur uniquement si le nom de fichier long du nom de fichier commence par l’espace.</span><span class="sxs-lookup"><span data-stu-id="04a99-129">A space can exist after the separator only if the long file name of the file name begins with the space.</span></span> <span data-ttu-id="04a99-130">Aucune syntaxe de chemin d’accès complet n’est autorisée.</span><span class="sxs-lookup"><span data-stu-id="04a99-130">No full-path syntax is allowed.</span></span>

> [!Note]  
> <span data-ttu-id="04a99-131">Le format de la colonne de nom de fichier de la table [MsiEmbeddedUI](msiembeddedui-table.md) est semblable au type de données format FileName, sauf que le séparateur de barre verticale ( \| ) pour la syntaxe de nom de fichier ou de nom de fichier long n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="04a99-131">The format of the FileName column of the [MsiEmbeddedUI](msiembeddedui-table.md) table is like the format Filename data type except that the vertical bar (\|) separator for the short file name/long file name syntax is not available.</span></span>

 

 

 



