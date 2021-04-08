---
title: Utilisation de plusieurs handles de contexte par appel
description: La possibilité d’utiliser des tableaux de handles de contexte comme paramètres est rendue disponible dans Windows Vista et les systèmes d’exploitation ultérieurs.
ms.assetid: 84f3036b-ff4d-485d-bf23-ad10a03076a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b7b1c69dd182bee8f68e7068bcfcef60efd380a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840018"
---
# <a name="using-more-than-one-context-handle-per-call"></a><span data-ttu-id="3f8c5-103">Utilisation de plusieurs handles de contexte par appel</span><span class="sxs-lookup"><span data-stu-id="3f8c5-103">Using More than One Context Handle per Call</span></span>

<span data-ttu-id="3f8c5-104">La possibilité d’utiliser des tableaux de handles de contexte comme paramètres est rendue disponible dans Windows Vista et les systèmes d’exploitation ultérieurs.</span><span class="sxs-lookup"><span data-stu-id="3f8c5-104">The ability to use arrays of context handles as parameters is made available in Windows Vista and later operating systems.</span></span> <span data-ttu-id="3f8c5-105">Toutefois, cette fonctionnalité doit être utilisée avec soin dans une application.</span><span class="sxs-lookup"><span data-stu-id="3f8c5-105">However, this feature should be used carefully within an application.</span></span> <span data-ttu-id="3f8c5-106">Par exemple, dans une situation où un descripteur de contexte est utilisé dans plusieurs appels, il devient de plus en plus difficile d’assurer le suivi de son utilisation.</span><span class="sxs-lookup"><span data-stu-id="3f8c5-106">For example, in a situation where a context handle is being used in multiple calls it becomes increasingly difficult to keep track of its use.</span></span>

 

 




