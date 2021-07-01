---
description: Contient une liste de fournisseurs de suivi pour MFTrace.
ms.assetid: ee483f0a-5a90-4150-ada4-0b63ae312523
title: élément providers
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d38a86bf3ca8ffa1ea9e3da20e0244e7abec8513
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118484"
---
# <a name="providers-element"></a><span data-ttu-id="aba8b-103">élément providers</span><span class="sxs-lookup"><span data-stu-id="aba8b-103">providers element</span></span>

<span data-ttu-id="aba8b-104">Contient une liste de fournisseurs de suivi pour [MFTrace](mftrace.md).</span><span class="sxs-lookup"><span data-stu-id="aba8b-104">Contains a list of trace providers for [MFTrace](mftrace.md).</span></span>

## <a name="usage"></a><span data-ttu-id="aba8b-105">Usage</span><span class="sxs-lookup"><span data-stu-id="aba8b-105">Usage</span></span>

``` syntax
<providers>
  child elements
</providers>
```

## <a name="attributes"></a><span data-ttu-id="aba8b-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="aba8b-106">Attributes</span></span>

<span data-ttu-id="aba8b-107">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="aba8b-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="aba8b-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="aba8b-108">Child elements</span></span>



| <span data-ttu-id="aba8b-109">Élément</span><span class="sxs-lookup"><span data-stu-id="aba8b-109">Element</span></span>                                   | <span data-ttu-id="aba8b-110">Description</span><span class="sxs-lookup"><span data-stu-id="aba8b-110">Description</span></span>                                                                                                      |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aba8b-111">**mfdetours**</span><span class="sxs-lookup"><span data-stu-id="aba8b-111">**mfdetours**</span></span>](mfdetours.md)<br/> | <span data-ttu-id="aba8b-112">Spécifie le fournisseur de détournements de Media Foundation, qui effectue le suivi des appels d’API Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="aba8b-112">Specifies the Media Foundation Detours provider, which traces Media Foundation API calls.</span></span><br/> <br/> |
| [<span data-ttu-id="aba8b-113">**moteur**</span><span class="sxs-lookup"><span data-stu-id="aba8b-113">**provider**</span></span>](provider.md)<br/>   | <span data-ttu-id="aba8b-114">Spécifie un fournisseur de trace (ETW ou WPP).</span><span class="sxs-lookup"><span data-stu-id="aba8b-114">Specifies a trace provider (ETW or WPP).</span></span><br/> <br/>                                                  |



### <a name="child-element-sequence"></a><span data-ttu-id="aba8b-115">Séquence d’éléments enfants</span><span class="sxs-lookup"><span data-stu-id="aba8b-115">Child element sequence</span></span>

``` syntax
(
  mfdetours?, 
  provider*
)
```

## <a name="parent-elements"></a><span data-ttu-id="aba8b-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="aba8b-116">Parent elements</span></span>

<span data-ttu-id="aba8b-117">Il n’y a pas d’éléments parents.</span><span class="sxs-lookup"><span data-stu-id="aba8b-117">There are no parent elements.</span></span>

## <a name="element-information"></a><span data-ttu-id="aba8b-118">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="aba8b-118">Element information</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="aba8b-119">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="aba8b-119">Can be empty</span></span>
    :::column-end:::
    :::column span="2":::
        <span data-ttu-id="aba8b-120">Oui</span><span class="sxs-lookup"><span data-stu-id="aba8b-120">Yes</span></span>
    :::column-end:::
:::row-end:::

## <a name="see-also"></a><span data-ttu-id="aba8b-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aba8b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aba8b-122">Fichier de configuration MFTrace</span><span class="sxs-lookup"><span data-stu-id="aba8b-122">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)
</dt> </dl>

 

 




