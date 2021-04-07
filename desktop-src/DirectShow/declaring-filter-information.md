---
description: Déclaration d’informations de filtre
ms.assetid: ed3c1d44-ccef-4dde-819b-f5d4d3be6d1e
title: Déclaration d’informations de filtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8975217f1b7746b26dc5dd16ce9f4e7f694f44bc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747412"
---
# <a name="declaring-filter-information"></a><span data-ttu-id="f70f2-103">Déclaration d’informations de filtre</span><span class="sxs-lookup"><span data-stu-id="f70f2-103">Declaring Filter Information</span></span>

<span data-ttu-id="f70f2-104">La première étape consiste à déclarer les informations de filtre, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="f70f2-104">The first step is to declare the filter information, if needed.</span></span> <span data-ttu-id="f70f2-105">DirectShow définit les structures suivantes pour décrire les filtres, les codes confidentiels et les types de média :</span><span class="sxs-lookup"><span data-stu-id="f70f2-105">DirectShow defines the following structures for describing filters, pins, and media types:</span></span>



| <span data-ttu-id="f70f2-106">Structure</span><span class="sxs-lookup"><span data-stu-id="f70f2-106">Structure</span></span>                                               | <span data-ttu-id="f70f2-107">Description</span><span class="sxs-lookup"><span data-stu-id="f70f2-107">Description</span></span>             |
|---------------------------------------------------------|-------------------------|
| [<span data-ttu-id="f70f2-108">**\_filtre AMOVIESETUP**</span><span class="sxs-lookup"><span data-stu-id="f70f2-108">**AMOVIESETUP\_FILTER**</span></span>](amoviesetup-filter.md)       | <span data-ttu-id="f70f2-109">Décrit un filtre.</span><span class="sxs-lookup"><span data-stu-id="f70f2-109">Describes a filter.</span></span>     |
| [<span data-ttu-id="f70f2-110">**\_code PIN AMOVIESETUP**</span><span class="sxs-lookup"><span data-stu-id="f70f2-110">**AMOVIESETUP\_PIN**</span></span>](amoviesetup-pin.md)             | <span data-ttu-id="f70f2-111">Décrit un code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="f70f2-111">Describes a pin.</span></span>        |
| [<span data-ttu-id="f70f2-112">**\_MediaType AMOVIESETUP**</span><span class="sxs-lookup"><span data-stu-id="f70f2-112">**AMOVIESETUP\_MEDIATYPE**</span></span>](amoviesetup-mediatype.md) | <span data-ttu-id="f70f2-113">Décrit un type de média.</span><span class="sxs-lookup"><span data-stu-id="f70f2-113">Describes a media type.</span></span> |



 

<span data-ttu-id="f70f2-114">Ces structures sont imbriquées.</span><span class="sxs-lookup"><span data-stu-id="f70f2-114">These structures are nested.</span></span> <span data-ttu-id="f70f2-115">La structure de **\_ filtre AMOVEIESETUP** a un pointeur vers un tableau de structures de **\_ code confidentiel AMOVIESETUP** , et chacune d’entre elles a un pointeur vers un tableau de structures de **\_ MediaType AMOVEIESETUP** .</span><span class="sxs-lookup"><span data-stu-id="f70f2-115">The **AMOVEIESETUP\_FILTER** structure has a pointer to an array of **AMOVIESETUP\_PIN** structures, and each of these has a pointer to an array of **AMOVEIESETUP\_MEDIATYPE** structures.</span></span> <span data-ttu-id="f70f2-116">Pris ensemble, ces structures fournissent suffisamment d’informations pour que l’interface [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) localise un filtre.</span><span class="sxs-lookup"><span data-stu-id="f70f2-116">Taken together, these structures provide enough information for the [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface to locate a filter.</span></span> <span data-ttu-id="f70f2-117">Il ne s’agit pas d’une description complète d’un filtre.</span><span class="sxs-lookup"><span data-stu-id="f70f2-117">They are not a complete description of a filter.</span></span> <span data-ttu-id="f70f2-118">Par exemple, si le filtre crée plusieurs instances du même code confidentiel, vous devez déclarer une seule structure [**AMOVIESETUP \_ pin**](amoviesetup-pin.md) pour ce code PIN.</span><span class="sxs-lookup"><span data-stu-id="f70f2-118">For example, if the filter creates multiple instances of the same pin, you should declare only one [**AMOVIESETUP\_PIN**](amoviesetup-pin.md) structure for that pin.</span></span> <span data-ttu-id="f70f2-119">En outre, un filtre n’est pas requis pour prendre en charge toutes les combinaisons de types de médias qu’il enregistre. vous n’avez pas non plus besoin d’inscrire chaque type de média qu’il prend en charge.</span><span class="sxs-lookup"><span data-stu-id="f70f2-119">Also, a filter is not required to support every combination of media types that it registers; nor is required to register every media type that it supports.</span></span>

<span data-ttu-id="f70f2-120">Déclarez les structures de configuration en tant que variables globales dans votre DLL.</span><span class="sxs-lookup"><span data-stu-id="f70f2-120">Declare the set-up structures as global variables within your DLL.</span></span> <span data-ttu-id="f70f2-121">L’exemple suivant montre un filtre avec une broche de sortie :</span><span class="sxs-lookup"><span data-stu-id="f70f2-121">The following example shows a filter with one output pin:</span></span>


```C++
static const WCHAR g_wszName[] = L"Some Filter";

AMOVIESETUP_MEDIATYPE sudMediaTypes[] = {
    { &MEDIATYPE_Video, &MEDIASUBTYPE_RGB24 },
    { &MEDIATYPE_Video, &MEDIASUBTYPE_RGB32 },
};

AMOVIESETUP_PIN sudOutputPin = {
    L"",            // Obsolete, not used.
    FALSE,          // Is this pin rendered?
    TRUE,           // Is it an output pin?
    FALSE,          // Can the filter create zero instances?
    FALSE,          // Does the filter create multiple instances?
    &GUID_NULL,     // Obsolete.
    NULL,           // Obsolete.
    2,              // Number of media types.
    sudMediaTypes   // Pointer to media types.
};

AMOVIESETUP_FILTER sudFilterReg = {
    &CLSID_SomeFilter,      // Filter CLSID.
    g_wszName,              // Filter name.
    MERIT_NORMAL,           // Merit.
    1,                      // Number of pin types.
    &sudOutputPin           // Pointer to pin information.
};
```



<span data-ttu-id="f70f2-122">Le nom du filtre est déclaré en tant que variable globale statique, car il sera réutilisé ailleurs.</span><span class="sxs-lookup"><span data-stu-id="f70f2-122">The filter name is declared as a static global variable, because it will be used again elsewhere.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f70f2-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f70f2-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f70f2-124">Comment inscrire des filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="f70f2-124">How to Register DirectShow Filters</span></span>](how-to-register-directshow-filters.md)
</dt> </dl>

 

 



