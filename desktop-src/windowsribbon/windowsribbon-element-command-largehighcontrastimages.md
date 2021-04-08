---
title: Command. LargeHighContrastImages, propriété
description: Représente un conteneur d’images ; dans ce cas, les grandes images à utiliser avec les paramètres système à contraste élevé.
ms.assetid: e25f207f-ac3f-4a5f-8104-c928b38a52a8
keywords:
- Ruban Windows de la propriété Command. LargeHighContrastImages
topic_type:
- apiref
api_name:
- Command.LargeHighContrastImages
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e94fc31e2113990a1862fab7288ffeefef787cff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033155"
---
# <a name="commandlargehighcontrastimages-property"></a><span data-ttu-id="86c51-104">Command. LargeHighContrastImages, propriété</span><span class="sxs-lookup"><span data-stu-id="86c51-104">Command.LargeHighContrastImages property</span></span>

<span data-ttu-id="86c51-105">Représente un conteneur d’images ; dans ce cas, les grandes images à utiliser avec les paramètres système à contraste élevé.</span><span class="sxs-lookup"><span data-stu-id="86c51-105">Represents a container of images; in this case, large images for use with high-contrast system settings.</span></span>

## <a name="usage"></a><span data-ttu-id="86c51-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="86c51-106">Usage</span></span>

``` syntax
<Command.LargeHighContrastImages>
  child elements
</Command.LargeHighContrastImages>
```

## <a name="attributes"></a><span data-ttu-id="86c51-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="86c51-107">Attributes</span></span>

<span data-ttu-id="86c51-108">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="86c51-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="86c51-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="86c51-109">Child elements</span></span>



| <span data-ttu-id="86c51-110">Élément</span><span class="sxs-lookup"><span data-stu-id="86c51-110">Element</span></span>                                                 | <span data-ttu-id="86c51-111">Description</span><span class="sxs-lookup"><span data-stu-id="86c51-111">Description</span></span>                                        |
|---------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="86c51-112">**Image**</span><span class="sxs-lookup"><span data-stu-id="86c51-112">**Image**</span></span>](windowsribbon-element-image.md)<br/> | <span data-ttu-id="86c51-113">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="86c51-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="86c51-114">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="86c51-114">Parent elements</span></span>



| <span data-ttu-id="86c51-115">Élément</span><span class="sxs-lookup"><span data-stu-id="86c51-115">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="86c51-116">**Commande**</span><span class="sxs-lookup"><span data-stu-id="86c51-116">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="86c51-117">Notes</span><span class="sxs-lookup"><span data-stu-id="86c51-117">Remarks</span></span>

<span data-ttu-id="86c51-118">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="86c51-118">Optional.</span></span>

<span data-ttu-id="86c51-119">Peut se produire au plus une fois pour chaque [**commande**](windowsribbon-element-command.md).</span><span class="sxs-lookup"><span data-stu-id="86c51-119">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="86c51-120">Les ressources d’image doivent être conformes au format graphique bitmap standard (BMP) utilisé dans Windows.</span><span class="sxs-lookup"><span data-stu-id="86c51-120">Image resources must conform to the standard bitmap (BMP) graphics format used in Windows.</span></span>

## <a name="examples"></a><span data-ttu-id="86c51-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="86c51-121">Examples</span></span>

<span data-ttu-id="86c51-122">L’exemple suivant illustre le balisage de base pour le [**SplitButton**](windowsribbon-element-splitbutton.md) avec un élément [**MenuGroup**](windowsribbon-element-menugroup.md) .</span><span class="sxs-lookup"><span data-stu-id="86c51-122">The following example demonstrates the basic markup for the [**SplitButton**](windowsribbon-element-splitbutton.md) with a [**MenuGroup**](windowsribbon-element-menugroup.md) element.</span></span>

<span data-ttu-id="86c51-123">Cette section de code montre les déclarations de commande [**SplitButton**](windowsribbon-element-splitbutton.md) et [**MenuGroup**](windowsribbon-element-menugroup.md) avec des ressources d’image à contraste élevé et de petite taille.</span><span class="sxs-lookup"><span data-stu-id="86c51-123">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and [**MenuGroup**](windowsribbon-element-menugroup.md) Command declarations with large and small high contrast image resources.</span></span> <span data-ttu-id="86c51-124">Un [**groupe**](windowsribbon-element-group.md) associé qui agit en tant que conteneur parent de l’élément **SplitButton** est également déclaré.</span><span class="sxs-lookup"><span data-stu-id="86c51-124">An associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **SplitButton** element is also declared.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="86c51-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="86c51-125">Requirements</span></span>



| <span data-ttu-id="86c51-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="86c51-126">Requirement</span></span> | <span data-ttu-id="86c51-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="86c51-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="86c51-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="86c51-128">Minimum supported client</span></span><br/> | <span data-ttu-id="86c51-129">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="86c51-129">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="86c51-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="86c51-130">Minimum supported server</span></span><br/> | <span data-ttu-id="86c51-131">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="86c51-131">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="86c51-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86c51-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86c51-133">Spécification des ressources d’image du ruban</span><span class="sxs-lookup"><span data-stu-id="86c51-133">Specifying Ribbon Image Resources</span></span>](windowsribbon-imageformats.md)
</dt> <dt>

[<span data-ttu-id="86c51-134">IU \_ \_ LargeHighContrastImage</span><span class="sxs-lookup"><span data-stu-id="86c51-134">UI\_PKEY\_LargeHighContrastImage</span></span>](windowsribbon-reference-properties-uipkey-largehighcontrastimage.md)
</dt> </dl>

 

 





