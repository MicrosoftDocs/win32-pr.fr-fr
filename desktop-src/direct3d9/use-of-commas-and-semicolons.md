---
description: L’utilisation de virgules et de points-virgules peut être le problème de syntaxe le plus complexe dans le format de fichier, et cette utilisation est très stricte. Les virgules sont utilisées pour séparer les membres de tableau ; les points-virgules mettent fin à chaque élément de données.
ms.assetid: 82582213-907c-4760-a849-e6cf5f6d60bc
title: Utilisation de virgules et de points-virgules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ba238d50ff5d0dace017f16b75547df6b016e14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109882"
---
# <a name="use-of-commas-and-semicolons"></a><span data-ttu-id="97d77-104">Utilisation de virgules et de points-virgules</span><span class="sxs-lookup"><span data-stu-id="97d77-104">Use of Commas and Semicolons</span></span>

<span data-ttu-id="97d77-105">L’utilisation de virgules et de points-virgules peut être le problème de syntaxe le plus complexe dans le format de fichier, et cette utilisation est très stricte.</span><span class="sxs-lookup"><span data-stu-id="97d77-105">Using commas and semicolons can be the most complex syntax issue in the file format, and this usage is very strict.</span></span> <span data-ttu-id="97d77-106">Les virgules sont utilisées pour séparer les membres de tableau ; les points-virgules mettent fin à chaque élément de données.</span><span class="sxs-lookup"><span data-stu-id="97d77-106">Commas are used to separate array members; semicolons terminate each data item.</span></span>

<span data-ttu-id="97d77-107">Par exemple, si un modèle est défini de la manière suivante :</span><span class="sxs-lookup"><span data-stu-id="97d77-107">For example, if a template is defined in the following manner:</span></span>


```
template mytemp {
DWORD myvar;
}
```



<span data-ttu-id="97d77-108">Une instance de ce modèle ressemble alors à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="97d77-108">Then an instance of this template looks like the following:</span></span>


```
mytemp dataTemp {
1;
}
```



<span data-ttu-id="97d77-109">Si un modèle contenant un autre modèle est défini de la manière suivante :</span><span class="sxs-lookup"><span data-stu-id="97d77-109">If a template containing another template is defined in the following manner;</span></span>


```
template mytemp {
DWORD myvar;
DWORD myvar2;
}
template container {
FLOAT aFloat;
mytemp aTemp;
}
```



<span data-ttu-id="97d77-110">Une instance de ce modèle ressemble alors à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="97d77-110">Then an instance of this template looks like the following:</span></span>


```
container dataContainer {
1.1;
2; 
3;;
}
```



<span data-ttu-id="97d77-111">Notez que la deuxième ligne qui représente le mytemp à l’intérieur d’un conteneur a deux points-virgules à la fin de la ligne.</span><span class="sxs-lookup"><span data-stu-id="97d77-111">Note that the second line that represents the mytemp inside container has two semicolons at the end of the line.</span></span> <span data-ttu-id="97d77-112">Le premier point-virgule indique la fin de l’élément de données, aTemp (dans le conteneur) et le deuxième point-virgule indique la fin du conteneur.</span><span class="sxs-lookup"><span data-stu-id="97d77-112">The first semicolon indicates the end of the data item, aTemp (inside container), and the second semicolon indicates the end of the container.</span></span>

<span data-ttu-id="97d77-113">Si un tableau est défini de la manière suivante :</span><span class="sxs-lookup"><span data-stu-id="97d77-113">If an array is defined in the following manner:</span></span>


```
Template mytemp {

array DWORD myvar[3];

}
```



<span data-ttu-id="97d77-114">Une instance de cet exemple se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="97d77-114">Then an instance of this looks like the following:</span></span>


```
mytemp aTemp {
1, 2, 3;
}
```



<span data-ttu-id="97d77-115">Dans l’exemple de tableau, il n’est pas nécessaire que les éléments de données soient séparés par des points-virgules, car ils sont délimités par des virgules.</span><span class="sxs-lookup"><span data-stu-id="97d77-115">In the array example, there is no need for the data items to be separated by semicolons because they are delineated by commas.</span></span> <span data-ttu-id="97d77-116">Le point-virgule à la fin marque la fin du tableau.</span><span class="sxs-lookup"><span data-stu-id="97d77-116">The semicolon at the end marks the end of the array.</span></span>

<span data-ttu-id="97d77-117">Prenons l’exemple d’un modèle qui contient un tableau d’éléments de données définis par un modèle.</span><span class="sxs-lookup"><span data-stu-id="97d77-117">Consider a template that contains an array of data items defined by a template.</span></span>


```
template mytemp {
DWORD myvar;
DWORD myvar2;
}
template container {
DWORD count;
array mytemp tempArray[count];
}
```



<span data-ttu-id="97d77-118">Une instance de cela ressemble à l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="97d77-118">An instance of this would look like the following example.</span></span>


```
container aContainer {
3;
1;2;,3;4;,5;6;;
}
```



## <a name="related-topics"></a><span data-ttu-id="97d77-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="97d77-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97d77-120">Encodage de texte</span><span class="sxs-lookup"><span data-stu-id="97d77-120">Text Encoding</span></span>](text-encoding.md)
</dt> </dl>

 

 



