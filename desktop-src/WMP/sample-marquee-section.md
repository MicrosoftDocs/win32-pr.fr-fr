---
title: Exemple de section de texte défilant
description: Exemple de section de texte défilant
ms.assetid: 44ed3257-2e1a-4b8d-9d55-a13b0400422d
keywords:
- Windows Media Player Mobile Skins, palissades
- apparences, rectangles de sélection
- informations de référence sur les habillages, les cadres
- textes défilant dans les enveloppes, section de texte défilant
- fichiers de définition d’apparence, section de texte défilant
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f66588d81b22051a9289a80c8733d5cfe154bed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462387"
---
# <a name="sample-marquee-section"></a><span data-ttu-id="3a2f6-108">Exemple de section de texte défilant</span><span class="sxs-lookup"><span data-stu-id="3a2f6-108">Sample Marquee Section</span></span>

<span data-ttu-id="3a2f6-109">Les lignes suivantes affichent une section de texte défilant standard d’un fichier de définition d’apparence :</span><span class="sxs-lookup"><span data-stu-id="3a2f6-109">The following lines show a typical Marquee section of a skin definition file:</span></span>


```C++
//  <Location>   <Font>       <Color>      <Text item combinations>

//  ----------   ------       -------      ------------------------

    3,2,234,20   Tahoma,12,N  255,0,0    Title+Author, Title, Author


```



<span data-ttu-id="3a2f6-110">Cela définit une zone d’affichage de texte défilant qui affiche le titre et l’auteur si les deux sont définis, le titre si seul le titre est défini, ou le nom de l’auteur si seul l’auteur est défini.</span><span class="sxs-lookup"><span data-stu-id="3a2f6-110">This defines a marquee display box that shows the title and author if both are defined, the title if only Title is defined, or the name of the author if only Author is defined.</span></span> <span data-ttu-id="3a2f6-111">Si aucun n’est défini, rien ne s’affiche.</span><span class="sxs-lookup"><span data-stu-id="3a2f6-111">If neither is defined, nothing will be displayed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a2f6-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3a2f6-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a2f6-113">**Chapiteau**</span><span class="sxs-lookup"><span data-stu-id="3a2f6-113">**Marquee**</span></span>](marquee.md)
</dt> </dl>

 

 




