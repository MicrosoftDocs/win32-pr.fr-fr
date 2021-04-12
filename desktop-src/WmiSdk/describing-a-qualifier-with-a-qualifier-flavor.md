---
description: Une version de qualificateur est un indicateur qui décrit des informations supplémentaires sur un qualificateur.
ms.assetid: a7d9d1c0-9386-4c90-9788-993b35ed12db
ms.tgt_platform: multiple
title: Description d’un qualificateur avec une version de qualificateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525cfc2c590ec8916e2e9538b3e8224e97b3b5dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202293"
---
# <a name="describing-a-qualifier-with-a-qualifier-flavor"></a><span data-ttu-id="43d06-103">Description d’un qualificateur avec une version de qualificateur</span><span class="sxs-lookup"><span data-stu-id="43d06-103">Describing a Qualifier with a Qualifier Flavor</span></span>

<span data-ttu-id="43d06-104">Une [*version de qualificateur*](gloss-q.md) est un indicateur qui décrit des informations supplémentaires sur un qualificateur.</span><span class="sxs-lookup"><span data-stu-id="43d06-104">A [*qualifier flavor*](gloss-q.md) is a flag that describes more information about a qualifier.</span></span> <span data-ttu-id="43d06-105">Par exemple, la version de qualificateur restreint indique que WMI ne doit pas propager le qualificateur associé à une instance ou à une classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="43d06-105">For example, the Restricted qualifier flavor states that WMI should not propagate the associated qualifier to any derived classes or instances.</span></span> <span data-ttu-id="43d06-106">Vous pouvez définir des versions à l’aide d’un code MOF ou par programme.</span><span class="sxs-lookup"><span data-stu-id="43d06-106">You can set flavors using either MOF code or programmatically.</span></span> <span data-ttu-id="43d06-107">Bien que vous puissiez décrire divers effets avec des versions, les principaux objectifs des indicateurs Flavors sont de définir comment WMI propage les qualificateurs par héritage.</span><span class="sxs-lookup"><span data-stu-id="43d06-107">While you can describe a variety of effects with flavors, the main purposes of flavor flags is to define how WMI propagates qualifiers through inheritance.</span></span>

<span data-ttu-id="43d06-108">WMI définit plusieurs versions de qualificateur que vous pouvez attacher à n’importe quel qualificateur, quelle que soit l’origine du qualificateur.</span><span class="sxs-lookup"><span data-stu-id="43d06-108">WMI defines several qualifier flavors that you can attach to any qualifier, regardless of the origin of the qualifier.</span></span> <span data-ttu-id="43d06-109">Toutefois, certaines versions ne sont pas appropriées pour tous les types de qualificateurs.</span><span class="sxs-lookup"><span data-stu-id="43d06-109">However, some flavors are not appropriate for all qualifier types.</span></span> <span data-ttu-id="43d06-110">Par exemple, la version **ToSubClass** est appropriée uniquement pour les qualificateurs définis pour une classe.</span><span class="sxs-lookup"><span data-stu-id="43d06-110">The **ToSubClass** flavor, for example, is appropriate only for qualifiers defined for a class.</span></span> <span data-ttu-id="43d06-111">Vous ne pouvez pas joindre **ToSubClass** à un qualificateur utilisé pour décrire une instance.</span><span class="sxs-lookup"><span data-stu-id="43d06-111">You cannot attach **ToSubClass** to a qualifier used to describe an instance.</span></span>

<span data-ttu-id="43d06-112">Vous pouvez utiliser des versions pour décrire divers effets différents pour les qualificateurs.</span><span class="sxs-lookup"><span data-stu-id="43d06-112">You can use flavors to describe a variety of different effects for qualifiers.</span></span> <span data-ttu-id="43d06-113">Par exemple, la version peut indiquer si un qualificateur peut être localisé.</span><span class="sxs-lookup"><span data-stu-id="43d06-113">For example, flavor can indicate if a qualifier can be localized.</span></span> <span data-ttu-id="43d06-114">Toutefois, l’un des principaux objectifs d’une version de qualificateur est de décrire si une classe parente peut passer des qualificateurs à une sous-classe ou à une instance de classe.</span><span class="sxs-lookup"><span data-stu-id="43d06-114">However, one of the main purposes of a qualifier flavor is to describe whether a parent class can pass qualifiers to a subclass or class instance.</span></span> <span data-ttu-id="43d06-115">Vous pouvez également utiliser des versions pour déterminer si une propriété de classe passe un qualificateur à une propriété d’instance.</span><span class="sxs-lookup"><span data-stu-id="43d06-115">You can also use flavors to determine if a class property passes a qualifier on to an instance property.</span></span> <span data-ttu-id="43d06-116">Enfin, utilisez des versions pour indiquer si une sous-classe peut remplacer la valeur d’origine d’un qualificateur hérité.</span><span class="sxs-lookup"><span data-stu-id="43d06-116">Finally, use flavors to state whether a subclass can override the original value of an inherited qualifier.</span></span> <span data-ttu-id="43d06-117">Toutefois, les qualificateurs que vous déclarez pour une classe ou une instance ne se propagent pas aux propriétés de cette classe ou instance.</span><span class="sxs-lookup"><span data-stu-id="43d06-117">However, qualifiers that you declare for a class or instance do not propagate to the properties of that class or instance.</span></span> <span data-ttu-id="43d06-118">En outre, les versions qui établissent des autorisations de remplacement ne sont valides que si vous définissez également les versions **ToInstance** ou **ToSubClass** .</span><span class="sxs-lookup"><span data-stu-id="43d06-118">Further, flavors that establish override permissions are valid only if you also set the **ToInstance** or **ToSubClass** flavors.</span></span>

