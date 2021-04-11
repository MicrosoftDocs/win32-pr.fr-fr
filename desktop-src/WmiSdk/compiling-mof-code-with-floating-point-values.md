---
description: Le compilateur MOF accepte une valeur à virgule flottante spécifiée pour une propriété à virgule flottante. La valeur est arrondie vers le haut ou vers le haut et stockée sous la forme d’un nombre à virgule flottante. Cette situation peut entraîner des résultats inattendus.
ms.assetid: 5cf7d8e1-c29d-4b9f-8557-e656c5e83370
ms.tgt_platform: multiple
title: Compilation de code MOF avec des valeurs Floating-Point
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 734639e1038b8e9739fead694740dbf5ab5f9cc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203967"
---
# <a name="compiling-mof-code-with-floating-point-values"></a><span data-ttu-id="5f4dd-105">Compilation de code MOF avec des valeurs Floating-Point</span><span class="sxs-lookup"><span data-stu-id="5f4dd-105">Compiling MOF Code with Floating-Point Values</span></span>

<span data-ttu-id="5f4dd-106">Le compilateur MOF accepte une valeur à virgule flottante spécifiée pour une propriété à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="5f4dd-106">The MOF compiler accepts a floating-point value specified for a nonfloating-point property.</span></span> <span data-ttu-id="5f4dd-107">La valeur est arrondie vers le haut ou vers le haut et stockée sous la forme d’un nombre à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="5f4dd-107">The value is rounded up or down and stored as a nonfloating-point number.</span></span> <span data-ttu-id="5f4dd-108">Cette situation peut entraîner des résultats inattendus.</span><span class="sxs-lookup"><span data-stu-id="5f4dd-108">This situation can cause some unexpected results.</span></span>

<span data-ttu-id="5f4dd-109">L’exemple de code MOF suivant définit une classe appelée **ABC** dans un espace de noms appelé « test ».</span><span class="sxs-lookup"><span data-stu-id="5f4dd-109">The following MOF code example defines a class called **abc** in a namespace called "Test".</span></span> <span data-ttu-id="5f4dd-110">Ce code MOF est compilé sans erreurs, mais vous ne pouvez pas interroger la valeur à virgule flottante définie pour la propriété **exampleUint16** dans l’instance créée par ce code.</span><span class="sxs-lookup"><span data-stu-id="5f4dd-110">This MOF code compiles without errors, but you cannot query for the floating-point value defined for the property **exampleUint16** in the instance this code creates.</span></span>

``` syntax
#pragma namespace ("\\\\.\\Root")

instance of __Namespace
{
    Name = "Test";
};

#pragma namespace ("\\\\.\\Root\\test")

Class abc
{
        [KEY] String testID ;
        Uint16 exampleUint16;
        Real64 exampleReal64;
};

Instance of abc
{ 
        TestID ="exampleID";
        exampleUint16 = 1000.4;
};
```

<span data-ttu-id="5f4dd-111">Si vous exécutez la requête suivante, vous recevez un code d’erreur qui indique une requête non valide.</span><span class="sxs-lookup"><span data-stu-id="5f4dd-111">If you issue the following query, you get an error code that indicates an invalid query.</span></span>


```sql
SELECT * FROM abc WHERE exampleUint16 = 1000.4
```



<span data-ttu-id="5f4dd-112">Toutefois, la requête suivante recherche l’instance indiquée.</span><span class="sxs-lookup"><span data-stu-id="5f4dd-112">However, the following query finds the indicated instance.</span></span>


```sql
SELECT * FROM abc WHERE exampleUint16 = 1000
```



## <a name="related-topics"></a><span data-ttu-id="5f4dd-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5f4dd-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f4dd-114">Compilation des fichiers MOF</span><span class="sxs-lookup"><span data-stu-id="5f4dd-114">Compiling MOF Files</span></span>](compiling-mof-files.md)
</dt> <dt>

[<span data-ttu-id="5f4dd-115">**mofcomp**</span><span class="sxs-lookup"><span data-stu-id="5f4dd-115">**mofcomp**</span></span>](mofcomp.md)
</dt> <dt>

[<span data-ttu-id="5f4dd-116">Commandes de préprocesseur</span><span class="sxs-lookup"><span data-stu-id="5f4dd-116">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 



