---
title: THEMe. openView
description: La méthode openView ouvre une vue dans une nouvelle fenêtre.
ms.assetid: 2aa63c29-dafe-4942-a010-076f1503862b
keywords:
- THEMe. openView lecteur Windows Media
topic_type:
- apiref
api_name:
- THEME.openView
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d66ff2cf47004c7687a37f1f22a87bdeb534d344
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540290"
---
# <a name="themeopenview"></a><span data-ttu-id="effb6-104">THEMe. openView</span><span class="sxs-lookup"><span data-stu-id="effb6-104">THEME.openView</span></span>

<span data-ttu-id="effb6-105">La méthode **openView** ouvre une **vue** dans une nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="effb6-105">The **openView** method opens a **VIEW** in a new window.</span></span>

``` syntax
        theme.openView(view)
```

## <a name="parameters"></a><span data-ttu-id="effb6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="effb6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="effb6-107"><span id="view"></span><span id="VIEW"></span>*affichage*</span><span class="sxs-lookup"><span data-stu-id="effb6-107"><span id="view"></span><span id="VIEW"></span>*view*</span></span>
</dt> <dd>

<span data-ttu-id="effb6-108">**Chaîne** spécifiant l' **ID** de la **vue** à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="effb6-108">A **String** specifying the **id** of the **VIEW** to open.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="effb6-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="effb6-109">Return Value</span></span>

<span data-ttu-id="effb6-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="effb6-110">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="effb6-111">Exemples</span><span class="sxs-lookup"><span data-stu-id="effb6-111">Examples</span></span>


```JScript
<THEME>
  <VIEW>
    <TEXT value="open" 
        onclick="jscript:theme.openView('newView')"/>
    <TEXT top="30" value="close" 
        onclick="jscript:theme.closeView('newView')"/>
  </VIEW>
  <VIEW id="newView"/>
</THEME>
```



## <a name="requirements"></a><span data-ttu-id="effb6-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="effb6-112">Requirements</span></span>



| <span data-ttu-id="effb6-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="effb6-113">Requirement</span></span> | <span data-ttu-id="effb6-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="effb6-114">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="effb6-115">Version</span><span class="sxs-lookup"><span data-stu-id="effb6-115">Version</span></span><br/> | <span data-ttu-id="effb6-116">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="effb6-116">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="effb6-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="effb6-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="effb6-118">**Élément THEMe**</span><span class="sxs-lookup"><span data-stu-id="effb6-118">**THEME Element**</span></span>](theme-element.md)
</dt> <dt>

[<span data-ttu-id="effb6-119">**THÈME. évènement CloseView**</span><span class="sxs-lookup"><span data-stu-id="effb6-119">**THEME.closeView**</span></span>](theme-closeview.md)
</dt> <dt>

[<span data-ttu-id="effb6-120">**THÈME. openViewRelative**</span><span class="sxs-lookup"><span data-stu-id="effb6-120">**THEME.openViewRelative**</span></span>](theme-openviewrelative.md)
</dt> </dl>

 

 





