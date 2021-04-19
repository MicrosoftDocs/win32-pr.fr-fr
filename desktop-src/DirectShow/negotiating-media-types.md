---
description: Négociation des types de médias
ms.assetid: 9872128c-4e3d-4ac8-afc4-b3dc516a0925
title: Négociation des types de médias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bdcb78cfef6b8396d866ea148267c5a899cd353
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106542100"
---
# <a name="negotiating-media-types"></a><span data-ttu-id="5a28b-103">Négociation des types de médias</span><span class="sxs-lookup"><span data-stu-id="5a28b-103">Negotiating Media Types</span></span>

<span data-ttu-id="5a28b-104">Quand le gestionnaire de graphique de filtre appelle la méthode [**IPIN :: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) , il dispose de plusieurs options pour spécifier un type de média :</span><span class="sxs-lookup"><span data-stu-id="5a28b-104">When the Filter Graph Manager calls the [**IPin::Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) method, it has several options for specifying a media type:</span></span>

-   <span data-ttu-id="5a28b-105">**Type complet :** Si le type de média est entièrement spécifié, les broches essaient de se connecter avec ce type.</span><span class="sxs-lookup"><span data-stu-id="5a28b-105">**Complete type:** If the media type is fully specified, the pins attempt to connect with that type.</span></span> <span data-ttu-id="5a28b-106">Si ce n’est pas le cas, la tentative de connexion échoue.</span><span class="sxs-lookup"><span data-stu-id="5a28b-106">If they cannot, the connection attempt fails.</span></span>
-   <span data-ttu-id="5a28b-107">**Type de média partiel :** Un type de média est *partiel* si le type principal, le sous-type ou le type de format est le GUID \_ null.</span><span class="sxs-lookup"><span data-stu-id="5a28b-107">**Partial media type:** A media type is *partial* if the major type, subtype, or format type is GUID\_NULL.</span></span> <span data-ttu-id="5a28b-108">La valeur du GUID \_ null agit comme un « caractère générique », indiquant que toute valeur est acceptable.</span><span class="sxs-lookup"><span data-stu-id="5a28b-108">The value GUID\_NULL acts as a "wildcard," indicating that any value is acceptable.</span></span> <span data-ttu-id="5a28b-109">Les codes confidentiels négocient un type qui est cohérent avec le type partiel.</span><span class="sxs-lookup"><span data-stu-id="5a28b-109">The pins negotiate a type that is consistent with the partial type.</span></span>
-   <span data-ttu-id="5a28b-110">**Aucun type de média :** Si le gestionnaire de graphique de filtre passe un pointeur **null** , les broches peuvent accepter tout type de média acceptable pour les deux codes PIN.</span><span class="sxs-lookup"><span data-stu-id="5a28b-110">**No media type:** If the Filter Graph Manager passes a **NULL** pointer, the pins can agree to any media type that is acceptable to both pins.</span></span>

<span data-ttu-id="5a28b-111">Si les broches se connectent, la connexion a toujours un type de support complet.</span><span class="sxs-lookup"><span data-stu-id="5a28b-111">If the pins do connect, the connection always has a complete media type.</span></span> <span data-ttu-id="5a28b-112">L’objectif du type de média donné par le gestionnaire de graphe de filtre est de limiter les types de connexions possibles.</span><span class="sxs-lookup"><span data-stu-id="5a28b-112">The purpose of the media type given by the Filter Graph Manager is to limit the possible connection types.</span></span>

<span data-ttu-id="5a28b-113">Pendant le processus de négociation, la broche de sortie propose un type de média en appelant la méthode [**IPIN :: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) du code confidentiel d’entrée.</span><span class="sxs-lookup"><span data-stu-id="5a28b-113">During the negotiation process, the output pin proposes a media type by calling the input pin's [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) method.</span></span> <span data-ttu-id="5a28b-114">La broche d’entrée peut accepter ou rejeter le type proposé.</span><span class="sxs-lookup"><span data-stu-id="5a28b-114">The input pin can accept or reject the proposed type.</span></span> <span data-ttu-id="5a28b-115">Ce processus se répète jusqu’à ce que la broche d’entrée accepte un type ou que la broche de sortie manque de types et que la connexion échoue.</span><span class="sxs-lookup"><span data-stu-id="5a28b-115">This process repeats until either the input pin accepts a type, or the output pin runs out of types and the connection fails.</span></span>

<span data-ttu-id="5a28b-116">La manière dont une broche de sortie sélectionne les types de média à proposer dépend de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="5a28b-116">How an output pin selects media types to propose depends on the implementation.</span></span> <span data-ttu-id="5a28b-117">Dans les classes de base DirectShow, la broche de sortie appelle [**IPIN :: EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) sur la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="5a28b-117">In the DirectShow base classes, the output pin calls [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) on the input pin.</span></span> <span data-ttu-id="5a28b-118">Cette méthode retourne un énumérateur qui énumère les types de média préférés du code confidentiel d’entrée.</span><span class="sxs-lookup"><span data-stu-id="5a28b-118">This method returns an enumerator that enumerates the input pin's preferred media types.</span></span> <span data-ttu-id="5a28b-119">À défaut, la broche de sortie énumère ses propres types préférés.</span><span class="sxs-lookup"><span data-stu-id="5a28b-119">Failing that, the output pin enumerates its own preferred types.</span></span>

<span data-ttu-id="5a28b-120">**Utilisation des types de médias**</span><span class="sxs-lookup"><span data-stu-id="5a28b-120">**Working with Media Types**</span></span>

<span data-ttu-id="5a28b-121">Dans toute fonction qui reçoit un paramètre de **\_ \_ type de média am** , validez toujours les valeurs de **cbFormat** et de **formatType** avant de déréférencer le membre **pbFormat** .</span><span class="sxs-lookup"><span data-stu-id="5a28b-121">In any function that receives an **AM\_MEDIA\_TYPE** parameter, always validate the values of **cbFormat** and **formattype** before dereferencing the **pbFormat** member.</span></span> <span data-ttu-id="5a28b-122">Le code suivant est incorrect :</span><span class="sxs-lookup"><span data-stu-id="5a28b-122">The following code is incorrect:</span></span>


```C++
if (pmt->formattype == FORMAT_VideoInfo)
{
    VIDEOINFOHEADER *pVIH = (VIDEOINFOHEADER*)pmt->pbFormat;
    // Wrong!
}
```



<span data-ttu-id="5a28b-123">Le code suivant est correct :</span><span class="sxs-lookup"><span data-stu-id="5a28b-123">The following code is correct:</span></span>


```C++
if ((pmt->formattype == FORMAT_VideoInfo) && 
    (pmt->cbFormat > sizeof(VIDEOINFOHEADER) &&
    (pbFormat != NULL))
{
    VIDEOINFOHEADER *pVIH = (VIDEOINFOHEADER*)pmt->pbFormat;
    // Now you can dereference pVIH.
}
```



 

 



