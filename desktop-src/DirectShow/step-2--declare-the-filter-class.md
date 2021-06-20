---
description: Déclarez une classe C++ qui hérite de la classe de base que votre a choisie dans le cadre de l’écriture d’un filtre de transformation.
ms.assetid: 74fbfc16-541f-4f80-a72f-26b67dc09a93
title: Étape 2. Déclarer la classe de filtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88be97e47d529ffa22c90e9c8c200160dbd5f261
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112410062"
---
# <a name="step-2-declare-the-filter-class"></a><span data-ttu-id="2e7b5-104">Étape 2.</span><span class="sxs-lookup"><span data-stu-id="2e7b5-104">Step 2.</span></span> <span data-ttu-id="2e7b5-105">Déclarer la classe de filtre</span><span class="sxs-lookup"><span data-stu-id="2e7b5-105">Declare the Filter Class</span></span>

<span data-ttu-id="2e7b5-106">Il s’agit de l’étape 2 du didacticiel [écriture de filtres de transformation](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="2e7b5-106">This is step 2 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="2e7b5-107">Commencez par déclarer une classe C++ qui hérite de la classe de base :</span><span class="sxs-lookup"><span data-stu-id="2e7b5-107">Start by declaring a C++ class that inherits the base class:</span></span>


```C++
class CRleFilter : public CTransformFilter
{
    /* Declarations will go here. */
};
```



<span data-ttu-id="2e7b5-108">Chacune des classes de filtre a des classes pin associées.</span><span class="sxs-lookup"><span data-stu-id="2e7b5-108">Each of the filter classes has associated pin classes.</span></span> <span data-ttu-id="2e7b5-109">En fonction des besoins spécifiques de votre filtre, vous devrez peut-être remplacer les classes pin.</span><span class="sxs-lookup"><span data-stu-id="2e7b5-109">Depending on the specific needs of your filter, you might need to override the pin classes.</span></span> <span data-ttu-id="2e7b5-110">Dans le cas de **CTransformFilter**, les pin délèguent la plus grande partie de leur travail au filtre, ce qui signifie que vous n’avez probablement pas besoin de remplacer les codes confidentiels.</span><span class="sxs-lookup"><span data-stu-id="2e7b5-110">In the case of **CTransformFilter**, the pins delegate most of their work to the filter, so you probably don't need to override the pins.</span></span>

<span data-ttu-id="2e7b5-111">Vous devez générer un CLSID unique pour le filtre.</span><span class="sxs-lookup"><span data-stu-id="2e7b5-111">You must generate a unique CLSID for the filter.</span></span> <span data-ttu-id="2e7b5-112">Vous pouvez utiliser l’utilitaire Guidgen ou uuidgen. ne jamais copier un GUID existant.</span><span class="sxs-lookup"><span data-stu-id="2e7b5-112">You can use the Guidgen or Uuidgen utility; never copy an existing GUID.</span></span> <span data-ttu-id="2e7b5-113">Il existe plusieurs façons de déclarer un CLSID.</span><span class="sxs-lookup"><span data-stu-id="2e7b5-113">There are several ways to declare a CLSID.</span></span> <span data-ttu-id="2e7b5-114">L’exemple suivant utilise la macro **définir le \_ GUID** :</span><span class="sxs-lookup"><span data-stu-id="2e7b5-114">The following example uses the **DEFINE\_GUID** macro:</span></span>


```C++
[RleFilt.h]
// {1915C5C7-02AA-415f-890F-76D94C85AAF1}
DEFINE_GUID(CLSID_RLEFilter, 
0x1915c5c7, 0x2aa, 0x415f, 0x89, 0xf, 0x76, 0xd9, 0x4c, 0x85, 0xaa, 0xf1);

[RleFilt.cpp]
#include <initguid.h>
#include "RleFilt.h"
```



<span data-ttu-id="2e7b5-115">Ensuite, écrivez une méthode de constructeur pour le filtre :</span><span class="sxs-lookup"><span data-stu-id="2e7b5-115">Next, write a constructor method for the filter:</span></span>


```C++
CRleFilter::CRleFilter()
  : CTransformFilter(NAME("My RLE Encoder"), 0, CLSID_RLEFilter)
{ 
   /* Initialize any private variables here. */
}
```



<span data-ttu-id="2e7b5-116">Notez que l’un des paramètres du constructeur [**CTransformFilter**](ctransformfilter-ctransformfilter.md) est le CLSID défini précédemment.</span><span class="sxs-lookup"><span data-stu-id="2e7b5-116">Notice that one of the parameters to the [**CTransformFilter**](ctransformfilter-ctransformfilter.md) constructor is the CLSID defined earlier.</span></span>

<span data-ttu-id="2e7b5-117">Suivant : [étape 3. Prendre en charge la négociation de type de média](step-3--support-media-type-negotiation.md).</span><span class="sxs-lookup"><span data-stu-id="2e7b5-117">Next: [Step 3. Support Media Type Negotiation](step-3--support-media-type-negotiation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2e7b5-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2e7b5-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e7b5-119">Écriture de filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="2e7b5-119">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



