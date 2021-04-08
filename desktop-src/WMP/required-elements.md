---
title: Éléments obligatoires
description: Éléments obligatoires
ms.assetid: 6aabbdcc-f834-4908-b25a-1dfce038132a
keywords:
- Windows Media Player Mobile Skins, éléments
- apparences, éléments
- fichiers de définition d’apparence, éléments
- éléments, fichiers de définition d’apparence
- éléments, Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e1f05ba51b83fad6585d24c3ad19830598b8975
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673450"
---
# <a name="required-elements"></a><span data-ttu-id="10d1d-108">Éléments obligatoires</span><span class="sxs-lookup"><span data-stu-id="10d1d-108">Required Elements</span></span>

<span data-ttu-id="10d1d-109">Vous devez fournir les éléments suivants dans votre fichier de définition d’apparence :</span><span class="sxs-lookup"><span data-stu-id="10d1d-109">You must provide the following elements in your skin definition file:</span></span>

-   <span data-ttu-id="10d1d-110">**Titre.**</span><span class="sxs-lookup"><span data-stu-id="10d1d-110">**Header.**</span></span> <span data-ttu-id="10d1d-111">L’en-tête du fichier de définition d’apparence principal est requis.</span><span class="sxs-lookup"><span data-stu-id="10d1d-111">The main skin definition file header is required.</span></span> <span data-ttu-id="10d1d-112">Pour plus d’informations sur la version de l’en-tête, consultez le tableau dans la section [création d’un fichier de définition d’apparence](creating-a-skin-definition-file.md) .</span><span class="sxs-lookup"><span data-stu-id="10d1d-112">For header version information, see the table in the [Creating a Skin Definition File](creating-a-skin-definition-file.md) section.</span></span>
-   <span data-ttu-id="10d1d-113">**Section Description.**</span><span class="sxs-lookup"><span data-stu-id="10d1d-113">**Description section.**</span></span> <span data-ttu-id="10d1d-114">La section Description est requise lors de la création d’habillages pour Windows Media Player 9 Series pour Windows Mobile.</span><span class="sxs-lookup"><span data-stu-id="10d1d-114">The Description section is required when creating skins for Windows Media Player 9 Series for Windows Mobile.</span></span> <span data-ttu-id="10d1d-115">Il doit s’agir de la première section du fichier de définition d’apparence, et il doit spécifier des valeurs valides pour les dimensions.</span><span class="sxs-lookup"><span data-stu-id="10d1d-115">It must be the first section in the skin definition file, and it must specify valid values for Dimensions.</span></span> <span data-ttu-id="10d1d-116">La spécification d’une valeur pour orientation est facultative.</span><span class="sxs-lookup"><span data-stu-id="10d1d-116">Specifying a value for Orientation is optional.</span></span>
-   <span data-ttu-id="10d1d-117">**Section bitmaps.**</span><span class="sxs-lookup"><span data-stu-id="10d1d-117">**Bitmaps section.**</span></span> <span data-ttu-id="10d1d-118">La section bitmaps est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="10d1d-118">The Bitmaps section is required.</span></span> <span data-ttu-id="10d1d-119">En outre, la section bitmaps doit spécifier des noms valides pour les fichiers d’arrière-plan, désactivés, poussés, régionaux et de Super image.</span><span class="sxs-lookup"><span data-stu-id="10d1d-119">Additionally, the Bitmaps section must specify valid names for Background, Disabled, Pushed, Region, and Super image files.</span></span>
-   <span data-ttu-id="10d1d-120">**fichiers image.**</span><span class="sxs-lookup"><span data-stu-id="10d1d-120">**Image files.**</span></span> <span data-ttu-id="10d1d-121">Vous devez fournir des fichiers d’arrière-plan, désactivés, poussés, régionaux et de Super image dans le cadre de votre apparence.</span><span class="sxs-lookup"><span data-stu-id="10d1d-121">You must provide Background, Disabled, Pushed, Region, and Super image files as part of your skin.</span></span> <span data-ttu-id="10d1d-122">Si vous créez des habillages pour Windows Media Player 10 mobile ou version ultérieure, vous n’avez pas besoin d’inclure des fichiers de région ou de Super image.</span><span class="sxs-lookup"><span data-stu-id="10d1d-122">If you are creating skins for Windows Media Player 10 Mobile or later, you do not need to include Region or Super image files.</span></span>

<span data-ttu-id="10d1d-123">Si vous créez une apparence avec uniquement des images définies, l’apparence est visible, mais n’offre aucune fonctionnalité significative à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="10d1d-123">If you create a skin with only images defined, the skin will be visible, but will not offer any meaningful functionality to the user.</span></span> <span data-ttu-id="10d1d-124">Si vous décidez de créer une apparence sans boutons, par exemple pour empêcher l’utilisateur d’ignorer certains contenus, sachez qu’il est toujours possible de mapper les fonctionnalités sur les boutons matériels de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="10d1d-124">If you decide to create a skin without buttons, perhaps to prevent the user from skipping over certain content, be aware that it may still be possible to map functionality to the hardware buttons on the device.</span></span>

<span data-ttu-id="10d1d-125">Les fichiers Thumb sont requis et votre trackbars ne peut pas être utilisé sans thumbs.</span><span class="sxs-lookup"><span data-stu-id="10d1d-125">Thumb files are required and your trackbars cannot be used without thumbs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="10d1d-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="10d1d-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10d1d-127">**Fichier de définition d’apparence**</span><span class="sxs-lookup"><span data-stu-id="10d1d-127">**Skin Definition File**</span></span>](skin-definition-file-mobile.md)
</dt> </dl>

 

 




