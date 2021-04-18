---
description: Un qualificateur est une chaîne de données qui fournit plus d’informations sur une classe, une instance, une propriété, une méthode ou un paramètre.
ms.assetid: 6984b575-b365-49dd-aeab-a763430f434c
ms.tgt_platform: multiple
title: Ajout d’un qualificateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5a6f18f2b79bcd25b2b4ca75811157c9091e6eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106542999"
---
# <a name="adding-a-qualifier"></a><span data-ttu-id="bc4b7-103">Ajout d’un qualificateur</span><span class="sxs-lookup"><span data-stu-id="bc4b7-103">Adding a Qualifier</span></span>

<span data-ttu-id="bc4b7-104">Un qualificateur est une chaîne de données qui fournit plus d’informations sur une classe, une instance, une propriété, une méthode ou un paramètre.</span><span class="sxs-lookup"><span data-stu-id="bc4b7-104">A qualifier is a data string that provides more information about a class, instance, property, method, or parameter.</span></span>

<span data-ttu-id="bc4b7-105">La définition de classe suivante est un exemple de classe dérivée qui a des qualificateurs de classe.</span><span class="sxs-lookup"><span data-stu-id="bc4b7-105">The following class definition is an example of a derived class that has class qualifiers.</span></span>

``` syntax
[Dynamic, Provider ("ProviderX")] 
class MyDerivedClass : MyClass
{
    [key] string sKey;
    [Implemented] sint32 ValueMethod();
    [Implemented] sint32 MyMethod ([in, Id(0)] sint32 Param);
};
```

<span data-ttu-id="bc4b7-106">Les qualificateurs peuvent être divisés en qualificateurs standard, qualificateurs CIM et qualificateurs uniques :</span><span class="sxs-lookup"><span data-stu-id="bc4b7-106">Qualifiers can be divided into standard qualifiers, CIM qualifiers, and unique qualifiers include the following:</span></span>

-   <span data-ttu-id="bc4b7-107">Qualificateur standard</span><span class="sxs-lookup"><span data-stu-id="bc4b7-107">Standard qualifier</span></span>

    <span data-ttu-id="bc4b7-108">Un qualificateur standard est un qualificateur défini par WMI et couramment utilisé dans le code MOF.</span><span class="sxs-lookup"><span data-stu-id="bc4b7-108">A standard qualifier is a qualifier defined by WMI and commonly used in MOF code.</span></span> <span data-ttu-id="bc4b7-109">Par exemple, les qualificateurs [**Dynamic**](dynamic-qualifier.md) et [**Read**](standard-qualifiers.md) sont à la fois des qualificateurs standard.</span><span class="sxs-lookup"><span data-stu-id="bc4b7-109">For example, the [**Dynamic**](dynamic-qualifier.md) and [**Read**](standard-qualifiers.md) qualifiers are both standard qualifiers.</span></span> <span data-ttu-id="bc4b7-110">Pour plus d’informations, consultez [qualificateurs WMI](wmi-qualifiers.md).</span><span class="sxs-lookup"><span data-stu-id="bc4b7-110">For more information, see [WMI Qualifiers](wmi-qualifiers.md).</span></span>

-   <span data-ttu-id="bc4b7-111">Qualificateur CIM</span><span class="sxs-lookup"><span data-stu-id="bc4b7-111">CIM qualifier</span></span>

    <span data-ttu-id="bc4b7-112">Un qualificateur CIM est un qualificateur inclus dans la spécification CIM.</span><span class="sxs-lookup"><span data-stu-id="bc4b7-112">A CIM qualifier is a qualifier included in the CIM specification.</span></span> <span data-ttu-id="bc4b7-113">Si vous utilisez des qualificateurs CIM dans du code MOF, les qualificateurs standard sont conçus spécifiquement avec WMI à l’esprit.</span><span class="sxs-lookup"><span data-stu-id="bc4b7-113">While use CIM qualifiers in MOF code, the standard qualifiers are designed specifically with WMI in mind.</span></span> <span data-ttu-id="bc4b7-114">Pour plus d’informations, consultez la [spécification CIM](https://www.dmtf.org/spec/cims.html/)de la DMTF.</span><span class="sxs-lookup"><span data-stu-id="bc4b7-114">For more information, see the DMTF [CIM Specification](https://www.dmtf.org/spec/cims.html/).</span></span>

-   <span data-ttu-id="bc4b7-115">Qualificateur unique</span><span class="sxs-lookup"><span data-stu-id="bc4b7-115">Unique qualifier</span></span>

    <span data-ttu-id="bc4b7-116">Un qualificateur unique est un qualificateur défini spécifiquement pour une nouvelle classe par un fournisseur de classe.</span><span class="sxs-lookup"><span data-stu-id="bc4b7-116">A unique qualifier is a qualifier defined specifically for a new class by a class provider.</span></span> <span data-ttu-id="bc4b7-117">Par exemple, le qualificateur [**Units**](standard-qualifiers.md) est un qualificateur non standard, spécifique au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="bc4b7-117">For example, the [**Units**](standard-qualifiers.md) qualifier is a nonstandard, provider-specific qualifier.</span></span> <span data-ttu-id="bc4b7-118">Vous pouvez créer vos propres qualificateurs à utiliser avec votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="bc4b7-118">You can create your own qualifiers for use with your provider.</span></span> <span data-ttu-id="bc4b7-119">Pour plus d’informations sur la création d’un fournisseur, consultez [développement d’un fournisseur WMI](developing-a-wmi-provider.md).</span><span class="sxs-lookup"><span data-stu-id="bc4b7-119">For more information about creating a provider, see [Developing a WMI Provider](developing-a-wmi-provider.md).</span></span>

<span data-ttu-id="bc4b7-120">Quel que soit votre qualificateur, le processus principal que vous effectuez consiste à utiliser le qualificateur dans votre code MOF.</span><span class="sxs-lookup"><span data-stu-id="bc4b7-120">Whatever your qualifier does, the main process you perform is to use the qualifier in your MOF code.</span></span> <span data-ttu-id="bc4b7-121">Pour plus d’informations, consultez [application d’un qualificateur](applying-a-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="bc4b7-121">For more information, see [Applying a Qualifier](applying-a-qualifier.md).</span></span> <span data-ttu-id="bc4b7-122">Vous pouvez décrire plus en détail un qualificateur avec une version de qualificateur.</span><span class="sxs-lookup"><span data-stu-id="bc4b7-122">You can further describe a qualifier with a qualifier flavor.</span></span> <span data-ttu-id="bc4b7-123">Une version de qualificateur contient plus d’informations sur la façon dont un fournisseur doit utiliser un qualificateur.</span><span class="sxs-lookup"><span data-stu-id="bc4b7-123">A qualifier flavor contains more information regarding how a provider should use a qualifier.</span></span> <span data-ttu-id="bc4b7-124">Pour plus d’informations, consultez [Description d’un qualificateur avec une version de qualificateur](describing-a-qualifier-with-a-qualifier-flavor.md).</span><span class="sxs-lookup"><span data-stu-id="bc4b7-124">For more information, see [Describing a Qualifier with a Qualifier Flavor](describing-a-qualifier-with-a-qualifier-flavor.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc4b7-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bc4b7-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc4b7-126">Conception de classes format MOF (MOF)</span><span class="sxs-lookup"><span data-stu-id="bc4b7-126">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



