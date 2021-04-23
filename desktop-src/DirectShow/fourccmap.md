---
description: La classe FOURCCMap fournit la conversion entre les sous-types de média GUID et les balises multimédias FOURCC 32 bits de style ancien.
ms.assetid: f77f1da9-34f6-44a0-9f1a-7db2e5a26268
title: FOURCCMap, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap
api_type:
- COM
api_location: ''
ms.openlocfilehash: b9254986bebadeffafaa832817f59194bfc58e12
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908857"
---
# <a name="fourccmap-class"></a><span data-ttu-id="3e75a-103">FOURCCMap, classe</span><span class="sxs-lookup"><span data-stu-id="3e75a-103">FOURCCMap class</span></span>

![hiérarchie de la classe fourccmap](images/fourcc01.png)

<span data-ttu-id="3e75a-105">La classe **FOURCCMap** fournit la conversion entre les sous-types de média **GUID** et les balises multimédias **FourCC** 32 bits de style ancien.</span><span class="sxs-lookup"><span data-stu-id="3e75a-105">The **FOURCCMap** class provides conversion between **GUID** media subtypes and old-style **FOURCC** 32-bit media tags.</span></span> <span data-ttu-id="3e75a-106">Dans les API multimédia Windows d’origine, les types de média ont été marqués avec des valeurs 32 bits créées à partir de caractères 4 8 bits et connues sous le nom de « **FourCC** s ».</span><span class="sxs-lookup"><span data-stu-id="3e75a-106">In the original Windows multimedia APIs, media types were tagged with 32-bit values created from four 8-bit characters and were known as **FOURCC** s.</span></span> <span data-ttu-id="3e75a-107">Les types de média DirectShow ont des **GUID** pour le sous-type, en partie parce qu’ils sont plus simples à créer (la création d’un nouveau **FourCC** nécessite son inscription auprès de Microsoft).</span><span class="sxs-lookup"><span data-stu-id="3e75a-107">DirectShow media types have **GUID** s for the subtype, partly because these are simpler to create (creation of a new **FOURCC** requires its registration with Microsoft).</span></span> <span data-ttu-id="3e75a-108">Étant donné que les valeurs **FourCC** sont uniques, un mappage un-à-un est rendu possible en allouant une plage de 4 milliards **GUID** représentant des **FourCC** s.</span><span class="sxs-lookup"><span data-stu-id="3e75a-108">Because **FOURCC** s are unique, a one-to-one mapping has been made possible by allocating a range of 4,000 million **GUID** s representing **FOURCC** s.</span></span> <span data-ttu-id="3e75a-109">Cette plage correspond à tous les **GUID** sous la forme :</span><span class="sxs-lookup"><span data-stu-id="3e75a-109">This range is all **GUID** s of the form:</span></span>

`XXXXXXXX-0000-0010-8000-00AA00389B71`

<span data-ttu-id="3e75a-110">Cette classe simplifie la conversion entre les **GUID** s et **FourCC**.</span><span class="sxs-lookup"><span data-stu-id="3e75a-110">This class simplifies conversion between **GUID** s and **FOURCC** s.</span></span> <span data-ttu-id="3e75a-111">Il s’agit d’une compatibilité uniquement.</span><span class="sxs-lookup"><span data-stu-id="3e75a-111">This is for compatibility only.</span></span> <span data-ttu-id="3e75a-112">Il est recommandé que tous les nouveaux sous-types de médias soient représentés par les **GUID** créés par Guidgen.exe ou un outil similaire, et non par le mappage de **FourCC** s.</span><span class="sxs-lookup"><span data-stu-id="3e75a-112">It is recommended that all new media subtypes be represented by **GUID** s created by Guidgen.exe or a similar tool, and not by mapping **FOURCC** s.</span></span>

<span data-ttu-id="3e75a-113">L’objet est dérivé d’un **GUID**, sans données membres supplémentaires, et peut faire l’objet d’un cast en **GUID**.</span><span class="sxs-lookup"><span data-stu-id="3e75a-113">The object is derived from a **GUID**, with no extra data members, and can be cast to a **GUID**.</span></span> <span data-ttu-id="3e75a-114">Un **FourCC** peut être passé à l’objet au moment de la construction.</span><span class="sxs-lookup"><span data-stu-id="3e75a-114">The object can be passed a **FOURCC** at construction time.</span></span> <span data-ttu-id="3e75a-115">Le constructeur par défaut initialise le **FourCC** à zéro.</span><span class="sxs-lookup"><span data-stu-id="3e75a-115">The default constructor will initialize the **FOURCC** to zero.</span></span>

<span data-ttu-id="3e75a-116">Les méthodes [**GetFOURCC**](fourccmap-getfourcc.md) et [**SetFOURCC**](fourccmap-setfourcc.md) ne vérifient pas que les parties fixes du **GUID** correspondent à la plage **FourCC** .</span><span class="sxs-lookup"><span data-stu-id="3e75a-116">The [**GetFOURCC**](fourccmap-getfourcc.md) and [**SetFOURCC**](fourccmap-setfourcc.md) methods do not check that the fixed portions of the **GUID** correspond to the **FOURCC** range.</span></span> <span data-ttu-id="3e75a-117">Ainsi, si vous effectuez un cast d’un pointeur vers un **GUID** en un pointeur vers un **FourCC** , puis que vous définissez ou récupérez le champ **FourCC** , vous devez également vérifier séparément que le **GUID** se trouve dans la plage **FourCC** .</span><span class="sxs-lookup"><span data-stu-id="3e75a-117">Thus, if you cast a pointer to a **GUID** into a pointer to a **FOURCC** and then set or get the **FOURCC** field, you also need to check separately that the **GUID** is within the **FOURCC** range.</span></span>

## <a name="member-functions"></a><span data-ttu-id="3e75a-118">Fonctions de membre</span><span class="sxs-lookup"><span data-stu-id="3e75a-118">Member Functions</span></span>



| <span data-ttu-id="3e75a-119">Étiquette</span><span class="sxs-lookup"><span data-stu-id="3e75a-119">Label</span></span> | <span data-ttu-id="3e75a-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e75a-120">Value</span></span> |
|------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="3e75a-121">**FOURCCMap**</span><span class="sxs-lookup"><span data-stu-id="3e75a-121">**FOURCCMap**</span></span>](fourccmap-fourccmap.md) | <span data-ttu-id="3e75a-122">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="3e75a-122">Constructor method.</span></span>                                      |
| [<span data-ttu-id="3e75a-123">**GetFOURCC**</span><span class="sxs-lookup"><span data-stu-id="3e75a-123">**GetFOURCC**</span></span>](fourccmap-getfourcc.md) | <span data-ttu-id="3e75a-124">Récupère le **FourCC** à partir d’un objet **FOURCCMap** .</span><span class="sxs-lookup"><span data-stu-id="3e75a-124">Retrieves the **FOURCC** from a **FOURCCMap** object.</span></span>    |
| [<span data-ttu-id="3e75a-125">**SetFOURCC**</span><span class="sxs-lookup"><span data-stu-id="3e75a-125">**SetFOURCC**</span></span>](fourccmap-setfourcc.md) | <span data-ttu-id="3e75a-126">Définit la partie **FourCC** de l’objet **FOURCCMap** .</span><span class="sxs-lookup"><span data-stu-id="3e75a-126">Sets the **FOURCC** portion of the **FOURCCMap** object.</span></span> |



 

 

 



