---
title: External. DownloadManager
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. La propriété DownloadManager récupère l’objet DownloadManager.
ms.assetid: 9fec7175-611e-4e7e-8978-132e6f86329a
keywords:
- External. DownloadManager Windows Media Player
topic_type:
- apiref
api_name:
- External.DownloadManager
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f55e6371f5c8d1e5dfcb17762340a82e8d921c17
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539698"
---
# <a name="externaldownloadmanager"></a><span data-ttu-id="44ec7-106">External. DownloadManager</span><span class="sxs-lookup"><span data-stu-id="44ec7-106">External.DownloadManager</span></span>

> [!Note]  
> <span data-ttu-id="44ec7-107">Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="44ec7-107">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="44ec7-108">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="44ec7-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="44ec7-109">La propriété **downloadmanager** récupère l’objet **downloadmanager** .</span><span class="sxs-lookup"><span data-stu-id="44ec7-109">The **DownloadManager** property retrieves the **DownloadManager** object.</span></span>

``` syntax
window.external.DownloadManager
      
```

## <a name="possible-values"></a><span data-ttu-id="44ec7-110">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="44ec7-110">Possible Values</span></span>

<span data-ttu-id="44ec7-111">Cette propriété est un objet **downloadmanager** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="44ec7-111">This property is a read-only **DownloadManager** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="44ec7-112">Notes</span><span class="sxs-lookup"><span data-stu-id="44ec7-112">Remarks</span></span>

<span data-ttu-id="44ec7-113">Dans le lecteur Windows Media 10 ou version ultérieure, la propriété et l’objet **downloadmanager** sont accessibles uniquement à partir des volets de tâches du service de magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="44ec7-113">In Windows Media Player 10 or later, the **DownloadManager** property and object are accessible only from online store service task panes.</span></span> <span data-ttu-id="44ec7-114">Vous ne pouvez pas utiliser **downloadmanager** à partir d’autres fonctionnalités où l’objet **externe** est disponible, par exemple HTMLView, le mode Info Center et les informations sur l’album.</span><span class="sxs-lookup"><span data-stu-id="44ec7-114">You cannot use the **DownloadManager** from other features where the **External** object is available, such as HTMLView, Info Center View, and album information.</span></span>

## <a name="requirements"></a><span data-ttu-id="44ec7-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="44ec7-115">Requirements</span></span>



| <span data-ttu-id="44ec7-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="44ec7-116">Requirement</span></span> | <span data-ttu-id="44ec7-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="44ec7-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="44ec7-118">Version</span><span class="sxs-lookup"><span data-stu-id="44ec7-118">Version</span></span><br/> | <span data-ttu-id="44ec7-119">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="44ec7-119">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="44ec7-120">DLL</span><span class="sxs-lookup"><span data-stu-id="44ec7-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="44ec7-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44ec7-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44ec7-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44ec7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44ec7-123">**Objet externe pour les magasins de type 2 en ligne**</span><span class="sxs-lookup"><span data-stu-id="44ec7-123">**External Object for Type 2 Online Stores**</span></span>](external-object-for-type-2-online-stores.md)
</dt> </dl>

 

 





