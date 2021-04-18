---
title: attribute_onchange
description: Lorsqu’un attribut d’apparence change de valeur, un événement qui peut être géré par un gestionnaire d’événements se produit. Le nom du gestionnaire d’événements est le nom de l’attribut suivi d’un trait de soulignement et de \ 0034 ; OnChange \ 0034 ;, par exemple, \ 0034 ; valeur \_ OnChange \ 0034 ;.
ms.assetid: 783b686c-d56c-4036-9af4-97b9b246ef7e
keywords:
- attribute_onchange le lecteur Windows Media
topic_type:
- apiref
api_name:
- attribute_onchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 45c4955193507e258d055a3399fc565c569fd291
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526795"
---
# <a name="attribute_onchange"></a><span data-ttu-id="fa098-105">OnChange d’attribut \_</span><span class="sxs-lookup"><span data-stu-id="fa098-105">attribute\_onchange</span></span>

<span data-ttu-id="fa098-106">Lorsqu’un attribut d’apparence change de valeur, un événement qui peut être géré par un gestionnaire d’événements se produit.</span><span class="sxs-lookup"><span data-stu-id="fa098-106">When a skin attribute changes value, an event occurs that can be handled by an event handler.</span></span> <span data-ttu-id="fa098-107">Le nom du gestionnaire d’événements est le nom de l’attribut suivi d’un trait de soulignement et de « OnChange », tels que « valeur \_ OnChange ».</span><span class="sxs-lookup"><span data-stu-id="fa098-107">The name of the event handler is the name of the attribute followed by an underscore and "onchange", such as "value\_onchange".</span></span>

``` syntax
        attribute_onchange
```

## <a name="examples"></a><span data-ttu-id="fa098-108">Exemples</span><span class="sxs-lookup"><span data-stu-id="fa098-108">Examples</span></span>


```JScript
<SLIDER 
  thumbImage = "thumb.gif"
  value_onchange = "JScript: if (value == 100) backgroundColor = 'green';"
/>

```



## <a name="requirements"></a><span data-ttu-id="fa098-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fa098-109">Requirements</span></span>



| <span data-ttu-id="fa098-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fa098-110">Requirement</span></span> | <span data-ttu-id="fa098-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa098-111">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="fa098-112">Version</span><span class="sxs-lookup"><span data-stu-id="fa098-112">Version</span></span><br/> | <span data-ttu-id="fa098-113">Lecteur Windows Media version 70 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="fa098-113">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fa098-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa098-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa098-115">**Gestionnaires d’événements ambiants**</span><span class="sxs-lookup"><span data-stu-id="fa098-115">**Ambient Event Handlers**</span></span>](ambient-event-handlers.md)
</dt> </dl>

 

 





