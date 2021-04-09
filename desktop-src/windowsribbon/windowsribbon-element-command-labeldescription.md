---
title: Command. LabelDescription, propriété
description: Représente une description de l’étiquette.
ms.assetid: 6c683e9e-0742-466e-9fdd-3d29f8ccb9ff
keywords:
- Ruban Windows de la propriété Command. LabelDescription
topic_type:
- apiref
api_name:
- Command.LabelDescription
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f748425b4c8363feee737d18c750b3a1d91121b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942677"
---
# <a name="commandlabeldescription-property"></a><span data-ttu-id="811ce-104">Command. LabelDescription, propriété</span><span class="sxs-lookup"><span data-stu-id="811ce-104">Command.LabelDescription property</span></span>

<span data-ttu-id="811ce-105">Représente une description de l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="811ce-105">Represents a label description.</span></span>

## <a name="usage"></a><span data-ttu-id="811ce-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="811ce-106">Usage</span></span>

``` syntax
<Command.LabelDescription>
  child elements
</Command.LabelDescription>
```

## <a name="attributes"></a><span data-ttu-id="811ce-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="811ce-107">Attributes</span></span>

<span data-ttu-id="811ce-108">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="811ce-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="811ce-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="811ce-109">Child elements</span></span>



| <span data-ttu-id="811ce-110">Élément</span><span class="sxs-lookup"><span data-stu-id="811ce-110">Element</span></span>                                                   | <span data-ttu-id="811ce-111">Description</span><span class="sxs-lookup"><span data-stu-id="811ce-111">Description</span></span>                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="811ce-112">**String**</span><span class="sxs-lookup"><span data-stu-id="811ce-112">**String**</span></span>](windowsribbon-element-string.md)<br/> | <span data-ttu-id="811ce-113">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="811ce-113">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="811ce-114">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="811ce-114">Parent elements</span></span>



| <span data-ttu-id="811ce-115">Élément</span><span class="sxs-lookup"><span data-stu-id="811ce-115">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="811ce-116">**Commande**</span><span class="sxs-lookup"><span data-stu-id="811ce-116">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="811ce-117">Notes</span><span class="sxs-lookup"><span data-stu-id="811ce-117">Remarks</span></span>

<span data-ttu-id="811ce-118">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="811ce-118">Optional.</span></span>

<span data-ttu-id="811ce-119">Peut se produire au plus une fois pour chaque [**commande**](windowsribbon-element-command.md).</span><span class="sxs-lookup"><span data-stu-id="811ce-119">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="811ce-120">**Command. LabelDescription** peut contenir une valeur de *type xs : String* limitée à toute séquence de caractères, y compris les espaces blancs et les sauts de ligne.</span><span class="sxs-lookup"><span data-stu-id="811ce-120">**Command.LabelDescription** can contain a value of *type xs:string* constrained to any sequence of characters, including white space and line-break characters.</span></span>

> [!Note]  
> <span data-ttu-id="811ce-121">Utilisez la référence de caractère XML UCS (Universal Character Set) `&#xA;` pour spécifier un saut de ligne.</span><span class="sxs-lookup"><span data-stu-id="811ce-121">Use the Universal Character Set (UCS) XML character reference `&#xA;` to specify a line break.</span></span>

 

<span data-ttu-id="811ce-122">La longueur maximale est illimitée.</span><span class="sxs-lookup"><span data-stu-id="811ce-122">The maximum length is unbounded.</span></span>

<span data-ttu-id="811ce-123">Si aucune valeur n’est fournie pour **Command. LabelDescription**, l’élément enfant [**String**](windowsribbon-element-string.md) est requis.</span><span class="sxs-lookup"><span data-stu-id="811ce-123">If no value is supplied for **Command.LabelDescription**, the [**String**](windowsribbon-element-string.md) child element is required.</span></span>

> [!Note]  
> <span data-ttu-id="811ce-124">Si **Command. LabelDescription** contient à la fois une valeur et un élément enfant de [**chaîne**](windowsribbon-element-string.md) , la **chaîne** est prioritaire.</span><span class="sxs-lookup"><span data-stu-id="811ce-124">If **Command.LabelDescription** contains both a value and a [**String**](windowsribbon-element-string.md) child element, **String** takes precedence.</span></span>

 

<span data-ttu-id="811ce-125">**Command. LabelDescription** prend uniquement en charge l’alignement à gauche.</span><span class="sxs-lookup"><span data-stu-id="811ce-125">**Command.LabelDescription** only supports left alignment.</span></span>

## <a name="examples"></a><span data-ttu-id="811ce-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="811ce-126">Examples</span></span>

<span data-ttu-id="811ce-127">L’exemple suivant montre un manifeste de commandes du presse-papiers avec différentes déclarations **Command. LabelDescription** .</span><span class="sxs-lookup"><span data-stu-id="811ce-127">The following example shows a manifest of clipboard Commands with various **Command.LabelDescription** declarations.</span></span>


```XML
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



## <a name="requirements"></a><span data-ttu-id="811ce-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="811ce-128">Requirements</span></span>



| <span data-ttu-id="811ce-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="811ce-129">Requirement</span></span> | <span data-ttu-id="811ce-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="811ce-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="811ce-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="811ce-131">Minimum supported client</span></span><br/> | <span data-ttu-id="811ce-132">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="811ce-132">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="811ce-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="811ce-133">Minimum supported server</span></span><br/> | <span data-ttu-id="811ce-134">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="811ce-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="811ce-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="811ce-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="811ce-136">IU \_ \_ LabelDescription</span><span class="sxs-lookup"><span data-stu-id="811ce-136">UI\_PKEY\_LabelDescription</span></span>](windowsribbon-reference-properties-uipkey-labeldescription.md)
</dt> </dl>

 

 





