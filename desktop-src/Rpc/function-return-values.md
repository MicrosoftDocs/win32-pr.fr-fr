---
title: Valeurs de retour de fonction
description: Les valeurs de retour de fonction sont similaires aux paramètres \ out \ uniquement car leurs données ne sont pas fournies par l’application cliente.
ms.assetid: 98d8d228-7222-49bf-9f29-7749a7a76d5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08ada3808d024f201ef01a5f4977149a0ab9c75e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106509467"
---
# <a name="function-return-values"></a><span data-ttu-id="abc66-103">Valeurs de retour de fonction</span><span class="sxs-lookup"><span data-stu-id="abc66-103">Function Return Values</span></span>

<span data-ttu-id="abc66-104">Les valeurs de retour de fonction sont similaires aux paramètres de **\[ sortie \]** uniquement, car leurs données ne sont pas fournies par l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="abc66-104">Function return values are similar to **\[out\]**-only parameters because their data is not provided by the client application.</span></span> <span data-ttu-id="abc66-105">Toutefois, elles sont gérées différemment.</span><span class="sxs-lookup"><span data-stu-id="abc66-105">However they are managed differently.</span></span> <span data-ttu-id="abc66-106">Contrairement aux paramètres de **\[ sortie \]** seule, il n’est pas nécessaire qu’ils soient des pointeurs.</span><span class="sxs-lookup"><span data-stu-id="abc66-106">Unlike **\[out\]**-only parameters, they are not required to be pointers.</span></span> <span data-ttu-id="abc66-107">La procédure distante peut retourner n’importe quel type de données valide, à l’exception des pointeurs de référence et des unions non encapsulées.</span><span class="sxs-lookup"><span data-stu-id="abc66-107">The remote procedure can return any valid data type except reference pointers and nonencapsulated unions.</span></span>

<span data-ttu-id="abc66-108">Toutefois, il est recommandé d’utiliser un paramètre **\[ out \]** au lieu d’une valeur de retour pour les types de données complexes.</span><span class="sxs-lookup"><span data-stu-id="abc66-108">However, using an **\[out\]** parameter instead of a return value for complex data types is recommended.</span></span> <span data-ttu-id="abc66-109">Lors du retour de types de données complexes, le compilateur MIDL génère un stub en mode/OS.</span><span class="sxs-lookup"><span data-stu-id="abc66-109">While returning complex data types, the MIDL compiler will generate an /Os mode stub.</span></span> <span data-ttu-id="abc66-110">Par conséquent, toutes les informations récentes de vérification des erreurs fournies par/Robust sont perdues.</span><span class="sxs-lookup"><span data-stu-id="abc66-110">As a result, all recent error-checking information provided by /robust is lost.</span></span>

<span data-ttu-id="abc66-111">Les valeurs de retour de fonction qui sont des types pointeur sont allouées par le stub client avec un appel à [MIDL \_ User \_ allocate](/windows/desktop/Midl/midl-user-allocate-1).</span><span class="sxs-lookup"><span data-stu-id="abc66-111">Function return values that are pointer types are allocated by the client stub with a call to [midl\_user\_allocate](/windows/desktop/Midl/midl-user-allocate-1).</span></span> <span data-ttu-id="abc66-112">En conséquence, seul l’attribut de pointeur complet ou unique peut être appliqué à un type de retour de fonction de pointeur.</span><span class="sxs-lookup"><span data-stu-id="abc66-112">Accordingly, only the unique or full pointer attribute can be applied to a pointer function-return type.</span></span>

 

 