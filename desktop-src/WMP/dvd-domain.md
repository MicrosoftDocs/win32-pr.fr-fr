---
title: DVD. domaine
description: La propriété de domaine récupère le domaine actuel du DVD.
ms.assetid: 74f4a6a3-8518-48c7-b023-f0255a3a62fd
keywords:
- DVD. domaine lecteur Windows Media
topic_type:
- apiref
api_name:
- DVD.domain
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db4a2af92abe533fed7a13e48cb7c0724223bbc1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317214"
---
# <a name="dvddomain"></a><span data-ttu-id="69e13-104">DVD. domaine</span><span class="sxs-lookup"><span data-stu-id="69e13-104">DVD.domain</span></span>

<span data-ttu-id="69e13-105">La propriété de **domaine** récupère le domaine actuel du DVD.</span><span class="sxs-lookup"><span data-stu-id="69e13-105">The **domain** property retrieves the current domain of the DVD.</span></span>

``` syntax
player.dvd.domain
      
```

## <a name="possible-values"></a><span data-ttu-id="69e13-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="69e13-106">Possible Values</span></span>

<span data-ttu-id="69e13-107">Cette propriété est une **chaîne** en lecture seule qui contient l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="69e13-107">This property is a read-only **String** containing one of the following values.</span></span>



| <span data-ttu-id="69e13-108">String</span><span class="sxs-lookup"><span data-stu-id="69e13-108">String</span></span>            | <span data-ttu-id="69e13-109">Description</span><span class="sxs-lookup"><span data-stu-id="69e13-109">Description</span></span>                                                                                                                           |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69e13-110">firstPlay</span><span class="sxs-lookup"><span data-stu-id="69e13-110">firstPlay</span></span>         | <span data-ttu-id="69e13-111">Exécution de l’initialisation par défaut d’un disque DVD.</span><span class="sxs-lookup"><span data-stu-id="69e13-111">Performing default initialization of a DVD disc.</span></span>                                                                                      |
| <span data-ttu-id="69e13-112">videoManagerMenu</span><span class="sxs-lookup"><span data-stu-id="69e13-112">videoManagerMenu</span></span>  | <span data-ttu-id="69e13-113">Affichage des menus pour l’ensemble du disque. Également appelé « menu » pour le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="69e13-113">Displaying menus for the entire disc. Also known as topMenu for Windows Media Player.</span></span> <span data-ttu-id="69e13-114">Communément appelé le menu du titre ou le menu supérieur.</span><span class="sxs-lookup"><span data-stu-id="69e13-114">Commonly called the title menu or the top menu.</span></span> |
| <span data-ttu-id="69e13-115">videoTitleSetMenu</span><span class="sxs-lookup"><span data-stu-id="69e13-115">videoTitleSetMenu</span></span> | <span data-ttu-id="69e13-116">Affichage des menus pour le jeu de titres actuel.</span><span class="sxs-lookup"><span data-stu-id="69e13-116">Displaying menus for current title set.</span></span> <span data-ttu-id="69e13-117">Également appelé titleMenu pour Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="69e13-117">Also known as titleMenu for Windows Media Player.</span></span> <span data-ttu-id="69e13-118">Communément appelé menu racine.</span><span class="sxs-lookup"><span data-stu-id="69e13-118">Commonly called the root menu.</span></span>              |
| <span data-ttu-id="69e13-119">title</span><span class="sxs-lookup"><span data-stu-id="69e13-119">title</span></span>             | <span data-ttu-id="69e13-120">Affiche généralement le titre actuel.</span><span class="sxs-lookup"><span data-stu-id="69e13-120">Usually displaying the current title.</span></span>                                                                                                 |
| <span data-ttu-id="69e13-121">stop</span><span class="sxs-lookup"><span data-stu-id="69e13-121">stop</span></span>              | <span data-ttu-id="69e13-122">Le navigateur DVD se trouve dans le domaine d’arrêt du DVD.</span><span class="sxs-lookup"><span data-stu-id="69e13-122">The DVD Navigator is in the DVD Stop domain.</span></span>                                                                                          |
| <span data-ttu-id="69e13-123">non défini</span><span class="sxs-lookup"><span data-stu-id="69e13-123">undefined</span></span>         | <span data-ttu-id="69e13-124">Le lecteur n’est pas dans un domaine DVD.</span><span class="sxs-lookup"><span data-stu-id="69e13-124">Player is not in any DVD domain.</span></span>                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="69e13-125">Notes</span><span class="sxs-lookup"><span data-stu-id="69e13-125">Remarks</span></span>

<span data-ttu-id="69e13-126">Chaque DVD est créé différemment.</span><span class="sxs-lookup"><span data-stu-id="69e13-126">Every DVD is authored differently.</span></span> <span data-ttu-id="69e13-127">Certains DVD ne contiennent pas les domaines firstPlay, videoManagerMenu ou videoTitleSetMenu.</span><span class="sxs-lookup"><span data-stu-id="69e13-127">Some DVDs do not contain the firstPlay, videoManagerMenu, or videoTitleSetMenu domains.</span></span>

<span data-ttu-id="69e13-128">**Lecteur Windows Media 10 Mobile :** Cette propriété retourne toujours une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="69e13-128">**Windows Media Player 10 Mobile:** This property always returns an empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="69e13-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="69e13-129">Requirements</span></span>



| <span data-ttu-id="69e13-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="69e13-130">Requirement</span></span> | <span data-ttu-id="69e13-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="69e13-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="69e13-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69e13-132">Minimum supported client</span></span><br/> | <span data-ttu-id="69e13-133">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="69e13-133">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="69e13-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69e13-134">Minimum supported server</span></span><br/> | <span data-ttu-id="69e13-135">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="69e13-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="69e13-136">Version</span><span class="sxs-lookup"><span data-stu-id="69e13-136">Version</span></span><br/>                  | <span data-ttu-id="69e13-137">Lecteur Windows Media pour Windows XP ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="69e13-137">Windows Media Player for Windows XP or later</span></span><br/>                            |
| <span data-ttu-id="69e13-138">DLL</span><span class="sxs-lookup"><span data-stu-id="69e13-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69e13-139"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69e13-139"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69e13-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69e13-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69e13-141">**Objet DVD**</span><span class="sxs-lookup"><span data-stu-id="69e13-141">**DVD Object**</span></span>](dvd-object.md)
</dt> </dl>

 

 





