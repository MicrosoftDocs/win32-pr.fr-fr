---
description: Spécifie un fournisseur de trace (ETW ou WPP) pour MFTrace.
ms.assetid: 692cce3b-ebf5-4a49-8c37-48c8ef6caee7
title: provider (élément)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56ca319b686101766dacd79821ac6d9caf859cf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753900"
---
# <a name="provider-element"></a><span data-ttu-id="143d0-103">provider (élément)</span><span class="sxs-lookup"><span data-stu-id="143d0-103">provider element</span></span>

<span data-ttu-id="143d0-104">Spécifie un fournisseur de trace (ETW ou WPP) pour [MFTrace](mftrace.md).</span><span class="sxs-lookup"><span data-stu-id="143d0-104">Specifies a trace provider (ETW or WPP) for [MFTrace](mftrace.md).</span></span>

## <a name="usage"></a><span data-ttu-id="143d0-105">Utilisation</span><span class="sxs-lookup"><span data-stu-id="143d0-105">Usage</span></span>

``` syntax
<provider
  ID = "CDATA"
  level = "CDATA">
  child elements
</provider>
```

## <a name="attributes"></a><span data-ttu-id="143d0-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="143d0-106">Attributes</span></span>



| <span data-ttu-id="143d0-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="143d0-107">Attribute</span></span>            | <span data-ttu-id="143d0-108">Type</span><span class="sxs-lookup"><span data-stu-id="143d0-108">Type</span></span>             | <span data-ttu-id="143d0-109">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="143d0-109">Required</span></span>       | <span data-ttu-id="143d0-110">Description</span><span class="sxs-lookup"><span data-stu-id="143d0-110">Description</span></span>                                              |
|----------------------|------------------|----------------|----------------------------------------------------------|
| <span data-ttu-id="143d0-111">**Identifiant**</span><span class="sxs-lookup"><span data-stu-id="143d0-111">**ID**</span></span><br/>    | <span data-ttu-id="143d0-112">CDATA</span><span class="sxs-lookup"><span data-stu-id="143d0-112">CDATA</span></span><br/> | <span data-ttu-id="143d0-113">Oui</span><span class="sxs-lookup"><span data-stu-id="143d0-113">Yes</span></span><br/> | <span data-ttu-id="143d0-114">Nom ou GUID du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="143d0-114">The name or GUID of the provider.</span></span><br/> <br/> |
| <span data-ttu-id="143d0-115">**level**</span><span class="sxs-lookup"><span data-stu-id="143d0-115">**level**</span></span><br/> | <span data-ttu-id="143d0-116">CDATA</span><span class="sxs-lookup"><span data-stu-id="143d0-116">CDATA</span></span><br/> | <span data-ttu-id="143d0-117">Oui</span><span class="sxs-lookup"><span data-stu-id="143d0-117">Yes</span></span><br/> | <span data-ttu-id="143d0-118">Niveau de trace.</span><span class="sxs-lookup"><span data-stu-id="143d0-118">The trace level.</span></span><br/> <br/>                  |



## <a name="child-elements"></a><span data-ttu-id="143d0-119">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="143d0-119">Child elements</span></span>



| <span data-ttu-id="143d0-120">Élément</span><span class="sxs-lookup"><span data-stu-id="143d0-120">Element</span></span>                               |
|---------------------------------------|
| [<span data-ttu-id="143d0-121">**keyword**</span><span class="sxs-lookup"><span data-stu-id="143d0-121">**keyword**</span></span>](keyword.md)<br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="143d0-122">Séquence d’éléments enfants</span><span class="sxs-lookup"><span data-stu-id="143d0-122">Child element sequence</span></span>

``` syntax
keyword+
```

## <a name="parent-elements"></a><span data-ttu-id="143d0-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="143d0-123">Parent elements</span></span>



| <span data-ttu-id="143d0-124">Élément</span><span class="sxs-lookup"><span data-stu-id="143d0-124">Element</span></span>                                   |
|-------------------------------------------|
| [<span data-ttu-id="143d0-125">**fournisseurs**</span><span class="sxs-lookup"><span data-stu-id="143d0-125">**providers**</span></span>](providers.md)<br/> |



## <a name="element-information"></a><span data-ttu-id="143d0-126">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="143d0-126">Element information</span></span>



|              |     |
|--------------|-----|
| <span data-ttu-id="143d0-127">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="143d0-127">Can be empty</span></span> | <span data-ttu-id="143d0-128">Non</span><span class="sxs-lookup"><span data-stu-id="143d0-128">No</span></span>  |



## <a name="see-also"></a><span data-ttu-id="143d0-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="143d0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="143d0-130">Fichier de configuration MFTrace</span><span class="sxs-lookup"><span data-stu-id="143d0-130">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)
</dt> </dl>

 

 




