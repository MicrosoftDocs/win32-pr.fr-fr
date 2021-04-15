---
title: Command. SmallImages, propriété
description: Représente un conteneur d’images ; dans ce cas, les petites images.
ms.assetid: 15c00e61-543a-4cc8-b329-516985d02359
keywords:
- Ruban Windows de la propriété Command. SmallImages
topic_type:
- apiref
api_name:
- Command.SmallImages
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b18556cf519c21b01c3e80b63cbfc9cdf9d7d153
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466579"
---
# <a name="commandsmallimages-property"></a><span data-ttu-id="3ba1b-104">Command. SmallImages, propriété</span><span class="sxs-lookup"><span data-stu-id="3ba1b-104">Command.SmallImages property</span></span>

<span data-ttu-id="3ba1b-105">Représente un conteneur d’images ; dans ce cas, les petites images.</span><span class="sxs-lookup"><span data-stu-id="3ba1b-105">Represents a container of images; in this case, small images.</span></span>

## <a name="usage"></a><span data-ttu-id="3ba1b-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="3ba1b-106">Usage</span></span>

``` syntax
<Command.SmallImages>
  child elements
</Command.SmallImages>
```

## <a name="attributes"></a><span data-ttu-id="3ba1b-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="3ba1b-107">Attributes</span></span>

<span data-ttu-id="3ba1b-108">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="3ba1b-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="3ba1b-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3ba1b-109">Child elements</span></span>



| <span data-ttu-id="3ba1b-110">Élément</span><span class="sxs-lookup"><span data-stu-id="3ba1b-110">Element</span></span>                                                 | <span data-ttu-id="3ba1b-111">Description</span><span class="sxs-lookup"><span data-stu-id="3ba1b-111">Description</span></span>                                        |
|---------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="3ba1b-112">**Image**</span><span class="sxs-lookup"><span data-stu-id="3ba1b-112">**Image**</span></span>](windowsribbon-element-image.md)<br/> | <span data-ttu-id="3ba1b-113">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="3ba1b-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="3ba1b-114">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="3ba1b-114">Parent elements</span></span>



| <span data-ttu-id="3ba1b-115">Élément</span><span class="sxs-lookup"><span data-stu-id="3ba1b-115">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="3ba1b-116">**Commande**</span><span class="sxs-lookup"><span data-stu-id="3ba1b-116">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="3ba1b-117">Notes</span><span class="sxs-lookup"><span data-stu-id="3ba1b-117">Remarks</span></span>

<span data-ttu-id="3ba1b-118">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="3ba1b-118">Optional.</span></span>

<span data-ttu-id="3ba1b-119">Peut se produire au plus une fois pour chaque [**commande**](windowsribbon-element-command.md).</span><span class="sxs-lookup"><span data-stu-id="3ba1b-119">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="3ba1b-120">Les ressources d’image doivent être conformes au format graphique bitmap standard (BMP) utilisé dans Windows.</span><span class="sxs-lookup"><span data-stu-id="3ba1b-120">Image resources must conform to the standard bitmap (BMP) graphics format used in Windows.</span></span>

## <a name="examples"></a><span data-ttu-id="3ba1b-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="3ba1b-121">Examples</span></span>

<span data-ttu-id="3ba1b-122">L’exemple suivant illustre le balisage de base pour le [**SplitButton**](windowsribbon-element-splitbutton.md) avec un élément [**MenuGroup**](windowsribbon-element-menugroup.md) .</span><span class="sxs-lookup"><span data-stu-id="3ba1b-122">The following example demonstrates the basic markup for the [**SplitButton**](windowsribbon-element-splitbutton.md) with a [**MenuGroup**](windowsribbon-element-menugroup.md) element.</span></span>

<span data-ttu-id="3ba1b-123">Cette section de code montre les déclarations de commande [**SplitButton**](windowsribbon-element-splitbutton.md) et [**MenuGroup**](windowsribbon-element-menugroup.md) avec une grande ressource d’image.</span><span class="sxs-lookup"><span data-stu-id="3ba1b-123">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and [**MenuGroup**](windowsribbon-element-menugroup.md) Command declarations with a large and a small image resource.</span></span> <span data-ttu-id="3ba1b-124">Un [**groupe**](windowsribbon-element-group.md) associé qui agit en tant que conteneur parent de l’élément **SplitButton** est également déclaré.</span><span class="sxs-lookup"><span data-stu-id="3ba1b-124">An associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **SplitButton** element is also declared.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="3ba1b-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3ba1b-125">Requirements</span></span>



| <span data-ttu-id="3ba1b-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3ba1b-126">Requirement</span></span> | <span data-ttu-id="3ba1b-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="3ba1b-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="3ba1b-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ba1b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3ba1b-129">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3ba1b-129">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="3ba1b-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ba1b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3ba1b-131">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3ba1b-131">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3ba1b-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ba1b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ba1b-133">Spécification des ressources d’image du ruban</span><span class="sxs-lookup"><span data-stu-id="3ba1b-133">Specifying Ribbon Image Resources</span></span>](windowsribbon-imageformats.md)
</dt> <dt>

[<span data-ttu-id="3ba1b-134">IU \_ \_ SmallImage</span><span class="sxs-lookup"><span data-stu-id="3ba1b-134">UI\_PKEY\_SmallImage</span></span>](windowsribbon-reference-properties-uipkey-smallimage.md)
</dt> </dl>

 

 





