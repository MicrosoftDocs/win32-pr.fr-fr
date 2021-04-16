---
description: Les objets de données contiennent les données réelles ou une référence à ces données. Chaque objet de données a un modèle correspondant qui spécifie le type de données. Les sections suivantes décrivent le formulaire et les parties des objets de données.
ms.assetid: 61dbe241-2658-4dd0-af89-3db204b56fad
title: Données (format de fichier X, encodage de texte)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1af117a0207ce804ccacd397bb990fe5f43c94
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392699"
---
# <a name="data-x-file-format-text-encoding"></a><span data-ttu-id="4681c-105">Données (format de fichier X, encodage de texte)</span><span class="sxs-lookup"><span data-stu-id="4681c-105">Data (X file format, text encoding)</span></span>

<span data-ttu-id="4681c-106">Les objets de données contiennent les données réelles ou une référence à ces données.</span><span class="sxs-lookup"><span data-stu-id="4681c-106">Data objects contain the actual data or a reference to that data.</span></span> <span data-ttu-id="4681c-107">Chaque objet de données a un modèle correspondant qui spécifie le type de données.</span><span class="sxs-lookup"><span data-stu-id="4681c-107">Each data object has a corresponding template that specifies the data type.</span></span> <span data-ttu-id="4681c-108">Les sections suivantes décrivent le formulaire et les parties des objets de données.</span><span class="sxs-lookup"><span data-stu-id="4681c-108">The following sections discuss the form and parts of data objects.</span></span>

## <a name="form-identifier-and-name"></a><span data-ttu-id="4681c-109">Formulaire, identificateur et nom</span><span class="sxs-lookup"><span data-stu-id="4681c-109">Form, Identifier, and Name</span></span>

<span data-ttu-id="4681c-110">Les objets de données se présentent sous la forme suivante.</span><span class="sxs-lookup"><span data-stu-id="4681c-110">Data objects have the following form.</span></span>


```
        <Identifier> [name] { [<UUID>]
    <member 1>;
...
    <member n>;
}
```



<span data-ttu-id="4681c-111">L’identificateur est obligatoire et doit correspondre à un type de données ou une primitive défini précédemment.</span><span class="sxs-lookup"><span data-stu-id="4681c-111">The identifier is compulsory and must match a previously defined data type or primitive.</span></span> <span data-ttu-id="4681c-112">Toutefois, le nom est facultatif.</span><span class="sxs-lookup"><span data-stu-id="4681c-112">However, the name is optional.</span></span>

## <a name="data-members"></a><span data-ttu-id="4681c-113">Données membres</span><span class="sxs-lookup"><span data-stu-id="4681c-113">Data Members</span></span>

<span data-ttu-id="4681c-114">Les membres de données peuvent être l’un des suivants : objet de données, référence de données, liste d’entiers, liste flottante ou liste de chaînes.</span><span class="sxs-lookup"><span data-stu-id="4681c-114">Data members can be one of the following: data object, data reference, integer list, float list, or string list.</span></span>

<span data-ttu-id="4681c-115">Un objet de données est un objet de données imbriqué.</span><span class="sxs-lookup"><span data-stu-id="4681c-115">A data object is a nested data object.</span></span> <span data-ttu-id="4681c-116">Cela permet d’exprimer la nature hiérarchique du format de fichier.</span><span class="sxs-lookup"><span data-stu-id="4681c-116">This enables the hierarchical nature of the file format to be expressed.</span></span> <span data-ttu-id="4681c-117">Les types d’objets de données imbriquées autorisés dans la hiérarchie peuvent être restreints.</span><span class="sxs-lookup"><span data-stu-id="4681c-117">The types of nested data objects allowed in the hierarchy may be restricted.</span></span>

<span data-ttu-id="4681c-118">Une référence de données est une référence à un objet de données précédemment rencontré, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="4681c-118">A data reference is a reference to a previously encountered data object as shown in the following example.</span></span>


```
{
  name |
  UUID |
  name UUID
}
```



<span data-ttu-id="4681c-119">Une liste d’entiers est une liste d’entiers séparés par des points-virgules, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="4681c-119">An integer list is a semicolon-separated list of integers, as shown in the following example.</span></span>


```
1; 2; 3;
```



<span data-ttu-id="4681c-120">Une liste flottante est une liste de valeurs float séparées par des points-virgules, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="4681c-120">A float list is a semicolon-separated list of floats, as shown in the following example.</span></span>


```
1.0; 2.0; 3.0;
```



<span data-ttu-id="4681c-121">Une liste de chaînes est une liste de chaînes séparées par des points-virgules, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="4681c-121">A string list is a semicolon-separated list of strings, as shown in the following example.</span></span>


```
"Moose"; "Goats"; "Sheep";
```



## <a name="related-topics"></a><span data-ttu-id="4681c-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4681c-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4681c-123">Encodage de texte</span><span class="sxs-lookup"><span data-stu-id="4681c-123">Text Encoding</span></span>](text-encoding.md)
</dt> </dl>

 

 



