---
description: Spécifie un fournisseur de trace (ETW ou WPP) pour MFTrace.
ms.assetid: 692cce3b-ebf5-4a49-8c37-48c8ef6caee7
title: provider (élément)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d96b3015dddbcff74c09f77a1b6245d052fe034
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118444"
---
# <a name="provider-element"></a><span data-ttu-id="c6508-103">provider (élément)</span><span class="sxs-lookup"><span data-stu-id="c6508-103">provider element</span></span>

<span data-ttu-id="c6508-104">Spécifie un fournisseur de trace (ETW ou WPP) pour [MFTrace](mftrace.md).</span><span class="sxs-lookup"><span data-stu-id="c6508-104">Specifies a trace provider (ETW or WPP) for [MFTrace](mftrace.md).</span></span>

## <a name="usage"></a><span data-ttu-id="c6508-105">Usage</span><span class="sxs-lookup"><span data-stu-id="c6508-105">Usage</span></span>

``` syntax
<provider
  ID = "CDATA"
  level = "CDATA">
  child elements
</provider>
```

## <a name="attributes"></a><span data-ttu-id="c6508-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="c6508-106">Attributes</span></span>



| <span data-ttu-id="c6508-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="c6508-107">Attribute</span></span>            | <span data-ttu-id="c6508-108">Type</span><span class="sxs-lookup"><span data-stu-id="c6508-108">Type</span></span>             | <span data-ttu-id="c6508-109">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c6508-109">Required</span></span>       | <span data-ttu-id="c6508-110">Description</span><span class="sxs-lookup"><span data-stu-id="c6508-110">Description</span></span>                                              |
|----------------------|------------------|----------------|----------------------------------------------------------|
| <span data-ttu-id="c6508-111">**Identifiant**</span><span class="sxs-lookup"><span data-stu-id="c6508-111">**ID**</span></span><br/>    | <span data-ttu-id="c6508-112">CDATA</span><span class="sxs-lookup"><span data-stu-id="c6508-112">CDATA</span></span><br/> | <span data-ttu-id="c6508-113">Oui</span><span class="sxs-lookup"><span data-stu-id="c6508-113">Yes</span></span><br/> | <span data-ttu-id="c6508-114">Nom ou GUID du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="c6508-114">The name or GUID of the provider.</span></span><br/> <br/> |
| <span data-ttu-id="c6508-115">**level**</span><span class="sxs-lookup"><span data-stu-id="c6508-115">**level**</span></span><br/> | <span data-ttu-id="c6508-116">CDATA</span><span class="sxs-lookup"><span data-stu-id="c6508-116">CDATA</span></span><br/> | <span data-ttu-id="c6508-117">Oui</span><span class="sxs-lookup"><span data-stu-id="c6508-117">Yes</span></span><br/> | <span data-ttu-id="c6508-118">Niveau de trace.</span><span class="sxs-lookup"><span data-stu-id="c6508-118">The trace level.</span></span><br/> <br/>                  |



## <a name="child-elements"></a><span data-ttu-id="c6508-119">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c6508-119">Child elements</span></span>



| <span data-ttu-id="c6508-120">Élément</span><span class="sxs-lookup"><span data-stu-id="c6508-120">Element</span></span>                               |
|---------------------------------------|
| [<span data-ttu-id="c6508-121">**mot**</span><span class="sxs-lookup"><span data-stu-id="c6508-121">**keyword**</span></span>](keyword.md)<br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="c6508-122">Séquence d’éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c6508-122">Child element sequence</span></span>

``` syntax
keyword+
```

## <a name="parent-elements"></a><span data-ttu-id="c6508-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="c6508-123">Parent elements</span></span>



| <span data-ttu-id="c6508-124">Élément</span><span class="sxs-lookup"><span data-stu-id="c6508-124">Element</span></span>                                   |
|-------------------------------------------|
| [<span data-ttu-id="c6508-125">**éditeurs**</span><span class="sxs-lookup"><span data-stu-id="c6508-125">**providers**</span></span>](providers.md)<br/> |



## <a name="element-information"></a><span data-ttu-id="c6508-126">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="c6508-126">Element information</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="c6508-127">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="c6508-127">Can be empty</span></span>
    :::column-end:::
    :::column span="2":::
        <span data-ttu-id="c6508-128">Non</span><span class="sxs-lookup"><span data-stu-id="c6508-128">No</span></span>
    :::column-end:::
:::row-end:::

## <a name="see-also"></a><span data-ttu-id="c6508-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6508-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6508-130">Fichier de configuration MFTrace</span><span class="sxs-lookup"><span data-stu-id="c6508-130">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)
</dt> </dl>

 

 




