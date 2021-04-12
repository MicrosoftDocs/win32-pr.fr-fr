---
title: Imbrication de refichiers
description: Imbrication de refichiers
ms.assetid: fa355c98-31e2-4bb9-ad67-fd9a727300c3
keywords:
- Fichiers Windows Media, imbrication
- Fichiers Windows Media, référencement d’autres sous-fichiers
- imbrication de refichiers
- refichiers, imbrication
- les sous-fichiers, qui font référence à d’autres sous-fichiers
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3cd5743424858c4bbcd6f66952f4275ea82d947e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309329"
---
# <a name="nesting-metafiles"></a><span data-ttu-id="6fa8a-108">Imbrication de refichiers</span><span class="sxs-lookup"><span data-stu-id="6fa8a-108">Nesting Metafiles</span></span>

<span data-ttu-id="6fa8a-109">Un métafichier peut faire référence à un autre métafichier.</span><span class="sxs-lookup"><span data-stu-id="6fa8a-109">A metafile can reference another metafile.</span></span> <span data-ttu-id="6fa8a-110">Pour référencer un autre métafichier, utilisez l’élément **ENTRYREF** .</span><span class="sxs-lookup"><span data-stu-id="6fa8a-110">To reference another metafile, use the **ENTRYREF** element.</span></span> <span data-ttu-id="6fa8a-111">Un élément **ENTRYREF** dans le métafichier principal pointe vers un métafichier externe.</span><span class="sxs-lookup"><span data-stu-id="6fa8a-111">An **ENTRYREF** element in the primary metafile points to an external metafile.</span></span>

<span data-ttu-id="6fa8a-112">Le contrôle du lecteur Windows Media traite les éléments d' **entrée** du métafichier référencé comme s’ils étaient inclus dans le métafichier principal à la position de l’élément **ENTRYREF** .</span><span class="sxs-lookup"><span data-stu-id="6fa8a-112">The Windows Media Player control processes the **ENTRY** elements of the referenced metafile as if they were included in the primary metafile at the position of the **ENTRYREF** element.</span></span> <span data-ttu-id="6fa8a-113">Toutefois, elle ignore tous les éléments d' **entrée** dans le métafichier référencé dont l’attribut **SKIPIFREF** a la valeur Yes.</span><span class="sxs-lookup"><span data-stu-id="6fa8a-113">However, it skips any **ENTRY** elements in the referenced metafile that have the **SKIPIFREF** attribute set to YES.</span></span>

<span data-ttu-id="6fa8a-114">Les contrôles Windows Media Player 7,0, 7,1 et Windows Media Player pour Windows XP ignorent tous les éléments **ENTRYREF** dans le métafichier référencé.</span><span class="sxs-lookup"><span data-stu-id="6fa8a-114">The Windows Media Player 7.0, 7.1, and Windows Media Player for Windows XP controls ignore any **ENTRYREF** elements in the referenced metafile.</span></span> <span data-ttu-id="6fa8a-115">Par conséquent, les fichiers de conversions ne peuvent être imbriqués qu’un niveau profond à l’aide de ces versions.</span><span class="sxs-lookup"><span data-stu-id="6fa8a-115">Thus, metafiles can only be nested one level deep using these versions.</span></span> <span data-ttu-id="6fa8a-116">Ces versions ignorent également l’élément **ASX** et ses attributs dans le fichier référencé.</span><span class="sxs-lookup"><span data-stu-id="6fa8a-116">These versions also ignore the **ASX** element and its attributes in the referenced file.</span></span> <span data-ttu-id="6fa8a-117">Le lecteur Windows Media série 9 ou version ultérieure prend en charge l’imbrication de fichiers de permétrage jusqu’à 5 de profondeur.</span><span class="sxs-lookup"><span data-stu-id="6fa8a-117">Windows Media Player 9 Series or later supports nesting metafiles up to 5 deep.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6fa8a-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6fa8a-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6fa8a-119">**Création de sélections de métafichiers**</span><span class="sxs-lookup"><span data-stu-id="6fa8a-119">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> </dl>

 

 




