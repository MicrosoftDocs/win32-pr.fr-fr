---
description: Une carte de valeur est un tableau lié à une propriété avec les qualificateurs value et ValueMap.
ms.assetid: 7667e87f-b997-4fd9-81ea-b27c9d2a9335
ms.tgt_platform: multiple
title: ValueMap et qualificateurs de valeur
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df85342df9543e4d62b04482785ec31bb5bd3982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524339"
---
# <a name="valuemap-and-value-qualifiers"></a><span data-ttu-id="ae512-103">ValueMap et qualificateurs de valeur</span><span class="sxs-lookup"><span data-stu-id="ae512-103">ValueMap and Value Qualifiers</span></span>

<span data-ttu-id="ae512-104">Une carte de valeur est un tableau lié à une propriété avec les qualificateurs **value** et **ValueMap** .</span><span class="sxs-lookup"><span data-stu-id="ae512-104">A value map is an array linked to a property with the **Value** and **ValueMap** qualifiers.</span></span>

<span data-ttu-id="ae512-105">La propriété agit comme un index dans le tableau, en maintenant une valeur qui représente l’une des valeurs du tableau.</span><span class="sxs-lookup"><span data-stu-id="ae512-105">The property acts as an index into the array, holding a value that represents one of the values in the array.</span></span> <span data-ttu-id="ae512-106">À l’aide de code MOF, vous pouvez avoir les types de mappages de valeurs suivants :</span><span class="sxs-lookup"><span data-stu-id="ae512-106">Using MOF code, you can have the following types of value maps:</span></span>

-   <span data-ttu-id="ae512-107">Tableau mappé à un entier.</span><span class="sxs-lookup"><span data-stu-id="ae512-107">Array mapping to an integer.</span></span>

    <span data-ttu-id="ae512-108">Vous pouvez définir un tableau avec le qualificateur de **valeur** et lier le tableau directement à une propriété entière, comme indiqué dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="ae512-108">You can define an array with the **Value** qualifier and link the array directly to an integer property, as shown in the following example:</span></span>

    ``` syntax
    [Values {"OK", "Error", "Degraded", "Unknown"}, Read]
    sint32 Status;
    ```

    <span data-ttu-id="ae512-109">Dans cet exemple, la valeur de la propriété **Status** est un index dans le tableau de chaînes défini par **value**.</span><span class="sxs-lookup"><span data-stu-id="ae512-109">In this example, the **Status** property value is an index into the string array defined by **Value**.</span></span> <span data-ttu-id="ae512-110">La propriété ne peut prendre que des valeurs qui correspondent aux positions ordinales dans le tableau de **valeurs** moins 1.</span><span class="sxs-lookup"><span data-stu-id="ae512-110">The property can only take on values that correspond to the ordinal positions in the **Value** array minus 1.</span></span> <span data-ttu-id="ae512-111">Par exemple, la définition de l' **État** sur « 1 » mappe à la valeur « erreur ».</span><span class="sxs-lookup"><span data-stu-id="ae512-111">For example, setting **Status** to "1" maps to the "Error" value.</span></span> <span data-ttu-id="ae512-112">La propriété d’index ne peut prendre que des valeurs qui correspondent aux positions dans le tableau de **valeurs** .</span><span class="sxs-lookup"><span data-stu-id="ae512-112">The index property can take only values that correspond to positions in the **Value** array.</span></span> <span data-ttu-id="ae512-113">Par exemple, si le tableau comporte 10 entrées, la valeur de la propriété index peut être comprise entre 0 et 9, et non 30 ou 177.</span><span class="sxs-lookup"><span data-stu-id="ae512-113">For example, if the array has 10 entries, the index property can story 0 through 9, not 30 or 177.</span></span>

