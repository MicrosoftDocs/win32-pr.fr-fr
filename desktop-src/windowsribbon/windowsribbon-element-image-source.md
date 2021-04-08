---
title: Image. source, propriété
description: Représente le chemin d’accès au répertoire d’une image.
ms.assetid: 174a518a-e9a3-4461-a9a3-d61b62d2b718
keywords:
- Image. source, ruban Windows
topic_type:
- apiref
api_name:
- Image.Source
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ace2a907280a11c54452b54bfb6172539980e38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740997"
---
# <a name="imagesource-property"></a><span data-ttu-id="bc757-104">Image. source, propriété</span><span class="sxs-lookup"><span data-stu-id="bc757-104">Image.Source property</span></span>

<span data-ttu-id="bc757-105">Représente le chemin d’accès au répertoire d’une image.</span><span class="sxs-lookup"><span data-stu-id="bc757-105">Represents the directory path of an image.</span></span>

## <a name="usage"></a><span data-ttu-id="bc757-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="bc757-106">Usage</span></span>

``` syntax
<Image.Source/>
```

## <a name="attributes"></a><span data-ttu-id="bc757-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="bc757-107">Attributes</span></span>

<span data-ttu-id="bc757-108">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="bc757-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="bc757-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="bc757-109">Child elements</span></span>

<span data-ttu-id="bc757-110">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="bc757-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="bc757-111">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="bc757-111">Parent elements</span></span>



| <span data-ttu-id="bc757-112">Élément</span><span class="sxs-lookup"><span data-stu-id="bc757-112">Element</span></span>                                                 |
|---------------------------------------------------------|
| [<span data-ttu-id="bc757-113">**Image**</span><span class="sxs-lookup"><span data-stu-id="bc757-113">**Image**</span></span>](windowsribbon-element-image.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="bc757-114">Notes</span><span class="sxs-lookup"><span data-stu-id="bc757-114">Remarks</span></span>

<span data-ttu-id="bc757-115">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="bc757-115">Optional.</span></span>

<span data-ttu-id="bc757-116">Peut se produire au plus une fois pour chaque [**image**](windowsribbon-element-image.md).</span><span class="sxs-lookup"><span data-stu-id="bc757-116">May occur at most once for each [**Image**](windowsribbon-element-image.md).</span></span>

<span data-ttu-id="bc757-117">Cet élément contient une valeur de type *XS : anyURI* ou toute séquence de caractères qui représente un Uniform Resource Identifier (Uri).</span><span class="sxs-lookup"><span data-stu-id="bc757-117">This element contains a value of type *xs:anyURI* or any sequence of characters that represents a Uniform Resource Identifier (URI).</span></span> <span data-ttu-id="bc757-118">La valeur URI est un chemin d’accès de répertoire absolu ou relatif (au fichier de balisage du ruban) d’une ressource image de type bitmap (BMP).</span><span class="sxs-lookup"><span data-stu-id="bc757-118">The URI value is an absolute or relative (to the Ribbon markup file) directory path of an image resource of type bitmap (BMP).</span></span>

## <a name="examples"></a><span data-ttu-id="bc757-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="bc757-119">Examples</span></span>

<span data-ttu-id="bc757-120">L’exemple de code suivant montre le balisage requis pour déclarer, via un ensemble d’éléments [**image**](windowsribbon-element-image.md) , une collection de ressources d’image conçues pour prendre en charge quatre paramètres de résolution d’écran spécifiques.</span><span class="sxs-lookup"><span data-stu-id="bc757-120">The following code example shows the markup required to declare, through a set of [**Image**](windowsribbon-element-image.md) elements, a collection of image resources that are designed to support four specific screen dpi settings.</span></span> <span data-ttu-id="bc757-121">La propriété **image. source** est utilisée pour spécifier le chemin d’accès à la ressource d’image.</span><span class="sxs-lookup"><span data-stu-id="bc757-121">The **Image.Source** property is used to specify the path to the image resource.</span></span>


```C++
<Command Name="cmdSizeAndColor" Symbol="IDR_CMD_SIZEANDCOLOR">
  <Command.LabelTitle>
    <String Id="250">Size and Color</String>
  </Command.LabelTitle>
  <Command.LargeImages>
    <Image Id="251" MinDPI="96">
      <Image.Source>res/sizeAndColor_96.bmp</Image.Source>
    </Image>
    <Image Id="252" MinDPI="120">
      <Image.Source>res/sizeAndColor_120.bmp</Image.Source>
    </Image>
    <Image Id="253" MinDPI="144">
      <Image.Source>res/sizeAndColor_144.bmp</Image.Source>
    </Image>
    <Image Id="254" MinDPI="192">
      <Image.Source>res/sizeAndColor_192.bmp</Image.Source>
    </Image>
  </Command.LargeImages>
</Command>
```



## <a name="requirements"></a><span data-ttu-id="bc757-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bc757-122">Requirements</span></span>



| <span data-ttu-id="bc757-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bc757-123">Requirement</span></span> | <span data-ttu-id="bc757-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc757-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="bc757-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc757-125">Minimum supported client</span></span><br/> | <span data-ttu-id="bc757-126">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bc757-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="bc757-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc757-127">Minimum supported server</span></span><br/> | <span data-ttu-id="bc757-128">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bc757-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





