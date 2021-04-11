---
title: Détermination d’un type d’attribut
description: L’attribut systemFlags d’un objet attributeSchema contient un ensemble d’indicateurs qui indiquent différentes qualités de l’objet attribut, par exemple si l’attribut est construit ou non répliqué.
ms.assetid: 58f44ea4-ecbd-4650-b366-37b05a975c68
ms.tgt_platform: multiple
keywords:
- Détermination d’une publicité de type d’attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b64b4d8b0ae5d6cbac38c9c44ed8e4a7aa5d5f57
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104031018"
---
# <a name="determining-an-attribute-type"></a><span data-ttu-id="08f15-104">Détermination d’un type d’attribut</span><span class="sxs-lookup"><span data-stu-id="08f15-104">Determining an Attribute Type</span></span>

<span data-ttu-id="08f15-105">L’attribut [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) d’un objet [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) contient un ensemble d’indicateurs qui indiquent différentes qualités de l’objet attribut, par exemple si l’attribut est construit ou non répliqué.</span><span class="sxs-lookup"><span data-stu-id="08f15-105">The [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) attribute of an [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) object contains a set of flags that indicate various qualities of the attribute object, such as whether the attribute is constructed or non-replicated.</span></span> <span data-ttu-id="08f15-106">Le tableau suivant répertorie les indicateurs de l’attribut **systemFlags** qui affectent le type de stockage de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="08f15-106">The following table lists the flags of the **systemFlags** attribute that affect the storage type of the attribute.</span></span> 

| <span data-ttu-id="08f15-107">Valeur d’indicateur</span><span class="sxs-lookup"><span data-stu-id="08f15-107">Flag value</span></span> | <span data-ttu-id="08f15-108">Description</span><span class="sxs-lookup"><span data-stu-id="08f15-108">Description</span></span>                                                                                                          |
|------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08f15-109">0x00000001</span><span class="sxs-lookup"><span data-stu-id="08f15-109">0x00000001</span></span> | <span data-ttu-id="08f15-110">Si cet indicateur est présent dans l’attribut [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) , l’attribut n’est pas répliqué.</span><span class="sxs-lookup"><span data-stu-id="08f15-110">If this flag is present in the [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) attribute, the attribute is not replicated.</span></span> |
| <span data-ttu-id="08f15-111">0x00000004</span><span class="sxs-lookup"><span data-stu-id="08f15-111">0x00000004</span></span> | <span data-ttu-id="08f15-112">Si cet indicateur est présent dans l’attribut [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) , l’attribut est construit.</span><span class="sxs-lookup"><span data-stu-id="08f15-112">If this flag is present in the [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) attribute, the attribute is constructed.</span></span>    |



 

<span data-ttu-id="08f15-113">Il est possible de construire une chaîne de requête qui peut être utilisée pour interroger des attributs construits ou non répliqués.</span><span class="sxs-lookup"><span data-stu-id="08f15-113">It is possible to construct a query string that can be used to query for constructed or non-replicated attributes.</span></span> <span data-ttu-id="08f15-114">Par exemple, la chaîne de requête suivante recherche tous les objets [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) non répliqués.</span><span class="sxs-lookup"><span data-stu-id="08f15-114">For example, the following query string finds all non-replicated [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) objects.</span></span> <span data-ttu-id="08f15-115">Sachez que la chaîne de requête requiert l’équivalent décimal de la valeur, et non l’équivalent hexadécimal de la valeur.</span><span class="sxs-lookup"><span data-stu-id="08f15-115">Be aware that the query string requires the decimal equivalent of the value, not the hexadecimal equivalent of the value.</span></span> <span data-ttu-id="08f15-116">Pour plus d’informations sur l’OID de règle de correspondance utilisé par cette chaîne de requête, consultez [comment spécifier des valeurs de comparaison](how-to-specify-comparison-values.md).</span><span class="sxs-lookup"><span data-stu-id="08f15-116">For more information about the matching rule OID used by this query string, see [How to Specify Comparison Values](how-to-specify-comparison-values.md).</span></span>


```C++
(&(objectCategory=attributeSchema)(systemFlags:1.2.840.113556.1.4.804:=1))
```



<span data-ttu-id="08f15-117">L’attribut [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) de l’objet [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) de chaque attribut définit si un attribut est indexé ; un attribut indexé a la valeur 1, un attribut non indexé a la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="08f15-117">The [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) attribute of each attribute's [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) object defines whether an attribute is indexed; an indexed attribute has a value of 1, a non-indexed attribute has a value of 0.</span></span> <span data-ttu-id="08f15-118">Par exemple, la chaîne de requête suivante recherche les objets **attributeSchema** représentant les attributs indexés.</span><span class="sxs-lookup"><span data-stu-id="08f15-118">For example, the following query string finds the **attributeSchema** objects representing indexed attributes.</span></span>


```C++
(&(objectCategory=attributeSchema)(searchFlags=1))
```



<span data-ttu-id="08f15-119">L’attribut [**isMemberOfPartialAttributeSet**](/windows/desktop/ADSchema/a-ismemberofpartialattributeset) de l’objet [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) de chaque attribut définit si un attribut est répliqué dans le catalogue global.</span><span class="sxs-lookup"><span data-stu-id="08f15-119">The [**isMemberOfPartialAttributeSet**](/windows/desktop/ADSchema/a-ismemberofpartialattributeset) attribute of each attribute's [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) object defines whether an attribute is replicated to the global catalog.</span></span> <span data-ttu-id="08f15-120">Cet attribut a la valeur **true** si l’attribut est membre du catalogue global ou **false** si les attributs ne se trouvent pas dans le catalogue global.</span><span class="sxs-lookup"><span data-stu-id="08f15-120">This attribute has a value of **TRUE** if the attribute is a member of the global catalog or **FALSE** if the attributes is not in the global catalog.</span></span> <span data-ttu-id="08f15-121">Par exemple, la chaîne de requête suivante recherche les objets **attributeSchema** répliqués dans le catalogue global.</span><span class="sxs-lookup"><span data-stu-id="08f15-121">For example, the following query string searches the **attributeSchema** objects that are replicated to the global catalog.</span></span>


```C++
(&(objectCategory=attributeSchema)(isMemberOfPartialAttributeSet=TRUE))
```



 

 