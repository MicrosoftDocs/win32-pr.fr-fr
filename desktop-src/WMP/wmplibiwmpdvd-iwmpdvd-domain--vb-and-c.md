---
title: Propriété de domaine IWMPDVD
description: La propriété de domaine obtient le domaine actuel du DVD.
ms.assetid: 0b7b39fe-2b04-44e2-aa5e-cab7be9a06b1
keywords:
- propriété de domaine lecteur Windows Media
- propriété de domaine lecteur Windows Media, interface IWMPDVD
- Interface IWMPDVD lecteur Windows Media, propriété de domaine
topic_type:
- apiref
api_name:
- IWMPDVD.domain
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6546a8288160fe80f7df4a7c41ea79a0edc905f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531099"
---
# <a name="iwmpdvddomain-property"></a><span data-ttu-id="2ce45-106">IWMPDVD ::d propriété omaine</span><span class="sxs-lookup"><span data-stu-id="2ce45-106">IWMPDVD::domain property</span></span>

<span data-ttu-id="2ce45-107">La propriété de **domaine** obtient le domaine actuel du DVD.</span><span class="sxs-lookup"><span data-stu-id="2ce45-107">The **domain** property gets the current domain of the DVD.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ce45-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2ce45-108">Syntax</span></span>


```CSharp
public System.String domain {get; set;}
```


```VB

Public ReadOnly Property domain As System.String
```





## <a name="property-value"></a><span data-ttu-id="2ce45-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="2ce45-109">Property value</span></span>

<span data-ttu-id="2ce45-110">**System. String** qui est l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="2ce45-110">A **System.String** that is one of the following values.</span></span>



| <span data-ttu-id="2ce45-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="2ce45-111">Value</span></span>                                                                                        | <span data-ttu-id="2ce45-112">Signification</span><span class="sxs-lookup"><span data-stu-id="2ce45-112">Meaning</span></span>                                                                                                                                          |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2ce45-113"><dt>firstPlay</dt></span><span class="sxs-lookup"><span data-stu-id="2ce45-113"><dt>firstPlay</dt></span></span> </dl>         | <span data-ttu-id="2ce45-114">Exécution de l’initialisation par défaut d’un disque DVD.</span><span class="sxs-lookup"><span data-stu-id="2ce45-114">Performing default initialization of a DVD disc.</span></span><br/>                                                                                      |
| <dl> <span data-ttu-id="2ce45-115"><dt>videoManagerMenu</dt></span><span class="sxs-lookup"><span data-stu-id="2ce45-115"><dt>videoManagerMenu</dt></span></span> </dl>  | <span data-ttu-id="2ce45-116">Affichage des menus pour l’ensemble du disque. Également appelé « menu » pour le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="2ce45-116">Displaying menus for the entire disc. Also known as topMenu for Windows Media Player.</span></span> <span data-ttu-id="2ce45-117">Communément appelé le menu du titre ou le menu supérieur.</span><span class="sxs-lookup"><span data-stu-id="2ce45-117">Commonly called the title menu or the top menu.</span></span><br/> |
| <dl> <span data-ttu-id="2ce45-118"><dt>videoTitleSetMenu</dt></span><span class="sxs-lookup"><span data-stu-id="2ce45-118"><dt>videoTitleSetMenu</dt></span></span> </dl> | <span data-ttu-id="2ce45-119">Affichage des menus pour l’ensemble de titres actuel.</span><span class="sxs-lookup"><span data-stu-id="2ce45-119">Displaying menus for the current title set.</span></span> <span data-ttu-id="2ce45-120">Également appelé titleMenu pour Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="2ce45-120">Also known as titleMenu for Windows Media Player.</span></span> <span data-ttu-id="2ce45-121">Communément appelé menu racine.</span><span class="sxs-lookup"><span data-stu-id="2ce45-121">Commonly called the root menu.</span></span><br/>          |
| <dl> <span data-ttu-id="2ce45-122"><dt>title</dt></span><span class="sxs-lookup"><span data-stu-id="2ce45-122"><dt>title</dt></span></span> </dl>             | <span data-ttu-id="2ce45-123">En général, affichage du titre actuel.</span><span class="sxs-lookup"><span data-stu-id="2ce45-123">Usually, displaying the current title.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="2ce45-124"><dt>stop</dt></span><span class="sxs-lookup"><span data-stu-id="2ce45-124"><dt>stop</dt></span></span> </dl>              | <span data-ttu-id="2ce45-125">Le navigateur DVD se trouve dans le domaine d’arrêt du DVD.</span><span class="sxs-lookup"><span data-stu-id="2ce45-125">The DVD Navigator is in the DVD Stop domain.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="2ce45-126"><dt>non défini</dt></span><span class="sxs-lookup"><span data-stu-id="2ce45-126"><dt>undefined</dt></span></span> </dl>         | <span data-ttu-id="2ce45-127">Le lecteur Windows Media n’est pas dans un domaine DVD.</span><span class="sxs-lookup"><span data-stu-id="2ce45-127">Windows Media Player is not in any DVD domain.</span></span><br/>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="2ce45-128">Notes</span><span class="sxs-lookup"><span data-stu-id="2ce45-128">Remarks</span></span>

<span data-ttu-id="2ce45-129">Chaque DVD est créé différemment.</span><span class="sxs-lookup"><span data-stu-id="2ce45-129">Every DVD is authored differently.</span></span> <span data-ttu-id="2ce45-130">Certains DVD ne contiennent pas les domaines firstPlay, videoManagerMenu ou videoTitleSetMenu.</span><span class="sxs-lookup"><span data-stu-id="2ce45-130">Some DVDs do not contain the firstPlay, videoManagerMenu, or videoTitleSetMenu domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ce45-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2ce45-131">Requirements</span></span>



| <span data-ttu-id="2ce45-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2ce45-132">Requirement</span></span> | <span data-ttu-id="2ce45-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="2ce45-133">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ce45-134">Version</span><span class="sxs-lookup"><span data-stu-id="2ce45-134">Version</span></span><br/>   | <span data-ttu-id="2ce45-135">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="2ce45-135">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="2ce45-136">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2ce45-136">Namespace</span></span><br/> | <span data-ttu-id="2ce45-137">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="2ce45-137">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="2ce45-138">Assembly</span><span class="sxs-lookup"><span data-stu-id="2ce45-138">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2ce45-139"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2ce45-139"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ce45-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ce45-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ce45-141">**Interface IWMPDVD (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="2ce45-141">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





