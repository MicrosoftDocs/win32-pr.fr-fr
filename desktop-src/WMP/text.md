---
title: Texte (kit de développement logiciel (SDK) Windows Media Player)
description: Texte
ms.assetid: 8c10cefb-d0d0-4214-8712-d171a76de95d
keywords:
- Windows Media Player Mobile Skins, Text
- apparences, texte
- informations de référence sur les apparences, le texte
- texte dans les enveloppes, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c801d93698bc7a17eea34df71514dd88b485f0d9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103843013"
---
# <a name="text-windows-media-player-sdk"></a><span data-ttu-id="28327-107">Texte (kit de développement logiciel (SDK) Windows Media Player)</span><span class="sxs-lookup"><span data-stu-id="28327-107">Text (Windows Media Player SDK)</span></span>

<span data-ttu-id="28327-108">Vous souhaiterez peut-être utiliser une ou plusieurs zones d’affichage de texte dans votre apparence.</span><span class="sxs-lookup"><span data-stu-id="28327-108">You may want to use one or more text display boxes in your skin.</span></span> <span data-ttu-id="28327-109">Chaque zone d’affichage de texte que vous utilisez doit être définie dans le fichier de définition d’apparence.</span><span class="sxs-lookup"><span data-stu-id="28327-109">Each text display box you use must be defined in the skin definition file.</span></span> <span data-ttu-id="28327-110">Si vous ne définissez pas de zone d’affichage de texte dans cette section, votre apparence ne sera pas en mesure de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="28327-110">If you do not define a text display box in this section, your skin will not be able to use it.</span></span>

<span data-ttu-id="28327-111">La section de texte du fichier de définition d’apparence commence par cette ligne :</span><span class="sxs-lookup"><span data-stu-id="28327-111">The Text section of the skin definition file begins with this line:</span></span>


```C++
[ Text ]

```



<span data-ttu-id="28327-112">Vous devez ensuite ajouter une ou plusieurs lignes qui contiennent des informations sur chacune des zones d’affichage de texte dans votre apparence.</span><span class="sxs-lookup"><span data-stu-id="28327-112">You then must add one or more lines that contain information about each of the text display boxes in your skin</span></span>


```C++
    Time         180,46,50,30   Right    Tahoma,16,N     255,255,255

```



<span data-ttu-id="28327-113">Vous pouvez utiliser le modèle suivant pour la section de texte de votre fichier de définition d’apparence :</span><span class="sxs-lookup"><span data-stu-id="28327-113">You can use the following template for the Text section of your skin definition file:</span></span>


```C++
//  <Type>       <Location>     <Align> <Font>          <Color>
//  ------       ----------     ------- ------          -------

```



<span data-ttu-id="28327-114">Vous devez utiliser l’ordre indiqué dans le modèle précédent pour obtenir des informations sur la zone d’affichage de texte pour chaque ligne de la section de texte.</span><span class="sxs-lookup"><span data-stu-id="28327-114">You must use the order shown in the preceding template for text display box information for each line in the Text section.</span></span> <span data-ttu-id="28327-115">Chaque partie de la ligne est requise.</span><span class="sxs-lookup"><span data-stu-id="28327-115">Each part of the line is required.</span></span> <span data-ttu-id="28327-116">Les sections suivantes décrivent chaque élément en détail.</span><span class="sxs-lookup"><span data-stu-id="28327-116">The following sections describe each item in detail.</span></span>

1.  [<span data-ttu-id="28327-117">Type de texte</span><span class="sxs-lookup"><span data-stu-id="28327-117">Text Type</span></span>](text-type.md)
2.  [<span data-ttu-id="28327-118">Emplacement du texte</span><span class="sxs-lookup"><span data-stu-id="28327-118">Text Location</span></span>](text-location.md)
3.  [<span data-ttu-id="28327-119">Alignement du texte</span><span class="sxs-lookup"><span data-stu-id="28327-119">Text Alignment</span></span>](text-alignment.md)
4.  [<span data-ttu-id="28327-120">Police du texte</span><span class="sxs-lookup"><span data-stu-id="28327-120">Text Font</span></span>](text-font.md)
5.  [<span data-ttu-id="28327-121">Couleur du texte</span><span class="sxs-lookup"><span data-stu-id="28327-121">Text Color</span></span>](text-color.md)

<span data-ttu-id="28327-122">Pour obtenir un exemple de code de texte, consultez la [section exemple de texte](sample-text-section.md).</span><span class="sxs-lookup"><span data-stu-id="28327-122">For an example of Text code, see [Sample Text Section](sample-text-section.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="28327-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="28327-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28327-124">**Référence d’apparence**</span><span class="sxs-lookup"><span data-stu-id="28327-124">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




