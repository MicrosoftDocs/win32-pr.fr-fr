---
description: L’espace de noms WMI est un objet de programmation qui définit la portée d’un ensemble de classes et d’instances. Les classes du fournisseur WMI doivent être définies à l’intérieur d’un espace de noms.
ms.assetid: a00f26e6-bb81-45bc-a530-9346a074bb3c
ms.tgt_platform: multiple
title: Création de hiérarchies dans WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5743c8da8c40fc0419a96a8ec9c65e7e112573a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202298"
---
# <a name="creating-hierarchies-within-wmi"></a><span data-ttu-id="52738-104">Création de hiérarchies dans WMI</span><span class="sxs-lookup"><span data-stu-id="52738-104">Creating Hierarchies Within WMI</span></span>

<span data-ttu-id="52738-105">L' [*espace de noms WMI*](gloss-n.md) est un objet de programmation qui définit la portée d’un ensemble de classes et d’instances.</span><span class="sxs-lookup"><span data-stu-id="52738-105">[*WMI namespace*](gloss-n.md) is a programming object that defines the scope for a set of classes and instances.</span></span> <span data-ttu-id="52738-106">Les classes du fournisseur WMI doivent être définies à l’intérieur d’un espace de noms.</span><span class="sxs-lookup"><span data-stu-id="52738-106">WMI provider classes must be defined inside a namespace.</span></span>

<span data-ttu-id="52738-107">Les espaces de noms décrivent différents environnements gérés, tels que l’environnement SMS.</span><span class="sxs-lookup"><span data-stu-id="52738-107">Namespaces describe different managed environments, such as the SMS environment.</span></span> <span data-ttu-id="52738-108">Étant donné que les classes et les instances d’un schéma définissent les composants d’un environnement managé, chaque nouveau schéma requiert un nouvel espace de noms.</span><span class="sxs-lookup"><span data-stu-id="52738-108">Because the classes and instances of a schema define the components of a managed environment, each new schema requires a new namespace.</span></span> <span data-ttu-id="52738-109">Par exemple, l' \\ espace de noms CIMV2 racine contient les classes et les instances définies dans le schéma Win32, ainsi que les classes parent Common Information Model (CIM) dont hérite le schéma Win32.</span><span class="sxs-lookup"><span data-stu-id="52738-109">For example, the root\\cimv2 namespace contains the classes and instances defined in the Win32 schema as well as the parent Common Information Model (CIM) classes from which the Win32 schema inherits.</span></span> <span data-ttu-id="52738-110">Les classes CIM sont définies par la[DMTF](https://www.dmtf.org/home)(Distributed Management Task Force).</span><span class="sxs-lookup"><span data-stu-id="52738-110">CIM classes are defined by the Distributed Management Task Force ([DMTF](https://www.dmtf.org/home)).</span></span>

> [!Note]  
> <span data-ttu-id="52738-111">Pour vous assurer que toutes les définitions de classe WMI pour les objets managés sont restaurées dans l' [*espace de stockage WMI*](gloss-w.md) en cas d’échec et de redémarrage de WMI, utilisez l’instruction [**\# pragma AutoRecover**](pragma-autorecover.md) de préprocesseur dans votre fichier [*format MOF (MOF)*](gloss-m.md) .</span><span class="sxs-lookup"><span data-stu-id="52738-111">To ensure that all of your WMI class definitions for managed objects are restored to the [*WMI repository*](gloss-w.md) if WMI has a failure and restarts, use the [**\#pragma autorecover**](pragma-autorecover.md) preprocessor instruction in your [*Managed Object Format (MOF)*](gloss-m.md) file.</span></span>

 

<span data-ttu-id="52738-112">WMI définit un espace de noms en tant qu’instance de la classe système d' [**\_ \_ espace de noms**](--namespace.md) ou toute classe qui dérive de l’espace de **\_ \_ noms**.</span><span class="sxs-lookup"><span data-stu-id="52738-112">WMI defines a namespace as an instance of the [**\_\_Namespace**](--namespace.md) system class or any class that derives from **\_\_Namespace**.</span></span> <span data-ttu-id="52738-113">La classe de système d' **\_ \_ espace de noms** a une propriété unique appelée **Name**, qui doit être unique dans l’étendue de l’espace de noms parent.</span><span class="sxs-lookup"><span data-stu-id="52738-113">The **\_\_Namespace** system class has a single property called **Name**, which must be unique within the scope of the parent namespace.</span></span> <span data-ttu-id="52738-114">La propriété **Name** doit également contenir une chaîne qui commence par une lettre.</span><span class="sxs-lookup"><span data-stu-id="52738-114">The **Name** property must also contain a string that begins with a letter.</span></span> <span data-ttu-id="52738-115">Tous les autres caractères de la chaîne peuvent être des lettres, des chiffres ou des traits de soulignement.</span><span class="sxs-lookup"><span data-stu-id="52738-115">All other characters in the string can be letters, digits, or underscores.</span></span> <span data-ttu-id="52738-116">Tous les caractères ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="52738-116">All characters are case-insensitive.</span></span>

