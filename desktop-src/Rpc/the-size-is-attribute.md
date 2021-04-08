---
title: Attribut size_is
description: L’attribut \ size \_ is \ est associé à une constante entière, une expression ou une variable qui spécifie la taille d’allocation du tableau.
ms.assetid: 5252c1a2-8e07-4e28-8280-6a9563d1b291
keywords:
- size_is
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7159c68d6bc3c1485c14db20d97c488916cb7b22
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842401"
---
# <a name="the-size_is-attribute"></a><span data-ttu-id="50444-104">La \[ taille \_ est un \] attribut</span><span class="sxs-lookup"><span data-stu-id="50444-104">The \[size\_is\] Attribute</span></span>

<span data-ttu-id="50444-105">La \[ [taille \_ est](/windows/desktop/Midl/size-is) \] un attribut associé à une constante entière, une expression ou une variable qui spécifie la taille d’allocation du tableau.</span><span class="sxs-lookup"><span data-stu-id="50444-105">The \[ [size\_is](/windows/desktop/Midl/size-is)\] attribute is associated with an integer constant, expression, or variable that specifies the allocation size of the array.</span></span> <span data-ttu-id="50444-106">Prenons l’exemple d’un tableau de caractères dont la longueur est déterminée par l’entrée utilisateur :</span><span class="sxs-lookup"><span data-stu-id="50444-106">Consider a character array whose length is determined by user input:</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(2.0)
]
interface arraytest
{
  void fArray2([in] short sSize,
               [in, out, size_is(sSize)] char achArray[*]);
}
```

> [!Note]  
> <span data-ttu-id="50444-107">L’astérisque ( \* ) qui marque l’espace réservé pour la dimension variable-tableau est facultatif.</span><span class="sxs-lookup"><span data-stu-id="50444-107">The asterisk (\*) that marks the placeholder for the variable-array dimension is optional.</span></span>

 

<span data-ttu-id="50444-108">Le stub serveur doit allouer de la mémoire sur le serveur qui correspond à la mémoire sur le client pour ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="50444-108">The server stub must allocate memory on the server that corresponds to the memory on the client for that parameter.</span></span> <span data-ttu-id="50444-109">La variable qui spécifie la taille doit toujours être au moins un \[ [](/windows/desktop/Midl/in) \] paramètre in.</span><span class="sxs-lookup"><span data-stu-id="50444-109">The variable that specifies the size must always be at least an \[ [in](/windows/desktop/Midl/in)\] parameter.</span></span> <span data-ttu-id="50444-110">L' **attribut directionnel est requis pour que la valeur taille soit définie à l’entrée sur le stub serveur. \[ \]**</span><span class="sxs-lookup"><span data-stu-id="50444-110">The **\[in\]** directional attribute is required so that the size value is defined on entry to the server stub.</span></span> <span data-ttu-id="50444-111">Cette valeur de taille fournit les informations dont le stub serveur a besoin pour allouer la mémoire.</span><span class="sxs-lookup"><span data-stu-id="50444-111">This size value provides information that the server stub requires to allocate the memory.</span></span>

<span data-ttu-id="50444-112">Le paramètre de taille peut également être \[ in, [out](/windows/desktop/Midl/out-idl) \] .</span><span class="sxs-lookup"><span data-stu-id="50444-112">The size parameter can also be \[in, [out](/windows/desktop/Midl/out-idl)\].</span></span> <span data-ttu-id="50444-113">Cela est utile si, par exemple, le tableau envoyé par le client n’est pas suffisamment grand pour les données que le serveur doit stocker dans celui-ci.</span><span class="sxs-lookup"><span data-stu-id="50444-113">This is useful if, for instance, the array the client sends is not large enough for the data that the server needs to store in it.</span></span> <span data-ttu-id="50444-114">Vous pouvez utiliser un paramètre **\[ in, \] out** size pour renvoyer la taille requise au programme client.</span><span class="sxs-lookup"><span data-stu-id="50444-114">You can use an **\[in, out\]** size parameter to send the required size back to the client program.</span></span>

## <a name="related-topics"></a><span data-ttu-id="50444-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="50444-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50444-116">Plusieurs niveaux de pointeurs</span><span class="sxs-lookup"><span data-stu-id="50444-116">Multiple Levels of Pointers</span></span>](multiple-levels-of-pointers.md)
</dt> </dl>

 

 