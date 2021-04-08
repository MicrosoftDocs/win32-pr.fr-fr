---
title: Apparences du lecteur Windows Media
description: Apparences du lecteur Windows Media
ms.assetid: 0cd23497-9a47-4391-a2c1-0e3102dcc1d2
keywords:
- Lecteur Windows Media, habillages
- Apparences du lecteur Windows Media, à propos de
- apparences, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e649a3a3708a04af5c21d059c3f06b5badc815d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839814"
---
# <a name="windows-media-player-skins"></a><span data-ttu-id="7384f-106">Apparences du lecteur Windows Media</span><span class="sxs-lookup"><span data-stu-id="7384f-106">Windows Media Player Skins</span></span>

<span data-ttu-id="7384f-107">Le lecteur Windows Media fournit une plateforme de programmation pour créer des apparences personnalisées.</span><span class="sxs-lookup"><span data-stu-id="7384f-107">Windows Media Player provides a programming platform to create custom skins.</span></span> <span data-ttu-id="7384f-108">Les apparences sont des ensembles de scripts, d’images, de fichiers multimédias et de fichiers texte qui peuvent être combinés pour créer une nouvelle apparence pour le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="7384f-108">Skins are sets of scripts, art, media, and text files that can be combined to create a new appearance for Windows Media Player.</span></span> <span data-ttu-id="7384f-109">À l’aide des apparences, vous pouvez modifier non seulement la façon dont le lecteur Windows Media se présente, mais également comment il fonctionne.</span><span class="sxs-lookup"><span data-stu-id="7384f-109">Using skins, you can change not only the way Windows Media Player looks, but how it functions.</span></span> <span data-ttu-id="7384f-110">Pas seulement où se trouvent les boutons et à quoi ils ressemblent, mais ce qu’ils font, en raison des limites de la technologie principale du lecteur Windows Media sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="7384f-110">Not just where the knobs are and what they look like, but what they do, given the limits of the underlying Windows Media Player core technology.</span></span>

<span data-ttu-id="7384f-111">La technologie d’apparence est très différente des autres types de programmation. Fondamentalement, vous allez mélanger la programmation et l’art dans des parties égales.</span><span class="sxs-lookup"><span data-stu-id="7384f-111">Skin technology is very different from other kinds of programming; essentially you will be mixing programming and art in equal parts.</span></span> <span data-ttu-id="7384f-112">Vous n’avez pas besoin d’être un programmeur d’experts (pas beaucoup plus que vous ne savez déjà si vous avez créé des pages Web et effectué des scripts simples). vous n’avez pas non plus besoin d’être un artiste (tant que vous pouvez utiliser une application de modification graphique).</span><span class="sxs-lookup"><span data-stu-id="7384f-112">You do not need to be an expert programmer (not much more than you already know if you have created webpages and done some simple scripting), nor do you need to be an artist (as long as you can use a graphics editing application).</span></span> <span data-ttu-id="7384f-113">Vous utiliserez XML (comme HTML), Microsoft JScript et les programmes que vous choisissez.</span><span class="sxs-lookup"><span data-stu-id="7384f-113">You'll be using XML (similar to HTML), Microsoft JScript, and whatever art programs you choose.</span></span>

<span data-ttu-id="7384f-114">La documentation sur les habillages contient les quatre sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="7384f-114">The skins documentation contains the following four sections.</span></span>



| <span data-ttu-id="7384f-115">Section</span><span class="sxs-lookup"><span data-stu-id="7384f-115">Section</span></span>                                                                    | <span data-ttu-id="7384f-116">Description</span><span class="sxs-lookup"><span data-stu-id="7384f-116">Description</span></span>                                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7384f-117">À propos des apparences</span><span class="sxs-lookup"><span data-stu-id="7384f-117">About Skins</span></span>](about-skins.md)                                             | <span data-ttu-id="7384f-118">Discute de la théorie des habillages en termes abstraits.</span><span class="sxs-lookup"><span data-stu-id="7384f-118">Discusses the theory of skins in abstract terms.</span></span> <span data-ttu-id="7384f-119">Nous vous conseillons de consulter au moins cette section, car la technologie Skin est tellement différente des autres types de programmation.</span><span class="sxs-lookup"><span data-stu-id="7384f-119">You are advised to at least browse this section because skin technology is so different from other kinds of programming.</span></span> <span data-ttu-id="7384f-120">Cette section vous explique pourquoi et comment les choses fonctionnent, mais ne présente que les détails.</span><span class="sxs-lookup"><span data-stu-id="7384f-120">This section tells you why and how things work, but only skims over the details.</span></span>                                             |
| [<span data-ttu-id="7384f-121">Guide de création d’apparence</span><span class="sxs-lookup"><span data-stu-id="7384f-121">Skin Creation Guide</span></span>](skin-creation-guide.md)                             | <span data-ttu-id="7384f-122">Explique ce que vous devez faire pour créer une apparence.</span><span class="sxs-lookup"><span data-stu-id="7384f-122">Explains what you need to do to create a skin.</span></span> <span data-ttu-id="7384f-123">Vous souhaiterez probablement lire cette section, car elle couvre les détails de la création d’apparences simples, puis les apparences plus compliquées qui utilisent des éléments d’apparence particuliers.</span><span class="sxs-lookup"><span data-stu-id="7384f-123">You will probably want to read this section because it covers the details of creating simple skins, and then more complicated skins that use particular skin elements.</span></span> <span data-ttu-id="7384f-124">Cette section comprend également des didacticiels sur la création de l’art nécessaire à la création d’apparences.</span><span class="sxs-lookup"><span data-stu-id="7384f-124">This section also includes tutorials on creating the art needed to create skins.</span></span> |
| [<span data-ttu-id="7384f-125">Référence de programmation de l’apparence</span><span class="sxs-lookup"><span data-stu-id="7384f-125">Skin Programming Reference</span></span>](skin-programming-reference.md)               | <span data-ttu-id="7384f-126">Contient des entrées de référence pour chaque élément et attribut pris en charge par les apparences.</span><span class="sxs-lookup"><span data-stu-id="7384f-126">Contains reference entries for every element and attribute supported by skins.</span></span> <span data-ttu-id="7384f-127">Lisez les rubriques qui expliquent les fonctionnalités que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="7384f-127">Read the topics that explain the functionality that you want to use.</span></span>                                                                                                                                                    |
| [<span data-ttu-id="7384f-128">Apparences mobiles du lecteur Windows Media</span><span class="sxs-lookup"><span data-stu-id="7384f-128">Windows Media Player Mobile Skins</span></span>](windows-media-player-mobile-skins.md) | <span data-ttu-id="7384f-129">Fournit des informations complètes sur la création d’apparences pour Windows Media Player Mobile.</span><span class="sxs-lookup"><span data-stu-id="7384f-129">Provides complete information for creating skins for Windows Media Player Mobile.</span></span>                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="7384f-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7384f-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7384f-131">**SDK du lecteur Windows Media**</span><span class="sxs-lookup"><span data-stu-id="7384f-131">**Windows Media Player SDK**</span></span>](windows-media-player-sdk.md)
</dt> </dl>

 

 