-   <span data-ttu-id="ae512-114">Mappage d’un tableau à un autre tableau à un entier.</span><span class="sxs-lookup"><span data-stu-id="ae512-114">Array mapping to another array mapping to an integer.</span></span>

    <span data-ttu-id="ae512-115">Si vous souhaitez créer un index qui n’utilise pas de système ordinal de comptage, utilisez le qualificateur **ValueMap** .</span><span class="sxs-lookup"><span data-stu-id="ae512-115">If you wish to create an index that does not use an ordinal system of counting, use the **ValueMap** qualifier.</span></span> <span data-ttu-id="ae512-116">Le qualificateur **ValueMap** définit un autre tableau qui contient un système de numérotation d’index arbitraire, comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="ae512-116">The **ValueMap** qualifier sets up another array that holds an arbitrary index numbering system, as shown in the following example:</span></span>

    ``` syntax
    [ValueMap {"1", "3", "99", "0"}, 
     Values {"OK", "Error", "Degraded", "Unknown"}, Read]
    sint32 Status;
    ```

    <span data-ttu-id="ae512-117">Bien que vous soyez tenu de placer les valeurs de **ValueMap** entre guillemets, WMI prend en compte les valeurs entières.</span><span class="sxs-lookup"><span data-stu-id="ae512-117">Although you must place the values of **ValueMap** in quotations, WMI considers the values integers.</span></span> <span data-ttu-id="ae512-118">Par conséquent, dans cet exemple, vous pouvez définir la propriété **Status** sur un entier dans l’ensemble **ValueMap** : 1, 3, 99 ou 0.</span><span class="sxs-lookup"><span data-stu-id="ae512-118">Therefore, In this example you can set the **Status** property to an integer in the **ValueMap** set: 1, 3, 99, or 0.</span></span> <span data-ttu-id="ae512-119">WMI mappe chaque entier d’une position ordinale dans le tableau de chaînes **ValueMap** à une position correspondante dans le tableau de **valeurs** .</span><span class="sxs-lookup"><span data-stu-id="ae512-119">WMI maps each integer from an ordinal position in the **ValueMap** string array to a corresponding position in the **Value** array.</span></span> <span data-ttu-id="ae512-120">Par exemple, la définition de l' **État** sur 0 correspond à « inconnu ».</span><span class="sxs-lookup"><span data-stu-id="ae512-120">For example, setting **Status** to 0 maps to "Unknown".</span></span>

-   <span data-ttu-id="ae512-121">Mappage d’un tableau à un autre tableau à une chaîne.</span><span class="sxs-lookup"><span data-stu-id="ae512-121">Array mapping to another array mapping to a string.</span></span>

    <span data-ttu-id="ae512-122">Si vous ne souhaitez pas utiliser un entier pour indexer votre tableau, vous pouvez utiliser à la place une chaîne pour contenir l’une des valeurs possibles dans votre tableau.</span><span class="sxs-lookup"><span data-stu-id="ae512-122">If you do not want to use an integer to index your array, you can instead use a string to hold one of the possible values in your array.</span></span> <span data-ttu-id="ae512-123">Pour ce faire, vous devez définir à la fois une **valeur** et un tableau **ValueMap** qui contiennent tous les deux des chaînes, comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="ae512-123">To do so, you must define both a **Value** and **ValueMap** array that both contain strings, as shown in the following example:</span></span>

    ``` syntax
    [ValueMap {"OK", "Error", "Degraded", "Unknown"}, 
     Values {"OK", "Error", "Degraded", "Unknown"}, Read]
    string Status;
    ```

    <span data-ttu-id="ae512-124">Avec une propriété de type chaîne, les valeurs réelles autorisées de la propriété sont les entrées du tableau **ValueMap** .</span><span class="sxs-lookup"><span data-stu-id="ae512-124">With a string property, the actual allowable values of the property are the entries in the **ValueMap** array.</span></span> <span data-ttu-id="ae512-125">Par exemple, vous pouvez définir l' **État** sur « OK » ou « inconnu ».</span><span class="sxs-lookup"><span data-stu-id="ae512-125">For example, you can set **Status** to "OK" or "Unknown".</span></span>

<span data-ttu-id="ae512-126">Il revient à l’application de tirer parti des mappages de façon utile.</span><span class="sxs-lookup"><span data-stu-id="ae512-126">It is up to the application to take advantage of mappings in a useful way.</span></span> <span data-ttu-id="ae512-127">Il revient au fournisseur d’appliquer une plage légale de valeurs.</span><span class="sxs-lookup"><span data-stu-id="ae512-127">It is up to the provider to enforce a legal range of values.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae512-128">Notes</span><span class="sxs-lookup"><span data-stu-id="ae512-128">Remarks</span></span>

<span data-ttu-id="ae512-129">Pour déterminer s’il faut utiliser les / qualificateurs de **valeur** ValueMap ou de **bitmaps de bitmap** /  , déterminez si l’une des valeurs indiquées peut se produire simultanément.</span><span class="sxs-lookup"><span data-stu-id="ae512-129">In deciding whether to use the **ValueMap**/**Value** or **BitMap**/**BitValues** qualifiers, determine whether any of the values being indicated could occur concurrently.</span></span> <span data-ttu-id="ae512-130">Si plusieurs valeurs simultanées peuvent exister, vous devez utiliser des / **bitvalues** bitmap.</span><span class="sxs-lookup"><span data-stu-id="ae512-130">If multiple concurrent values can exist, you must use **BitMap**/**BitValues**.</span></span> <span data-ttu-id="ae512-131">Si toutes les valeurs s’excluent mutuellement, vous devez utiliser les / qualificateurs de **valeur** ValueMap.</span><span class="sxs-lookup"><span data-stu-id="ae512-131">If all the values are mutually exclusive, you should use the **ValueMap**/**Value** qualifiers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae512-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ae512-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae512-133">BitMap et BitValue</span><span class="sxs-lookup"><span data-stu-id="ae512-133">BitMap and BitValues</span></span>](bitmap-and-bitvalues.md)
</dt> </dl>

 

 



