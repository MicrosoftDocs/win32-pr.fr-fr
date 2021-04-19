---
title: show servicestate
description: Affiche un instantané du service HTTP.
ms.assetid: a50a3ef5-5e62-412e-a443-11d453778f70
keywords:
- afficher ServiceState HTTP
topic_type:
- apiref
api_name:
- show servicestate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f79bfdb946d286c31ce284efa09e75ad93c34438
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2019
ms.locfileid: "106517991"
---
# <a name="show-servicestate"></a><span data-ttu-id="bdb28-104">show servicestate</span><span class="sxs-lookup"><span data-stu-id="bdb28-104">show servicestate</span></span>

<span data-ttu-id="bdb28-105">Affiche un instantané du service HTTP.</span><span class="sxs-lookup"><span data-stu-id="bdb28-105">Shows a snapshot of the HTTP service.</span></span>

``` syntax
show servicestate [[view=]{session|requestq}] [[verbose=]{yes|no}]
 
```

## <a name="parameters"></a><span data-ttu-id="bdb28-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bdb28-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdb28-107"><span id="__view___session_requestq__"></span><span id="__VIEW___SESSION_REQUESTQ__"></span>**\[\[View = \] {session \| requestq}\]**</span><span class="sxs-lookup"><span data-stu-id="bdb28-107"><span id="__view___session_requestq__"></span><span id="__VIEW___SESSION_REQUESTQ__"></span>**\[\[view=\]{session\|requestq}\]**</span></span>
</dt> <dd>

<span data-ttu-id="bdb28-108">Affichez l’instantané de l’état du service HTTP en fonction de la session du serveur ou des files d’attente des demandes.</span><span class="sxs-lookup"><span data-stu-id="bdb28-108">View snapshot of HTTP service state based on server session or request queues.</span></span>

</dd> <dt>

<span data-ttu-id="bdb28-109"><span id="__verbose___yes_no__"></span><span id="__VERBOSE___YES_NO__"></span>**\[\[verbose = \] {Oui \| non}\]**</span><span class="sxs-lookup"><span data-stu-id="bdb28-109"><span id="__verbose___yes_no__"></span><span id="__VERBOSE___YES_NO__"></span>**\[\[verbose=\]{yes\|no}\]**</span></span>
</dt> <dd>

<span data-ttu-id="bdb28-110">Affichez les informations détaillées qui affichent également les informations de propriété.</span><span class="sxs-lookup"><span data-stu-id="bdb28-110">View verbose information showing property information too.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="bdb28-111">Exemples</span><span class="sxs-lookup"><span data-stu-id="bdb28-111">Examples</span></span>

<span data-ttu-id="bdb28-112">**afficher la vue ServiceState = session**</span><span class="sxs-lookup"><span data-stu-id="bdb28-112">**show servicestate view=session**</span></span>

<span data-ttu-id="bdb28-113">**afficher ServiceState affichage = requestq détaillé = Oui**</span><span class="sxs-lookup"><span data-stu-id="bdb28-113">**show servicestate view=requestq verbose=yes**</span></span>

 

 




