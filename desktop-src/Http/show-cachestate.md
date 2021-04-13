---
title: show cachestate
description: Répertorie toutes les ressources et leurs propriétés associées qui sont mises en cache dans le cache de réponse HTTP ou affiche une ressource unique et ses propriétés associées.
ms.assetid: 9daa445e-dd2f-4b73-8938-58df931c015b
keywords:
- afficher le HTTP de cathorax
topic_type:
- apiref
api_name:
- show cachestate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 088a59eaa92db8ed9e8cbe59075d540507e51535
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2019
ms.locfileid: "104313315"
---
# <a name="show-cachestate"></a><span data-ttu-id="ee3c0-104">show cachestate</span><span class="sxs-lookup"><span data-stu-id="ee3c0-104">show cachestate</span></span>

<span data-ttu-id="ee3c0-105">Répertorie toutes les ressources et leurs propriétés associées qui sont mises en cache dans le cache de réponse HTTP ou affiche une ressource unique et ses propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="ee3c0-105">Lists all resources and their associated properties that are cached in the HTTP response cache or displays a single resource and its associated properties.</span></span>

``` syntax
show cachestate [[url=]string]
 
```

## <a name="parameters"></a><span data-ttu-id="ee3c0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ee3c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee3c0-107"><span id="__url__string_"></span><span id="__URL__STRING_"></span>**\[\[URL = \] ***chaîne***\]**</span><span class="sxs-lookup"><span data-stu-id="ee3c0-107"><span id="__url__string_"></span><span id="__URL__STRING_"></span>**\[\[url=\]***string***\]**</span></span>
</dt> <dd>

<span data-ttu-id="ee3c0-108">URL complète.</span><span class="sxs-lookup"><span data-stu-id="ee3c0-108">Fully qualified URL.</span></span> <span data-ttu-id="ee3c0-109">S’il n’est pas spécifié, implique toutes les URL.</span><span class="sxs-lookup"><span data-stu-id="ee3c0-109">If unspecified, implies all URLs.</span></span> <span data-ttu-id="ee3c0-110">L’URL peut également être un préfixe des URL inscrites.</span><span class="sxs-lookup"><span data-stu-id="ee3c0-110">The URL can also be a prefix to registered URLs.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="ee3c0-111">Exemples</span><span class="sxs-lookup"><span data-stu-id="ee3c0-111">Examples</span></span>

<span data-ttu-id="ee3c0-112">**afficher l’URL de cathorax =https://www.contoso.com:80/myresource**</span><span class="sxs-lookup"><span data-stu-id="ee3c0-112">**show cachestate url=https://www.contoso.com:80/myresource**</span></span>

 

 




