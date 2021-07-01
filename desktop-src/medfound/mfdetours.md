---
description: Spécifie le fournisseur de détournements de Microsoft Media Foundation, qui effectue le suivi des appels d’API Media Foundation.
ms.assetid: 7c9abda9-7968-463c-b4a9-19b54012ef56
title: élément mfdetours
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cd03711c74c21a9a6ff33d2cc2560e4b6d6e0a3
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119334"
---
# <a name="mfdetours-element"></a><span data-ttu-id="a53fd-103">élément mfdetours</span><span class="sxs-lookup"><span data-stu-id="a53fd-103">mfdetours element</span></span>

<span data-ttu-id="a53fd-104">Spécifie le fournisseur de détournements de Microsoft Media Foundation, qui effectue le suivi des appels d’API Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="a53fd-104">Specifies the Microsoft Media Foundation Detours provider, which traces Media Foundation API calls.</span></span>

## <a name="usage"></a><span data-ttu-id="a53fd-105">Usage</span><span class="sxs-lookup"><span data-stu-id="a53fd-105">Usage</span></span>

``` syntax
<mfdetours
  level = "CDATA">
  child elements
</mfdetours>
```

## <a name="attributes"></a><span data-ttu-id="a53fd-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="a53fd-106">Attributes</span></span>



| <span data-ttu-id="a53fd-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="a53fd-107">Attribute</span></span>            | <span data-ttu-id="a53fd-108">Type</span><span class="sxs-lookup"><span data-stu-id="a53fd-108">Type</span></span>             | <span data-ttu-id="a53fd-109">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a53fd-109">Required</span></span>       | <span data-ttu-id="a53fd-110">Description</span><span class="sxs-lookup"><span data-stu-id="a53fd-110">Description</span></span>                             |
|----------------------|------------------|----------------|-----------------------------------------|
| <span data-ttu-id="a53fd-111">**level**</span><span class="sxs-lookup"><span data-stu-id="a53fd-111">**level**</span></span><br/> | <span data-ttu-id="a53fd-112">CDATA</span><span class="sxs-lookup"><span data-stu-id="a53fd-112">CDATA</span></span><br/> | <span data-ttu-id="a53fd-113">Oui</span><span class="sxs-lookup"><span data-stu-id="a53fd-113">Yes</span></span><br/> | <span data-ttu-id="a53fd-114">Niveau de trace.</span><span class="sxs-lookup"><span data-stu-id="a53fd-114">The trace level.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="a53fd-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a53fd-115">Child elements</span></span>



| <span data-ttu-id="a53fd-116">Élément</span><span class="sxs-lookup"><span data-stu-id="a53fd-116">Element</span></span>                               |
|---------------------------------------|
| [<span data-ttu-id="a53fd-117">**mot**</span><span class="sxs-lookup"><span data-stu-id="a53fd-117">**keyword**</span></span>](keyword.md)<br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="a53fd-118">Séquence d’éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a53fd-118">Child element sequence</span></span>

``` syntax
keyword+
```

## <a name="parent-elements"></a><span data-ttu-id="a53fd-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="a53fd-119">Parent elements</span></span>

| <span data-ttu-id="a53fd-120">Élément</span><span class="sxs-lookup"><span data-stu-id="a53fd-120">Element</span></span>                                   |
|-------------------------------------------|
| [<span data-ttu-id="a53fd-121">**éditeurs**</span><span class="sxs-lookup"><span data-stu-id="a53fd-121">**providers**</span></span>](providers.md)<br/> |



## <a name="element-information"></a><span data-ttu-id="a53fd-122">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="a53fd-122">Element information</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="a53fd-123">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="a53fd-123">Can be empty</span></span>
    :::column-end:::
    :::column span="2":::
        <span data-ttu-id="a53fd-124">Non</span><span class="sxs-lookup"><span data-stu-id="a53fd-124">No</span></span>
    :::column-end:::
:::row-end:::

## <a name="see-also"></a><span data-ttu-id="a53fd-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a53fd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a53fd-126">Fichier de configuration MFTrace</span><span class="sxs-lookup"><span data-stu-id="a53fd-126">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)
</dt> </dl>

 

 




