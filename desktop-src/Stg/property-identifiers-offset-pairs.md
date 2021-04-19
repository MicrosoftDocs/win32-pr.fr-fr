---
title: Identificateurs de propriété/paires d’offsets
description: La valeur définie pour la propriété nombre de propriétés est un tableau d’identificateurs de propriété/valeurs de jeu de propriétés de paires d’offsets.
ms.assetid: 341608a1-3ab1-4fa9-ab9a-4124c63c78a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b55ed20aef2c76dc97fcb3f4acfe981b9800308
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106533547"
---
# <a name="property-identifiersoffset-pairs"></a><span data-ttu-id="750e2-103">Identificateurs de propriété/paires d’offsets</span><span class="sxs-lookup"><span data-stu-id="750e2-103">Property Identifiers/Offset Pairs</span></span>

<span data-ttu-id="750e2-104">La valeur définie pour la propriété nombre de propriétés est un tableau d’identificateurs de propriété/valeurs de jeu de propriétés de paires d’offsets.</span><span class="sxs-lookup"><span data-stu-id="750e2-104">Following the Count of Properties property set value is an array of Property Identifiers/Offset Pairs property set values.</span></span> <span data-ttu-id="750e2-105">Les identificateurs de propriété sont des valeurs 32 bits qui identifient de façon unique une propriété dans une section.</span><span class="sxs-lookup"><span data-stu-id="750e2-105">Property Identifiers are 32-bit values that uniquely identify a property within a section.</span></span> <span data-ttu-id="750e2-106">Les paires décalage indiquent la distance entre le début de la section et le début de la paire type/valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="750e2-106">The Offset Pairs indicate the distance from the start of the section to the start of the property Type/Value Pair.</span></span> <span data-ttu-id="750e2-107">Étant donné que les décalages sont relatifs à la section, les sections peuvent être copiées sous la forme d’un tableau d’octets.</span><span class="sxs-lookup"><span data-stu-id="750e2-107">Because the offsets are relative to the section, sections can be copied as an array of bytes.</span></span>

<span data-ttu-id="750e2-108">Les identificateurs de propriété ne sont pas triés dans un ordre particulier.</span><span class="sxs-lookup"><span data-stu-id="750e2-108">Property identifiers are not sorted in any particular order.</span></span> <span data-ttu-id="750e2-109">Les propriétés peuvent être omises dans le jeu de propriétés stocké. les lecteurs ne doivent pas compter sur un ordre ou une plage spécifique d’identificateurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="750e2-109">Properties can be omitted from the stored property set; readers must not rely on a specific order or range of property identifiers.</span></span>

 

 




