---
description: À l’instar de nombreuses autres techniques en format MOF (MOF), l’application d’un qualificateur à votre code est un processus relativement simple.
ms.assetid: aaa5c921-bdcd-40e6-ab4b-9441a1957e5b
ms.tgt_platform: multiple
title: Application d’un qualificateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 042a3cdbf7236dc838735ce0cbf18a6315dd02e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760779"
---
# <a name="applying-a-qualifier"></a><span data-ttu-id="a4f7d-103">Application d’un qualificateur</span><span class="sxs-lookup"><span data-stu-id="a4f7d-103">Applying a Qualifier</span></span>

<span data-ttu-id="a4f7d-104">À l’instar de nombreuses autres techniques en format MOF (MOF), l’application d’un qualificateur à votre code est un processus relativement simple.</span><span class="sxs-lookup"><span data-stu-id="a4f7d-104">Like many other techniques in Managed Object Format (MOF), applying a qualifier to your code is a relatively simple process.</span></span>

<span data-ttu-id="a4f7d-105">Les conventions d’affectation de noms appliquées par WMI sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="a4f7d-105">The only real challenges are the following restrictions in naming conventions that WMI enforces:</span></span>

-   <span data-ttu-id="a4f7d-106">Un qualificateur peut décrire une classe, une instance, une propriété, une méthode ou un paramètre de méthode.</span><span class="sxs-lookup"><span data-stu-id="a4f7d-106">A qualifier can describe a class, instance, property, method, or method parameter.</span></span>
-   <span data-ttu-id="a4f7d-107">Les noms de qualificateurs ne peuvent pas avoir de traits de soulignement de début ou de fin.</span><span class="sxs-lookup"><span data-stu-id="a4f7d-107">Qualifier names cannot have either leading or trailing underscores.</span></span>
-   <span data-ttu-id="a4f7d-108">Un nom de qualificateur ne peut pas commencer par un chiffre.</span><span class="sxs-lookup"><span data-stu-id="a4f7d-108">A qualifier name cannot begin with a digit.</span></span>
-   <span data-ttu-id="a4f7d-109">Un nom de qualificateur ne peut pas contenir de caractères spéciaux tels que & \* @ !</span><span class="sxs-lookup"><span data-stu-id="a4f7d-109">A qualifier name cannot contain special characters such as & \* @ !</span></span><span data-ttu-id="a4f7d-110"> ~ \\ /.</span><span class="sxs-lookup"><span data-stu-id="a4f7d-110"> ~ \\ /.</span></span>
-   <span data-ttu-id="a4f7d-111">Tous les noms de qualificateurs ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="a4f7d-111">All qualifier names are case-insensitive.</span></span>
-   <span data-ttu-id="a4f7d-112">Vous ne pouvez pas redéfinir les qualificateurs WMI standard ou les qualificateurs décrits dans la spécification CIM DMTF.</span><span class="sxs-lookup"><span data-stu-id="a4f7d-112">You cannot redefine the standard WMI qualifiers or any qualifiers described in the DMTF CIM specification.</span></span>
-   <span data-ttu-id="a4f7d-113">Les types de qualificateurs ne sont pas explicitement déclarés.</span><span class="sxs-lookup"><span data-stu-id="a4f7d-113">Qualifier types are not explicitly declared.</span></span>

    <span data-ttu-id="a4f7d-114">Si vous ne déclarez pas de type de qualificateur, WMI suppose que le type est booléen avec la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="a4f7d-114">If you do not declare a qualifier type, WMI assumes the type as Boolean with a value of **TRUE**.</span></span> <span data-ttu-id="a4f7d-115">Sinon, les qualificateurs de type WMI sont basés sur les valeurs de qualificateur que vous déclarez.</span><span class="sxs-lookup"><span data-stu-id="a4f7d-115">Otherwise, WMI types qualifiers based on the qualifier values you declare.</span></span>

-   <span data-ttu-id="a4f7d-116">Lorsque vous créez vos propres qualificateurs, vous devez faire précéder le nom de votre schéma d’un nom de qualificateur.</span><span class="sxs-lookup"><span data-stu-id="a4f7d-116">When creating your own qualifiers, you should prefix your schema name to your qualifier name.</span></span>

    <span data-ttu-id="a4f7d-117">L’objectif de cette règle est d’éviter toute confusion avec les nouveaux qualificateurs.</span><span class="sxs-lookup"><span data-stu-id="a4f7d-117">The purpose of this rule is to avoid confusion with new qualifiers.</span></span>

