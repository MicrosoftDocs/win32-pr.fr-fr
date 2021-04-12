---
title: Application. Commands, propriété
description: Représente un conteneur pour toutes les commandes qui sont définies par l’application.
ms.assetid: 160d7d28-2d64-4cbc-b2b9-2da6b2f5b3c8
keywords:
- Ruban Windows de la propriété application. Commands
topic_type:
- apiref
api_name:
- Application.Commands
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8de2b88b97dda96636a9c5da3ad078f678091d8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465275"
---
# <a name="applicationcommands-property"></a><span data-ttu-id="3b88a-104">Application. Commands, propriété</span><span class="sxs-lookup"><span data-stu-id="3b88a-104">Application.Commands property</span></span>

<span data-ttu-id="3b88a-105">Représente un conteneur pour toutes les commandes qui sont définies par l’application.</span><span class="sxs-lookup"><span data-stu-id="3b88a-105">Represents a container for all the Commands that are defined by the application.</span></span>

## <a name="usage"></a><span data-ttu-id="3b88a-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="3b88a-106">Usage</span></span>

``` syntax
<Application.Commands>
  child elements
</Application.Commands>
```

## <a name="attributes"></a><span data-ttu-id="3b88a-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="3b88a-107">Attributes</span></span>

<span data-ttu-id="3b88a-108">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="3b88a-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="3b88a-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3b88a-109">Child elements</span></span>



| <span data-ttu-id="3b88a-110">Élément</span><span class="sxs-lookup"><span data-stu-id="3b88a-110">Element</span></span>                                                     | <span data-ttu-id="3b88a-111">Description</span><span class="sxs-lookup"><span data-stu-id="3b88a-111">Description</span></span>                                        |
|-------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="3b88a-112">**Commande**</span><span class="sxs-lookup"><span data-stu-id="3b88a-112">**Command**</span></span>](windowsribbon-element-command.md)<br/> | <span data-ttu-id="3b88a-113">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="3b88a-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="3b88a-114">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="3b88a-114">Parent elements</span></span>



| <span data-ttu-id="3b88a-115">Élément</span><span class="sxs-lookup"><span data-stu-id="3b88a-115">Element</span></span>                                                             |
|---------------------------------------------------------------------|
| [<span data-ttu-id="3b88a-116">**Application**</span><span class="sxs-lookup"><span data-stu-id="3b88a-116">**Application**</span></span>](windowsribbon-element-application.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="3b88a-117">Notes</span><span class="sxs-lookup"><span data-stu-id="3b88a-117">Remarks</span></span>

<span data-ttu-id="3b88a-118">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="3b88a-118">Optional.</span></span>

<span data-ttu-id="3b88a-119">Peut se produire au plus une fois pour chaque élément d' [**application**](windowsribbon-element-application.md) .</span><span class="sxs-lookup"><span data-stu-id="3b88a-119">May occur at most once for each [**Application**](windowsribbon-element-application.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="3b88a-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="3b88a-120">Examples</span></span>

<span data-ttu-id="3b88a-121">L’exemple suivant montre un élément **application. Commands** qui contient un manifeste de commandes du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="3b88a-121">The following example shows an **Application.Commands** element that contains a manifest of clipboard Commands.</span></span>


```C++
<Application.Commands>
```




```C++
<Command Name="cmdHomeTab"
         LabelTitle="Home"
         Keytip="H" />
<Command Name="cmdClipboardGroup"
         Symbol="IDR_CMD_CLIPBOARD"
         Id="10000"
         Comment="Command definition for clipboard group"
         LabelTitle="Clipboard"
         Keytip="CB" />
<Command Name="cmdCopy"
         Symbol="IDR_CMD_COPY"
         LabelTitle="Copy"
         LabelDescription="Copy"
         Keytip="C"
         TooltipTitle="Copy"
         TooltipDescription="Click to copy">
  <Command.SmallImages>
    <Image>res/copyS_16.bmp</Image>
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/copyL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdPaste"
         Symbol="IDR_CMD_PASTE" >
  <Command.LabelTitle>Paste</Command.LabelTitle>
  <Command.LabelDescription>
    <String Content="Paste contents of clipboard"
            Id="10001"
            Symbol="IDR_RES_LABELDESC_PASTE" />
  </Command.LabelDescription>
  <Command.Keytip>P</Command.Keytip>
  <Command.TooltipTitle>
    <String Content="Paste contents of clipboard"
            Id="10002"
            Symbol="IDR_RES_TOOLTIP_PASTE"/>
  </Command.TooltipTitle>
  <Command.TooltipDescription>
    <String Content="Click to paste contents of clipboard"/>
  </Command.TooltipDescription>
  <Command.SmallImages>
    <Image
      Id="10010"
      MinDPI="96"
      Symbol="IDR_RES_SMALL_IMAGE96">
      <Image.Source>res/pasteS_96bpp.bmp</Image.Source>
    </Image>
    <Image Source="res/pasteS_120bpp.bmp"
           Id="10011"
           MinDPI="120"
           Symbol="IDR_RES_SMALL_IMAGE120" />
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/pasteL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdMinimize"
         Symbol="IDR_CMD_MINIMIZE"
         Id="10001"
         LabelTitle="Minimize" />
```




```C++
</Application.Commands>
```



## <a name="requirements"></a><span data-ttu-id="3b88a-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3b88a-122">Requirements</span></span>



| <span data-ttu-id="3b88a-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3b88a-123">Requirement</span></span> | <span data-ttu-id="3b88a-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b88a-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="3b88a-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b88a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3b88a-126">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3b88a-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="3b88a-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b88a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3b88a-128">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3b88a-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3b88a-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b88a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b88a-130">**Application. views**</span><span class="sxs-lookup"><span data-stu-id="3b88a-130">**Application.Views**</span></span>](windowsribbon-element-application-views.md)
</dt> </dl>

 

 





