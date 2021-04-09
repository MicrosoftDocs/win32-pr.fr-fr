---
title: Gestion des erreurs inconnues
description: Gestion des erreurs inconnues
ms.assetid: d6a4cc60-8320-4b67-9f2e-7c4bea6c37fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8c3d9e70b89a9a78be62d2940ad8a69ac34c8f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029773"
---
# <a name="handling-unknown-errors"></a><span data-ttu-id="60925-103">Gestion des erreurs inconnues</span><span class="sxs-lookup"><span data-stu-id="60925-103">Handling Unknown Errors</span></span>

<span data-ttu-id="60925-104">Il est légal de retourner un code d’état uniquement à partir de l’implémentation d’une méthode d’interface approuvée comme légitimement retournée.</span><span class="sxs-lookup"><span data-stu-id="60925-104">It is legal to return a status code only from the implementation of an interface method sanctioned as legally returnable.</span></span> <span data-ttu-id="60925-105">Si vous ne respectez pas cette règle, l’éventualité d’un conflit entre les valeurs de code d’erreur renvoyées et celles approuvées par l’application est incompatible.</span><span class="sxs-lookup"><span data-stu-id="60925-105">Failure to observe this rule invites the possibility of conflict between returned error-code values and those sanctioned by the application.</span></span> <span data-ttu-id="60925-106">Portez une attention particulière à ce problème potentiel lors de la propagation des codes d’erreur à partir de fonctions appelées en interne.</span><span class="sxs-lookup"><span data-stu-id="60925-106">Pay particular attention to this potential problem when propagating error codes from functions that are called internally.</span></span>

<span data-ttu-id="60925-107">Les applications qui appellent des interfaces doivent traiter tout code d’erreur retourné inconnu (par opposition à un code de réussite) comme synonyme de E \_ inattendue.</span><span class="sxs-lookup"><span data-stu-id="60925-107">Applications that call interfaces should treat any unknown returned error code (as opposed to a success code) as synonymous with E\_UNEXPECTED.</span></span> <span data-ttu-id="60925-108">Cette pratique de gestion des codes d’erreur inconnus est requise par les clients des interfaces et fonctions définies par COM.</span><span class="sxs-lookup"><span data-stu-id="60925-108">This practice of handling unknown error codes is required by clients of the COM-defined interfaces and functions.</span></span> <span data-ttu-id="60925-109">Étant donné que la pratique de programmation consiste à gérer quelques codes d’erreur spécifiques en détail et à traiter le reste de façon générique, cette exigence de gestion des codes d’erreur inattendus ou inconnus est facilement respectée.</span><span class="sxs-lookup"><span data-stu-id="60925-109">Because typical programming practice is to handle a few specific error codes in detail and treat the rest generically, this requirement of handling unexpected or unknown error codes is easily met.</span></span>

<span data-ttu-id="60925-110">Il est important de gérer toutes les erreurs possibles lors de l’appel d’une méthode d’interface.</span><span class="sxs-lookup"><span data-stu-id="60925-110">It is important to handle all possible errors when calling an interface method.</span></span> <span data-ttu-id="60925-111">Si vous ne le faites pas, votre application risque de se bloquer, de corrompre les données ou de devenir vulnérable aux attaques de sécurité.</span><span class="sxs-lookup"><span data-stu-id="60925-111">Failure to do so could cause your application to crash, to corrupt data, or to become vulnerable to security exploits.</span></span> <span data-ttu-id="60925-112">L’exemple de code suivant montre la méthode recommandée pour gérer les erreurs inconnues :</span><span class="sxs-lookup"><span data-stu-id="60925-112">The following code sample shows the recommended way of handling unknown errors:</span></span>


```C++
HRESULT hr; 
hr = xxMethod(); 
 
switch (GetScode(hr))  
{ 
    case NOERROR: 
      // Method returned success. 
      break; 
 
    case x1: 
      // Handle error x1 here.
      break; 
 
    case x2: 
      // Handle error x2 here.
      break; 
 
    case E_UNEXPECTED: 
    default: 
      // Handle unexpected errors here. 
      break; 
} 
 
```



<span data-ttu-id="60925-113">La vérification des erreurs suivante est souvent utilisée avec les routines qui ne retournent pas d’éléments spéciaux (autres que S \_ OK ou une erreur inattendue) :</span><span class="sxs-lookup"><span data-stu-id="60925-113">The following error check is often used with those routines that do not return anything special (other than S\_OK or some unexpected error):</span></span>


```C++
if (xxMethod() == NOERROR) 
{
    // Handle success here.
} 
else 
{
    // Handle failure here.
} 
```



## <a name="related-topics"></a><span data-ttu-id="60925-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="60925-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60925-115">Gestion des erreurs dans COM</span><span class="sxs-lookup"><span data-stu-id="60925-115">Error Handling in COM</span></span>](error-handling-in-com.md)
</dt> </dl>

 

 