<span data-ttu-id="52738-117">En plus de déterminer le nom unique d’un espace de noms enfant, l’espace de noms WMI parent peut protéger les instances statiques de vos classes contre les modifications accidentelles d’autres fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="52738-117">In addition to determining the unique name for a child namespace, the parent WMI namespace can protect the static instances of your classes from accidental modification by other providers.</span></span> <span data-ttu-id="52738-118">Par exemple, il peut s’avérer pratique d’imbriquer un nouvel espace de noms sous un espace de noms existant pour un autre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="52738-118">For example, you may find it convenient to nest a new namespace under an existing namespace for another provider.</span></span> <span data-ttu-id="52738-119">Toutefois, le fournisseur d’origine peut tenter de mettre à jour toutes les instances de classe pour qu’elles correspondent à un nouveau schéma.</span><span class="sxs-lookup"><span data-stu-id="52738-119">However, the original provider may try to update all class instances to match up with a new schema.</span></span> <span data-ttu-id="52738-120">Dans ce cas, le fournisseur d’origine peut supprimer tous les sous-enfants d’un espace de noms.</span><span class="sxs-lookup"><span data-stu-id="52738-120">In doing so, the original provider may delete all sub-children in a namespace.</span></span> <span data-ttu-id="52738-121">Bien qu’il s’agit d’une action appropriée pour l’espace de noms cible, elle peut affecter les instances de classe non liées dans un espace de noms enfant (c’est-à-dire vos propres classes de fournisseur).</span><span class="sxs-lookup"><span data-stu-id="52738-121">While this may be an appropriate action for the target namespace, it may affect unrelated class instances in a child namespace (i.e., your own provider classes).</span></span>

<span data-ttu-id="52738-122">Par conséquent, il est généralement recommandé de créer et d’enregistrer votre espace de noms séparément des espaces de noms que vous ne contrôlez pas directement.</span><span class="sxs-lookup"><span data-stu-id="52738-122">Therefore, it is generally recommended that you create and register your namespace as separate from namespaces that you do not directly control.</span></span> <span data-ttu-id="52738-123">Cela est particulièrement vrai si vos classes dérivent uniquement de classes CIM générales ou d’autres classes de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="52738-123">This is especially true if your classes derive only from general CIM classes or other classes from your company.</span></span> <span data-ttu-id="52738-124">Votre espace de noms peut être sous l’espace de noms **racine** , comme suit :</span><span class="sxs-lookup"><span data-stu-id="52738-124">Your namespace can be under the **Root** namespace, such as the following:</span></span>

<span data-ttu-id="52738-125">**Root/myCompany/myProduct**</span><span class="sxs-lookup"><span data-stu-id="52738-125">**Root/myCompany/myProduct**</span></span>

<span data-ttu-id="52738-126">En revanche, si votre nouvelle classe dérive de la classe d’un autre fournisseur, vous devrez peut-être stocker votre classe dans un sous-espace de noms de ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="52738-126">In contrast, if your new class derives from the class of another provider, you may need to store your class in a sub-namespace of that provider.</span></span> <span data-ttu-id="52738-127">Notez que cela expose votre nouvelle classe à une suppression accidentelle par le fournisseur d’origine.</span><span class="sxs-lookup"><span data-stu-id="52738-127">Note that this exposes your new class to accidental deletion by the original provider.</span></span>

<span data-ttu-id="52738-128">WMI offre plusieurs méthodes différentes pour créer un espace de noms :</span><span class="sxs-lookup"><span data-stu-id="52738-128">WMI provides several different ways to create a namespace:</span></span>

-   [<span data-ttu-id="52738-129">Création d’un espace de noms enfant avec du code MOF</span><span class="sxs-lookup"><span data-stu-id="52738-129">Creating a Child Namespace with MOF Code</span></span>](creating-a-child-namespace-with-mof-code.md)
-   [<span data-ttu-id="52738-130">Création d’un espace de noms frère avec du code MOF</span><span class="sxs-lookup"><span data-stu-id="52738-130">Creating a Sibling Namespace with MOF Code</span></span>](creating-a-sibling-namespace-with-mof-code.md)
-   [<span data-ttu-id="52738-131">Création d’un espace de noms avec l’API WMI</span><span class="sxs-lookup"><span data-stu-id="52738-131">Creating a Namespace with the WMI API</span></span>](creating-a-namespace-with-the-wmi-api.md)

## <a name="related-topics"></a><span data-ttu-id="52738-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="52738-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52738-133">Conception de classes format MOF (MOF)</span><span class="sxs-lookup"><span data-stu-id="52738-133">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



