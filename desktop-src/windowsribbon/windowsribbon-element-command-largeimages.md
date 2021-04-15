---
title: Command. LargeImages, propriété
description: Représente un conteneur d’images ; dans ce cas, les grandes images.
ms.assetid: 9fcd3694-7847-43e2-9877-47daf47aae9a
keywords:
- Ruban Windows de la propriété Command. LargeImages
topic_type:
- apiref
api_name:
- Command.LargeImages
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf71557506d4b9cced21069473d1a6db9b208b8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466583"
---
# <a name="commandlargeimages-property"></a><span data-ttu-id="58ed9-104">Command. LargeImages, propriété</span><span class="sxs-lookup"><span data-stu-id="58ed9-104">Command.LargeImages property</span></span>

<span data-ttu-id="58ed9-105">Représente un conteneur d’images ; dans ce cas, les grandes images.</span><span class="sxs-lookup"><span data-stu-id="58ed9-105">Represents a container of images; in this case, large images.</span></span>

## <a name="usage"></a><span data-ttu-id="58ed9-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="58ed9-106">Usage</span></span>

``` syntax
<Command.LargeImages>
  child elements
</Command.LargeImages>
```

## <a name="attributes"></a><span data-ttu-id="58ed9-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="58ed9-107">Attributes</span></span>

<span data-ttu-id="58ed9-108">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="58ed9-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="58ed9-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="58ed9-109">Child elements</span></span>



| <span data-ttu-id="58ed9-110">Élément</span><span class="sxs-lookup"><span data-stu-id="58ed9-110">Element</span></span>                                                 | <span data-ttu-id="58ed9-111">Description</span><span class="sxs-lookup"><span data-stu-id="58ed9-111">Description</span></span>                                        |
|---------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="58ed9-112">**Image**</span><span class="sxs-lookup"><span data-stu-id="58ed9-112">**Image**</span></span>](windowsribbon-element-image.md)<br/> | <span data-ttu-id="58ed9-113">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="58ed9-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="58ed9-114">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="58ed9-114">Parent elements</span></span>



| <span data-ttu-id="58ed9-115">Élément</span><span class="sxs-lookup"><span data-stu-id="58ed9-115">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="58ed9-116">**Commande**</span><span class="sxs-lookup"><span data-stu-id="58ed9-116">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="58ed9-117">Notes</span><span class="sxs-lookup"><span data-stu-id="58ed9-117">Remarks</span></span>

<span data-ttu-id="58ed9-118">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="58ed9-118">Optional.</span></span>

<span data-ttu-id="58ed9-119">Peut se produire au plus une fois pour chaque [**commande**](windowsribbon-element-command.md).</span><span class="sxs-lookup"><span data-stu-id="58ed9-119">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="58ed9-120">Les ressources d’image doivent être conformes au format graphique bitmap standard (BMP) utilisé dans Windows.</span><span class="sxs-lookup"><span data-stu-id="58ed9-120">Image resources must conform to the standard bitmap (BMP) graphics format used in Windows.</span></span>

## <a name="examples"></a><span data-ttu-id="58ed9-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="58ed9-121">Examples</span></span>

<span data-ttu-id="58ed9-122">L’exemple suivant illustre le balisage de base pour le [**SplitButton**](windowsribbon-element-splitbutton.md) avec un élément [**MenuGroup**](windowsribbon-element-menugroup.md) .</span><span class="sxs-lookup"><span data-stu-id="58ed9-122">The following example demonstrates the basic markup for the [**SplitButton**](windowsribbon-element-splitbutton.md) with a [**MenuGroup**](windowsribbon-element-menugroup.md) element.</span></span>

<span data-ttu-id="58ed9-123">Cette section de code montre les déclarations de commande [**SplitButton**](windowsribbon-element-splitbutton.md) et [**MenuGroup**](windowsribbon-element-menugroup.md) avec une grande ressource d’image.</span><span class="sxs-lookup"><span data-stu-id="58ed9-123">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and [**MenuGroup**](windowsribbon-element-menugroup.md) Command declarations with a large and a small image resource.</span></span> <span data-ttu-id="58ed9-124">Un [**groupe**](windowsribbon-element-group.md) associé qui agit en tant que conteneur parent de l’élément **SplitButton** est également déclaré.</span><span class="sxs-lookup"><span data-stu-id="58ed9-124">An associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **SplitButton** element is also declared.</span></span>


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



## <a name="requirements"></a><span data-ttu-id="58ed9-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="58ed9-125">Requirements</span></span>



| <span data-ttu-id="58ed9-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="58ed9-126">Requirement</span></span> | <span data-ttu-id="58ed9-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="58ed9-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="58ed9-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58ed9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="58ed9-129">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="58ed9-129">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="58ed9-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58ed9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="58ed9-131">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="58ed9-131">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="58ed9-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58ed9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58ed9-133">Spécification des ressources d’image du ruban</span><span class="sxs-lookup"><span data-stu-id="58ed9-133">Specifying Ribbon Image Resources</span></span>](windowsribbon-imageformats.md)
</dt> <dt>

[<span data-ttu-id="58ed9-134">IU \_ \_ LARGEIMAGE</span><span class="sxs-lookup"><span data-stu-id="58ed9-134">UI\_PKEY\_LargeImage</span></span>](windowsribbon-reference-properties-uipkey-largeimage.md)
</dt> </dl>

 

 





