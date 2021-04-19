---
title: THÈME. évènement CloseView
description: La méthode évènement CloseView ferme une vue ouverte.
ms.assetid: 37b56a7d-8031-4055-95ad-0510105e1c1f
keywords:
- THEMe. évènement CloseView Windows Media Player
topic_type:
- apiref
api_name:
- THEME.closeView
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b39083979809fc2e747c54569db8d03298a951c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530498"
---
# <a name="themecloseview"></a><span data-ttu-id="85ece-104">THÈME. évènement CloseView</span><span class="sxs-lookup"><span data-stu-id="85ece-104">THEME.closeView</span></span>

<span data-ttu-id="85ece-105">La méthode **évènement CloseView** ferme une **vue** ouverte.</span><span class="sxs-lookup"><span data-stu-id="85ece-105">The **closeView** method closes an open **VIEW**.</span></span>

``` syntax
        theme.closeView(theView)
```

## <a name="parameters"></a><span data-ttu-id="85ece-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="85ece-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85ece-107"><span id="theView"></span><span id="theview"></span><span id="THEVIEW"></span>*theView*</span><span class="sxs-lookup"><span data-stu-id="85ece-107"><span id="theView"></span><span id="theview"></span><span id="THEVIEW"></span>*theView*</span></span>
</dt> <dd>

<span data-ttu-id="85ece-108">**Chaîne** spécifiant l' **ID** de la **vue** à fermer.</span><span class="sxs-lookup"><span data-stu-id="85ece-108">A **String** specifying the **id** of the **VIEW** to close.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85ece-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="85ece-109">Return Value</span></span>

<span data-ttu-id="85ece-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="85ece-110">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="85ece-111">Exemples</span><span class="sxs-lookup"><span data-stu-id="85ece-111">Examples</span></span>


```C++
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



## <a name="requirements"></a><span data-ttu-id="85ece-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="85ece-112">Requirements</span></span>



| <span data-ttu-id="85ece-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="85ece-113">Requirement</span></span> | <span data-ttu-id="85ece-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="85ece-114">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="85ece-115">Version</span><span class="sxs-lookup"><span data-stu-id="85ece-115">Version</span></span><br/> | <span data-ttu-id="85ece-116">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="85ece-116">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="85ece-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="85ece-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85ece-118">**Élément THEMe**</span><span class="sxs-lookup"><span data-stu-id="85ece-118">**THEME Element**</span></span>](theme-element.md)
</dt> <dt>

[<span data-ttu-id="85ece-119">**THEMe. openView**</span><span class="sxs-lookup"><span data-stu-id="85ece-119">**THEME.openView**</span></span>](theme-openview.md)
</dt> </dl>

 

 





