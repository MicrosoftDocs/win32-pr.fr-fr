---
description: Polices de plusieurs fichiers de ressources
ms.assetid: 4625fe62-d55d-4828-9174-975a731a8f62
title: Polices de plusieurs fichiers de ressources
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3802705ba4b199fa00d2cc2961d3c4472c4e365
ms.sourcegitcommit: fa5c081bf792b119a7bb92182cde1f85ca75967b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/17/2021
ms.locfileid: "104996448"
---
# <a name="fonts-from-multiple-resource-files"></a><span data-ttu-id="fbd6a-103">Polices de plusieurs fichiers de ressources</span><span class="sxs-lookup"><span data-stu-id="fbd6a-103">Fonts from Multiple Resource Files</span></span>

<span data-ttu-id="fbd6a-104">En règle générale, une police est contenue dans un fichier de ressources de police unique.</span><span class="sxs-lookup"><span data-stu-id="fbd6a-104">Typically, a font is contained in a single font resource file.</span></span> <span data-ttu-id="fbd6a-105">Toutefois, les informations de certaines polices sont réparties entre plusieurs fichiers.</span><span class="sxs-lookup"><span data-stu-id="fbd6a-105">However, the information for some fonts is spread among several files.</span></span> <span data-ttu-id="fbd6a-106">Par exemple, tapez 1 plusieurs polices principales requièrent deux fichiers :</span><span class="sxs-lookup"><span data-stu-id="fbd6a-106">For example, Type 1 multiple master fonts require two files:</span></span>

-   <span data-ttu-id="fbd6a-107">. PFM pour les métriques de police</span><span class="sxs-lookup"><span data-stu-id="fbd6a-107">.pfm for the font metrics</span></span>
-   <span data-ttu-id="fbd6a-108">. PFB pour les bits de police</span><span class="sxs-lookup"><span data-stu-id="fbd6a-108">.pfb for the font bits</span></span>

<span data-ttu-id="fbd6a-109">Pour ajouter une police de plusieurs fichiers au système, utilisez les fonctions [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) ou [**AddFontResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa) .</span><span class="sxs-lookup"><span data-stu-id="fbd6a-109">To add a font from multiple files to the system, use the [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) or [**AddFontResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa) functions.</span></span> <span data-ttu-id="fbd6a-110">Le paramètre *lpszFilename* dans ces fonctions doit pointer vers une chaîne qui contient les noms de fichiers séparés par la barre verticale ou le canal ( \| ).</span><span class="sxs-lookup"><span data-stu-id="fbd6a-110">The *lpszFilename* parameter in these functions must point to a string that contains the file names separated by the vertical bar or pipe ( \| ).</span></span> <span data-ttu-id="fbd6a-111">Par exemple, pour spécifier abcxxxxx. PFM et abcxxxxx. PFB pour une police de type 1, utilisez la chaîne « abcxxxxx. PFM \| abcxxxxx. PFB ».</span><span class="sxs-lookup"><span data-stu-id="fbd6a-111">For example, to specify abcxxxxx.pfm and abcxxxxx.pfb for a Type 1 font, use the string "abcxxxxx.pfm \| abcxxxxx.pfb."</span></span>

<span data-ttu-id="fbd6a-112">[**AddFontResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa) diffère de [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) en ce que l’application qui appelle **AddFontResourceEx** peut spécifier la police comme étant privée ou non énumérable.</span><span class="sxs-lookup"><span data-stu-id="fbd6a-112">[**AddFontResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa) differs from [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) in that the application calling **AddFontResourceEx** can specify the font as private to itself or non-enumerable.</span></span>

<span data-ttu-id="fbd6a-113">Pour ajouter une police à partir d’une image mémoire, utilisez [**AddFontMemResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontmemresourceex).</span><span class="sxs-lookup"><span data-stu-id="fbd6a-113">To add a font from a memory image, use [**AddFontMemResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontmemresourceex).</span></span> <span data-ttu-id="fbd6a-114">Cela permet à une application d’utiliser une police incorporée dans un document ou une page Web.</span><span class="sxs-lookup"><span data-stu-id="fbd6a-114">This allows an application to use a font that is embedded in a document or a webpage.</span></span>

<span data-ttu-id="fbd6a-115">Pour supprimer une police provenant de plusieurs fichiers de ressources, appelez [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) ou [**RemoveFontResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourceexa), selon la fonction utilisée pour ajouter la police.</span><span class="sxs-lookup"><span data-stu-id="fbd6a-115">To remove a font that came from multiple resource files, call [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) or [**RemoveFontResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourceexa), depending on the function used to add the font.</span></span> <span data-ttu-id="fbd6a-116">Vous devez spécifier les mêmes indicateurs que ceux utilisés pour ajouter la police.</span><span class="sxs-lookup"><span data-stu-id="fbd6a-116">You must specify the same flags that were used to add the font.</span></span> <span data-ttu-id="fbd6a-117">Pour supprimer une police qui a été ajoutée à partir d’une image mémoire, utilisez [**RemoveFontMemResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontmemresourceex).</span><span class="sxs-lookup"><span data-stu-id="fbd6a-117">To remove a font that was added from a memory image, use [**RemoveFontMemResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontmemresourceex).</span></span>

<span data-ttu-id="fbd6a-118">L’utilisation d’une police qui provient de plusieurs fichiers de ressources de police est identique à l’utilisation d’une police d’un fichier de ressources unique.</span><span class="sxs-lookup"><span data-stu-id="fbd6a-118">Using a font that comes from multiple font-resource files is identical to using a font from a single resource file.</span></span>

 

 