<span data-ttu-id="43d06-119">Une version peut être affectée globalement à un qualificateur pour l’intégralité d’un fichier MOF à l’aide de la syntaxe suivante, dans laquelle l’espace blanc agit comme séparateur lorsque plusieurs versions sont spécifiées.</span><span class="sxs-lookup"><span data-stu-id="43d06-119">A flavor can be globally assigned to a qualifier for an entire MOF file using the following syntax in which white space acts as the delimiter when multiple flavors are specified.</span></span>

``` syntax
Qualifier QualifierName : flavor1 <flavor2...>;
```

<span data-ttu-id="43d06-120">Les versions globales s’appliquent à toutes les utilisations suivantes du qualificateur dans le fichier MOF.</span><span class="sxs-lookup"><span data-stu-id="43d06-120">Global flavors apply to all subsequent uses of the qualifier in the MOF file.</span></span> <span data-ttu-id="43d06-121">Les instructions de version globale peuvent se trouver n’importe où dans le fichier en dehors d’un bloc de déclaration d’objet.</span><span class="sxs-lookup"><span data-stu-id="43d06-121">Global flavor statements may occur anywhere in the file outside of an object declaration block.</span></span> <span data-ttu-id="43d06-122">Les parfums redéfinis au niveau de la classe, de l’instance ou de la propriété remplacent les déclarations de arôme global pour la portée de cet objet.</span><span class="sxs-lookup"><span data-stu-id="43d06-122">Flavors redefined at the class, instance, or property level override the global flavor declarations for the scope of that object.</span></span>

<span data-ttu-id="43d06-123">Vous ne pouvez pas définir une nouvelle version.</span><span class="sxs-lookup"><span data-stu-id="43d06-123">You cannot define a new flavor.</span></span> <span data-ttu-id="43d06-124">Bien que vous puissiez créer un qualificateur, utilisez uniquement des [versions de qualificateur](qualifier-flavors.md) existantes pour décrire votre nouveau qualificateur.</span><span class="sxs-lookup"><span data-stu-id="43d06-124">Although you can create a new qualifier, use only existing [Qualifier Flavors](qualifier-flavors.md) to describe your new qualifier.</span></span>

<span data-ttu-id="43d06-125">**Pour définir des versions de qualificateur dans MOF**</span><span class="sxs-lookup"><span data-stu-id="43d06-125">**To define qualifier flavors in MOF**</span></span>

-   <span data-ttu-id="43d06-126">Déclarez les versions qui décrivent un qualificateur donné après le nom du qualificateur, entre les crochets du qualificateur.</span><span class="sxs-lookup"><span data-stu-id="43d06-126">Declare the flavors that describe a given qualifier after the qualifier name, between the qualifier brackets.</span></span> <span data-ttu-id="43d06-127">Utilisez un espace blanc comme délimiteur entre plusieurs versions.</span><span class="sxs-lookup"><span data-stu-id="43d06-127">Use white space as the delimiter between multiple flavors.</span></span>

    <span data-ttu-id="43d06-128">L’exemple suivant illustre le modèle d’attachement de qualificateurs prédéfinis.</span><span class="sxs-lookup"><span data-stu-id="43d06-128">The following example shows the pattern for attaching predefined qualifiers.</span></span>

    ``` syntax
    [qualifier1 : flavor1 flavor2 flavor3, qualifier2 : flavor1]
    ```

<span data-ttu-id="43d06-129">Vous pouvez ajouter des versions de qualificateur par programmation uniquement en C++.</span><span class="sxs-lookup"><span data-stu-id="43d06-129">You can add qualifier flavors programmatically only in C++.</span></span> <span data-ttu-id="43d06-130">Cette opération n’est pas disponible dans l' [API de script pour WMI](scripting-api-for-wmi.md), bien que vous puissiez ajouter un nouveau qualificateur en appelant [**SWbemQualifierSet. Add**](swbemqualifierset-add.md).</span><span class="sxs-lookup"><span data-stu-id="43d06-130">This operation is not available in the [Scripting API for WMI](scripting-api-for-wmi.md), although you can add a new qualifier by calling [**SWbemQualifierSet.Add**](swbemqualifierset-add.md).</span></span>

<span data-ttu-id="43d06-131">**Pour assigner une version à l’aide de C++**</span><span class="sxs-lookup"><span data-stu-id="43d06-131">**To assign a flavor using C++**</span></span>

-   <span data-ttu-id="43d06-132">Appelez la méthode [**IWbemQualifierSet ::P ut**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) avec le paramètre *lFlavor* défini sur l’une des constantes définies pour la méthode.</span><span class="sxs-lookup"><span data-stu-id="43d06-132">Call the [**IWbemQualifierSet::Put**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) method with the *lFlavor* parameter set to one of the constants defined for the method.</span></span>

 

 



