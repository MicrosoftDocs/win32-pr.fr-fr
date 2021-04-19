---
title: Combinaison d’attributs de tableau
description: Les attributs de champ peuvent être fournis dans différentes combinaisons tant que le stub peut utiliser les informations pour déterminer la taille du tableau et le nombre d’octets à transmettre au serveur.
ms.assetid: ff4f971f-9e46-4454-9d57-d8ebdf70b261
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffc60777caeb3950e37fe167fe09ecc181d88b8f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106513542"
---
# <a name="combining-array-attributes"></a><span data-ttu-id="0fd5e-103">Combinaison d’attributs de tableau</span><span class="sxs-lookup"><span data-stu-id="0fd5e-103">Combining Array Attributes</span></span>

<span data-ttu-id="0fd5e-104">Les attributs de champ peuvent être fournis dans différentes combinaisons tant que le stub peut utiliser les informations pour déterminer la taille du tableau et le nombre d’octets à transmettre au serveur.</span><span class="sxs-lookup"><span data-stu-id="0fd5e-104">Field attributes can be supplied in various combinations as long as the stub can use the information to determine the size of the array and the number of bytes to transmit to the server.</span></span> <span data-ttu-id="0fd5e-105">Les relations entre les attributs sont définies à l’aide des formules suivantes :</span><span class="sxs-lookup"><span data-stu-id="0fd5e-105">The relationships between the attributes are defined using the following formulas:</span></span>

``` syntax
size_is = max_is + 1;
length_is = last_is - first_is + 1;
```

<span data-ttu-id="0fd5e-106">Les valeurs associées aux attributs doivent respecter plusieurs règles de sens commun basées sur ces formules.</span><span class="sxs-lookup"><span data-stu-id="0fd5e-106">The values associated with the attributes must obey several common-sense rules based on those formulas.</span></span> <span data-ttu-id="0fd5e-107">Il s’agit des règles suivantes :</span><span class="sxs-lookup"><span data-stu-id="0fd5e-107">These rules are:</span></span>

-   <span data-ttu-id="0fd5e-108">Ne spécifiez pas un premier si la \[ valeur d’index [**\_ est**](/windows/desktop/Midl/first-is) \] inférieure à zéro ou si la \[ [**dernière \_**](/windows/desktop/Midl/last-is) \] valeur supérieure à \[ [**Max \_ est**](/windows/desktop/Midl/max-is) \] .</span><span class="sxs-lookup"><span data-stu-id="0fd5e-108">Do not specify a \[[**first\_is**](/windows/desktop/Midl/first-is)\] index value smaller than zero or a \[[**last\_is**](/windows/desktop/Midl/last-is)\] value greater than \[[**max\_is**](/windows/desktop/Midl/max-is)\].</span></span>
-   <span data-ttu-id="0fd5e-109">Ne spécifiez pas de taille négative pour un tableau.</span><span class="sxs-lookup"><span data-stu-id="0fd5e-109">Do not specify a negative size for an array.</span></span> <span data-ttu-id="0fd5e-110">Définissez le premier et le dernier élément afin qu’ils génèrent une valeur de longueur égale ou supérieure à zéro.</span><span class="sxs-lookup"><span data-stu-id="0fd5e-110">Define the first and last elements so that they result in a length value of zero or greater.</span></span> <span data-ttu-id="0fd5e-111">Définissez la \[ valeur [**Max \_ is**](/windows/desktop/Midl/max-is) \] pour que la taille soit égale à zéro ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="0fd5e-111">Define the \[[**max\_is**](/windows/desktop/Midl/max-is)\] value so that the size is zero or greater.</span></span> <span data-ttu-id="0fd5e-112">Si MIDL a été appelé avec l’option de vérification des limites [**/Error**](/windows/desktop/Midl/-error) \_ , le stub lève une exception lorsque la taille est inférieure à zéro, ou la longueur transmise est inférieure à zéro.</span><span class="sxs-lookup"><span data-stu-id="0fd5e-112">If MIDL was invoked with the [**/error**](/windows/desktop/Midl/-error) bounds\_check option, then the stub raises an exception when the size is less than zero, or the transmitted length is less than zero.</span></span>
-   <span data-ttu-id="0fd5e-113">N’utilisez pas la \[ [**longueur \_ :**](/windows/desktop/Midl/length-is) \] et le \[ [**dernier \_ est**](/windows/desktop/Midl/last-is) un \] attribut en même temps, ou la \[ **taille \_** est \] et le \[ **dernier attribut \_ est** \] en même temps.</span><span class="sxs-lookup"><span data-stu-id="0fd5e-113">Do not use the \[[**length\_is**](/windows/desktop/Midl/length-is)\] and \[[**last\_is**](/windows/desktop/Midl/last-is)\] attributes at the same time, nor the \[**size\_is**\] and \[**last\_is**\] attributes at the same time.</span></span>

<span data-ttu-id="0fd5e-114">En raison de la relation étroite en C entre les tableaux et les pointeurs, MIDL vous permet également de déclarer des tableaux dans des listes de paramètres à l’aide de la notation par pointeur.</span><span class="sxs-lookup"><span data-stu-id="0fd5e-114">Because of the close relationship in C between arrays and pointers, MIDL also lets you declare arrays in parameter lists using pointer notation.</span></span> <span data-ttu-id="0fd5e-115">MIDL traite un paramètre qui est un pointeur vers un type en tant que tableau de ce type si le paramètre possède l’un des attributs couramment associés aux tableaux.</span><span class="sxs-lookup"><span data-stu-id="0fd5e-115">MIDL treats a parameter that is a pointer to a type as an array of that type if the parameter has any of the attributes commonly associated with arrays.</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45)
  version(6.0) 
]
interface arraytest
{
  void fArray6([in] short sSize, 
               [in, out, size_is(sSize)] char * p1);
  void fArray7([in] short sSize, 
               [in, out, size_is(sSize)] char achArray[]);
}
```

<span data-ttu-id="0fd5e-116">Dans l’exemple précédent, les paramètres de tableau et de pointeur dans les fonctions fArray6 et fArray7 sont équivalents.</span><span class="sxs-lookup"><span data-stu-id="0fd5e-116">In the preceding example, the array and pointer parameters in the functions fArray6 and fArray7 are equivalent.</span></span>

 

 