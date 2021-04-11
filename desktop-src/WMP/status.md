---
title: État (kit de développement logiciel Windows Media Player)
description: Statut
ms.assetid: b8d6d026-819c-4889-a894-c82fe81ec922
keywords:
- Apparences mobiles du lecteur Windows Media, affichage de l’État
- apparences, affichage de l’État
- référence pour les apparences, affichage de l’État
- affichage de l’État dans les apparences, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6f1cd9e0df209d6a37ed880765fd607e939765
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104032181"
---
# <a name="status-windows-media-player-sdk"></a><span data-ttu-id="ad068-107">État (kit de développement logiciel Windows Media Player)</span><span class="sxs-lookup"><span data-stu-id="ad068-107">Status (Windows Media Player SDK)</span></span>

<span data-ttu-id="ad068-108">Vous souhaiterez peut-être utiliser un affichage d’État dans votre apparence.</span><span class="sxs-lookup"><span data-stu-id="ad068-108">You may want to use a status display in your skin.</span></span> <span data-ttu-id="ad068-109">Si c’est le cas, l’élément Status doit être défini dans le fichier de définition d’apparence.</span><span class="sxs-lookup"><span data-stu-id="ad068-109">If so, the status element must be defined in the skin definition file.</span></span> <span data-ttu-id="ad068-110">Vous pouvez également afficher ces informations à l’aide de l’attribut Status dans l’élément de texte.</span><span class="sxs-lookup"><span data-stu-id="ad068-110">As an alternative, you may also display this information by using the Status attribute in the Text element.</span></span>

<span data-ttu-id="ad068-111">La section d’État du fichier de définition d’apparence commence par cette ligne :</span><span class="sxs-lookup"><span data-stu-id="ad068-111">The Status section of the skin definition file begins with this line:</span></span>


```C++
[ Status ]

```



<span data-ttu-id="ad068-112">Vous devez ensuite ajouter une ou plusieurs lignes qui contiennent des informations sur l’affichage de l’État dans votre apparence.</span><span class="sxs-lookup"><span data-stu-id="ad068-112">You then must add one or more lines that contain information about the status display in your skin.</span></span>


```C++
    On           45,193,120,13    Left    Tahoma,8,B        0,255,  0

```



<span data-ttu-id="ad068-113">Vous pouvez utiliser le modèle suivant pour la section État de votre fichier de définition d’apparence :</span><span class="sxs-lookup"><span data-stu-id="ad068-113">You can use the following template for the Status section of your skin definition file:</span></span>


```C++
//  <Item>       <Location>     <Align>  <Font>          <Color>
//  ------       ----------     -------  ------          -------

```



<span data-ttu-id="ad068-114">Vous devez utiliser l’ordre indiqué dans le modèle précédent pour obtenir des informations sur l’affichage de l’état de chaque ligne de la section État.</span><span class="sxs-lookup"><span data-stu-id="ad068-114">You must use the order shown in the preceding template for status display information for each line in the Status section.</span></span> <span data-ttu-id="ad068-115">Chaque partie de la ligne est requise.</span><span class="sxs-lookup"><span data-stu-id="ad068-115">Each part of the line is required.</span></span> <span data-ttu-id="ad068-116">Les sections suivantes décrivent chaque élément :</span><span class="sxs-lookup"><span data-stu-id="ad068-116">The following sections describe each item:</span></span>

-   [<span data-ttu-id="ad068-117">Élément d'état</span><span class="sxs-lookup"><span data-stu-id="ad068-117">Status Item</span></span>](status-item.md)
-   [<span data-ttu-id="ad068-118">Emplacement de l’État</span><span class="sxs-lookup"><span data-stu-id="ad068-118">Status Location</span></span>](status-location.md)
-   [<span data-ttu-id="ad068-119">Alignement de l’État</span><span class="sxs-lookup"><span data-stu-id="ad068-119">Status Alignment</span></span>](status-alignment.md)
-   [<span data-ttu-id="ad068-120">Police d’État</span><span class="sxs-lookup"><span data-stu-id="ad068-120">Status Font</span></span>](status-font.md)
-   [<span data-ttu-id="ad068-121">Couleur d’État</span><span class="sxs-lookup"><span data-stu-id="ad068-121">Status Color</span></span>](status-color.md)

<span data-ttu-id="ad068-122">Pour obtenir un exemple de code d’État, consultez la [section exemple d’État](sample-status-section.md).</span><span class="sxs-lookup"><span data-stu-id="ad068-122">For an example of Status code, see [Sample Status Section](sample-status-section.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ad068-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ad068-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad068-124">**Référence d’apparence**</span><span class="sxs-lookup"><span data-stu-id="ad068-124">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




