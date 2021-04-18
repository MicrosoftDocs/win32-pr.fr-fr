---
description: Spécifie le fournisseur de détournements de Microsoft Media Foundation, qui effectue le suivi des appels d’API Media Foundation.
ms.assetid: 7c9abda9-7968-463c-b4a9-19b54012ef56
title: élément mfdetours
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c09d39d6f8a7c7ff1d88471e71c6fc58aa49bd62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533768"
---
# <a name="mfdetours-element"></a><span data-ttu-id="2d259-103">élément mfdetours</span><span class="sxs-lookup"><span data-stu-id="2d259-103">mfdetours element</span></span>

<span data-ttu-id="2d259-104">Spécifie le fournisseur de détournements de Microsoft Media Foundation, qui effectue le suivi des appels d’API Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="2d259-104">Specifies the Microsoft Media Foundation Detours provider, which traces Media Foundation API calls.</span></span>

## <a name="usage"></a><span data-ttu-id="2d259-105">Utilisation</span><span class="sxs-lookup"><span data-stu-id="2d259-105">Usage</span></span>

``` syntax
<mfdetours
  level = "CDATA">
  child elements
</mfdetours>
```

## <a name="attributes"></a><span data-ttu-id="2d259-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="2d259-106">Attributes</span></span>



| <span data-ttu-id="2d259-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="2d259-107">Attribute</span></span>            | <span data-ttu-id="2d259-108">Type</span><span class="sxs-lookup"><span data-stu-id="2d259-108">Type</span></span>             | <span data-ttu-id="2d259-109">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="2d259-109">Required</span></span>       | <span data-ttu-id="2d259-110">Description</span><span class="sxs-lookup"><span data-stu-id="2d259-110">Description</span></span>                             |
|----------------------|------------------|----------------|-----------------------------------------|
| <span data-ttu-id="2d259-111">**level**</span><span class="sxs-lookup"><span data-stu-id="2d259-111">**level**</span></span><br/> | <span data-ttu-id="2d259-112">CDATA</span><span class="sxs-lookup"><span data-stu-id="2d259-112">CDATA</span></span><br/> | <span data-ttu-id="2d259-113">Oui</span><span class="sxs-lookup"><span data-stu-id="2d259-113">Yes</span></span><br/> | <span data-ttu-id="2d259-114">Niveau de trace.</span><span class="sxs-lookup"><span data-stu-id="2d259-114">The trace level.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="2d259-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="2d259-115">Child elements</span></span>



| <span data-ttu-id="2d259-116">Élément</span><span class="sxs-lookup"><span data-stu-id="2d259-116">Element</span></span>                               |
|---------------------------------------|
| [<span data-ttu-id="2d259-117">**keyword**</span><span class="sxs-lookup"><span data-stu-id="2d259-117">**keyword**</span></span>](keyword.md)<br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="2d259-118">Séquence d’éléments enfants</span><span class="sxs-lookup"><span data-stu-id="2d259-118">Child element sequence</span></span>

``` syntax
keyword+
```

## <a name="parent-elements"></a><span data-ttu-id="2d259-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="2d259-119">Parent elements</span></span>



| <span data-ttu-id="2d259-120">Élément</span><span class="sxs-lookup"><span data-stu-id="2d259-120">Element</span></span>                                   |
|-------------------------------------------|
| [<span data-ttu-id="2d259-121">**fournisseurs**</span><span class="sxs-lookup"><span data-stu-id="2d259-121">**providers**</span></span>](providers.md)<br/> |



## <a name="element-information"></a><span data-ttu-id="2d259-122">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="2d259-122">Element information</span></span>



|              |     |
|--------------|-----|
| <span data-ttu-id="2d259-123">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="2d259-123">Can be empty</span></span> | <span data-ttu-id="2d259-124">Non</span><span class="sxs-lookup"><span data-stu-id="2d259-124">No</span></span>  |



## <a name="see-also"></a><span data-ttu-id="2d259-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d259-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d259-126">Fichier de configuration MFTrace</span><span class="sxs-lookup"><span data-stu-id="2d259-126">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)
</dt> </dl>

 

 




