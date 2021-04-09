---
title: Tableaux fixes
description: Si votre interface spécifie un tableau avec un nombre spécifique d’éléments en tant que paramètre, elle utilise un tableau fixe. Lors de l’utilisation de MIDL, vous définissez des tableaux fixes de la même façon que vous les définissez en C. Vous spécifiez le type, le nom et la taille du tableau.
ms.assetid: b9a2fa0b-1386-43e1-ab55-0a57cd8d1f18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bb3a620e86bff47e04afb5078dff50faee9fef0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673821"
---
# <a name="fixed-arrays"></a><span data-ttu-id="d50ad-104">Tableaux fixes</span><span class="sxs-lookup"><span data-stu-id="d50ad-104">Fixed Arrays</span></span>

<span data-ttu-id="d50ad-105">Si votre interface spécifie un tableau avec un nombre spécifique d’éléments en tant que paramètre, elle utilise un tableau fixe.</span><span class="sxs-lookup"><span data-stu-id="d50ad-105">If your interface specifies an array with a specific number of elements as a parameter, it is using a fixed array.</span></span> <span data-ttu-id="d50ad-106">Lors de l’utilisation de MIDL, vous définissez des tableaux fixes de la même façon que vous les définissez en C. Vous spécifiez le type, le nom et la taille du tableau.</span><span class="sxs-lookup"><span data-stu-id="d50ad-106">When using MIDL, you define fixed arrays in the same way you define them in C. You specify the array's type, name, and size.</span></span>

<span data-ttu-id="d50ad-107">L’exemple suivant montre comment définir un tableau fixe.</span><span class="sxs-lookup"><span data-stu-id="d50ad-107">The following example demonstrates how to define a fixed array.</span></span>

``` syntax
[
    /*Attributes are defined here. */
]
interface MyInterface
{
    const long ARRAY_SIZE = 1000;

    MyRemoteProc(char achArray[ARRAY_SIZE]);

    /* Other interface procedures are defined here. */
}
```

<span data-ttu-id="d50ad-108">Lorsqu’un programme client transmet un tableau fixe à un programme serveur, le stub client envoie l’intégralité du tableau au stub serveur.</span><span class="sxs-lookup"><span data-stu-id="d50ad-108">When a client program passes a fixed array to a server program, the client stub sends the entire array to the server stub.</span></span> <span data-ttu-id="d50ad-109">Le stub serveur alloue de la mémoire pour le tableau et stocke les données de tableau qu’il reçoit sur le réseau dans la mémoire allouée.</span><span class="sxs-lookup"><span data-stu-id="d50ad-109">The server stub allocates memory for the array and stores the array data it receives across the network into the allocated memory.</span></span> <span data-ttu-id="d50ad-110">Il passe ensuite le tableau à la procédure distante sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="d50ad-110">It then passes the array to the remote procedure on the server.</span></span> <span data-ttu-id="d50ad-111">Le serveur peut modifier les données dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="d50ad-111">The server may modify the data in the array.</span></span>

<span data-ttu-id="d50ad-112">Lorsque la procédure distante se termine, le stub serveur renvoie le contenu du tableau au client.</span><span class="sxs-lookup"><span data-stu-id="d50ad-112">When the remote procedure terminates, the server stub sends the contents of the array back to the client.</span></span> <span data-ttu-id="d50ad-113">Le stub client copie les données qu’il a reçues du stub serveur dans le tableau d’origine.</span><span class="sxs-lookup"><span data-stu-id="d50ad-113">The client stub copies the data it received from the server stub into the original array.</span></span> <span data-ttu-id="d50ad-114">Le programme client peut ensuite utiliser les données comme si elles avaient reçu les données d’un appel de procédure local.</span><span class="sxs-lookup"><span data-stu-id="d50ad-114">The client program can then use the data as it would if it received the data from a local procedure call.</span></span>

 

 




