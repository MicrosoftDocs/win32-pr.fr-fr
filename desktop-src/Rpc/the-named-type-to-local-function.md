---
title: Fonction named_type_to_local
description: Les stubs appellent le \_ type nommé \_ à la \_ fonction locale pour convertir les données d’un type transmis vers le type qu’ils présentent à l’application.
ms.assetid: c272cc1f-e47b-4d5a-a4e2-cefeaeb8c175
keywords:
- named_type_to_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 746cbdd01ea657408b1bf355f41b3b9dfba673a9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029209"
---
# <a name="the-named_type_to_local-function"></a><span data-ttu-id="2bf3e-104">Le \_ type nommé \_ vers la \_ fonction locale</span><span class="sxs-lookup"><span data-stu-id="2bf3e-104">The named\_type\_to\_local Function</span></span>

<span data-ttu-id="2bf3e-105">Les stubs appellent **le \_ type nommé \_ à \_** la fonction locale pour convertir les données d’un type transmis vers le type qu’ils présentent à l’application.</span><span class="sxs-lookup"><span data-stu-id="2bf3e-105">The stubs call the **named\_type\_to\_local** function to convert data from a transmitted type to the type that they present to the application.</span></span> <span data-ttu-id="2bf3e-106">La fonction est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="2bf3e-106">The function is defined as:</span></span>

``` syntax
void __RPC_USER <named_type>_to_local( 
    <named_type> __RPC_FAR * _RPC_FAR * , 
    <local_type> __RPC_FAR * );
```

<span data-ttu-id="2bf3e-107">Le premier paramètre pointe vers les données transmises.</span><span class="sxs-lookup"><span data-stu-id="2bf3e-107">The first parameter points to the transmitted data.</span></span> <span data-ttu-id="2bf3e-108">La fonction définit le deuxième paramètre pour qu’il pointe vers les données présentées.</span><span class="sxs-lookup"><span data-stu-id="2bf3e-108">The function sets the second parameter to point to the presented data.</span></span>

<span data-ttu-id="2bf3e-109">Le **\_ type nommé \_ à \_** la fonction locale doit gérer la mémoire pour le type présenté.</span><span class="sxs-lookup"><span data-stu-id="2bf3e-109">The **named\_type\_to\_local** function must manage memory for the presented type.</span></span> <span data-ttu-id="2bf3e-110">La fonction doit allouer de la mémoire pour l’ensemble de la structure de données qui commence à l’adresse indiquée par le deuxième paramètre, à l’exception du paramètre lui-même (le stub alloue de la mémoire pour le nœud racine et le transmet à la fonction).</span><span class="sxs-lookup"><span data-stu-id="2bf3e-110">The function must allocate memory for the entire data structure that starts at the address indicated by the second parameter, except for the parameter itself (the stub allocates memory for the root node and passes it to the function).</span></span> <span data-ttu-id="2bf3e-111">La valeur du deuxième paramètre ne peut pas changer pendant l’appel.</span><span class="sxs-lookup"><span data-stu-id="2bf3e-111">The value of the second parameter cannot change during the call.</span></span> <span data-ttu-id="2bf3e-112">La fonction peut modifier le contenu à cette adresse.</span><span class="sxs-lookup"><span data-stu-id="2bf3e-112">The function can change the contents at that address.</span></span>

 

 




