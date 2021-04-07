---
description: Le modèle CMSPArray implémente un tableau intelligent qui s’agrandit à la demande.
ms.assetid: 9b30885c-01a4-4aea-a1c3-5d7966e4697f
title: CMSPArray
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a6c14d4bdc0b57a295efa5bcc2adfd79d23d31d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952097"
---
# <a name="cmsparray"></a><span data-ttu-id="2bd64-103">CMSPArray</span><span class="sxs-lookup"><span data-stu-id="2bd64-103">CMSPArray</span></span>

<span data-ttu-id="2bd64-104">Le modèle CMSPArray implémente un tableau intelligent qui s’agrandit à la demande.</span><span class="sxs-lookup"><span data-stu-id="2bd64-104">The CMSPArray template implements a smart array that will grow on demand.</span></span> <span data-ttu-id="2bd64-105">Il est conçu pour contenir des tableaux de petite taille avec des types de données simples.</span><span class="sxs-lookup"><span data-stu-id="2bd64-105">It is designed to hold small arrays with simple data types.</span></span> <span data-ttu-id="2bd64-106">Elle n’a pas de section critique.</span><span class="sxs-lookup"><span data-stu-id="2bd64-106">It doesn't have a critical section.</span></span> <span data-ttu-id="2bd64-107">Ses seules dépendances sont **realloc** et **memmove**.</span><span class="sxs-lookup"><span data-stu-id="2bd64-107">Its only dependencies are **realloc** and **memmove**.</span></span> <span data-ttu-id="2bd64-108">Il est utilisé en interne pour conserver les listes de pointeurs d’objets.</span><span class="sxs-lookup"><span data-stu-id="2bd64-108">It is used internally to keep lists of object pointers.</span></span> <span data-ttu-id="2bd64-109">Elle est similaire à l’implémentation **CSimpleArray** d’ATL, mais elle est plus efficace pour les allocations initiales.</span><span class="sxs-lookup"><span data-stu-id="2bd64-109">It is similar to ATL's **CSimpleArray** implementation, but it is more efficient for initial allocations.</span></span>

<span data-ttu-id="2bd64-110">Ce modèle est défini dans MSPutils. h.</span><span class="sxs-lookup"><span data-stu-id="2bd64-110">This template is defined in MSPutils.h.</span></span>

 

 