-   <span data-ttu-id="a4f7d-118">Vous pouvez créer des tableaux homogènes de qualificateurs.</span><span class="sxs-lookup"><span data-stu-id="a4f7d-118">You can create homogeneous arrays of qualifiers.</span></span>

    <span data-ttu-id="a4f7d-119">L’exemple de code suivant montre comment les tableaux de qualificateurs sont spécifiés à l’aide d’accolades qui entourent les valeurs.</span><span class="sxs-lookup"><span data-stu-id="a4f7d-119">The following code example shows how qualifier arrays are specified with curly braces that surround the values.</span></span>

    ``` syntax
    [StringArray{"hello", "there"}, SingleElementArray{3}]
    ```

-   <span data-ttu-id="a4f7d-120">WMI ne prend pas en charge les types Automation non listés dans la référence, tels que VT \_ null.</span><span class="sxs-lookup"><span data-stu-id="a4f7d-120">WMI does not support automation types not listed in the reference, such as VT\_NULL.</span></span> <span data-ttu-id="a4f7d-121">Pour plus d’informations, consultez [types de données MOF](mof-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="a4f7d-121">For more information, see [MOF Data Types](mof-data-types.md).</span></span>

<span data-ttu-id="a4f7d-122">La procédure suivante vous aide à utiliser C++ pour ajouter un qualificateur à une propriété.</span><span class="sxs-lookup"><span data-stu-id="a4f7d-122">The following procedure helps you to use C++ to add a qualifier to a property.</span></span>

<span data-ttu-id="a4f7d-123">**Pour appliquer un qualificateur à l’aide de C++**</span><span class="sxs-lookup"><span data-stu-id="a4f7d-123">**To apply a qualifier using C++**</span></span>

-   <span data-ttu-id="a4f7d-124">Appliquez le qualificateur avec un appel à la méthode [**IWbemQualifierSet ::P ut**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) .</span><span class="sxs-lookup"><span data-stu-id="a4f7d-124">Apply the qualifier with a call to the [**IWbemQualifierSet::Put**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) method.</span></span>

    <span data-ttu-id="a4f7d-125">Vous pouvez utiliser d’autres méthodes de [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) pour récupérer ou supprimer des qualificateurs existants.</span><span class="sxs-lookup"><span data-stu-id="a4f7d-125">You can use other methods of [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) to retrieve or delete existing qualifiers.</span></span>

<span data-ttu-id="a4f7d-126">La procédure suivante vous permet d’appliquer un qualificateur dans les fichiers MOF.</span><span class="sxs-lookup"><span data-stu-id="a4f7d-126">The following procedure helps you to apply a qualifier in MOF files.</span></span>

<span data-ttu-id="a4f7d-127">**Pour décrire un mot clé ou un identificateur avec un qualificateur à l’aide de MOF**</span><span class="sxs-lookup"><span data-stu-id="a4f7d-127">**To describe a keyword or identifier with a qualifier using MOF**</span></span>

-   <span data-ttu-id="a4f7d-128">Placez un qualificateur entre crochets avant le mot clé ou l’identificateur décrit par le qualificateur.</span><span class="sxs-lookup"><span data-stu-id="a4f7d-128">Place a qualifier in brackets before the keyword or identifier described by the qualifier.</span></span>

    <span data-ttu-id="a4f7d-129">L’exemple de code suivant montre comment les qualificateurs sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="a4f7d-129">The following code example shows how qualifiers are used.</span></span>

    ``` syntax
    [qualifiers...]
    class StdDisk
    {
      [qualifiers...]  uint32 dwNumCylinders;
      [qualifiers...]  uint32 dwNumHeads;
      [qualifiers...]  sint32 Method1();
      sint32 Method2([qualifiers...] Parameter1);
    };
    ```

    <span data-ttu-id="a4f7d-130">L’exemple suivant décrit le positionnement correct des qualificateurs.</span><span class="sxs-lookup"><span data-stu-id="a4f7d-130">The following example describes the proper placement of qualifiers.</span></span>

    ``` syntax
    [Abstract]
    class MyClass
    {
        [Amendment, InstanceOf]  uint32 dwNumber;
        sint32 MyMethod ([in] sint32 Param);
    };
    ```

 

 



