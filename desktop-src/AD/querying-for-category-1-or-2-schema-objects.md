---
title: Interrogation des objets de schéma de catégorie 1 ou 2
description: L’attribut systemFlags des objets attributeSchema et classSchema est un masque de passe entier qui contient des indicateurs qui indiquent des qualités système supplémentaires de l’attribut ou de la classe.
ms.assetid: 5cc8f296-df3e-4643-9694-543f069a2cc7
ms.tgt_platform: multiple
keywords:
- Interrogation des objets de schéma de catégorie 1 ou 2 AD
- objet AD, interrogation des objets de schéma de catégorie 1 ou 2
- Active Directory de schéma, interrogation des objets de schéma de catégorie 1 ou 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c67b57821cbebc80b3b6e93d158bbb8af8f7103
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104314621"
---
# <a name="querying-for-category-1-or-2-schema-objects"></a><span data-ttu-id="743ed-106">Interrogation des objets de schéma de catégorie 1 ou 2</span><span class="sxs-lookup"><span data-stu-id="743ed-106">Querying for Category 1 or 2 Schema Objects</span></span>

<span data-ttu-id="743ed-107">L’attribut **systemFlags** des objets **attributeSchema** et **classSchema** est un masque de passe entier qui contient des indicateurs qui indiquent des qualités système supplémentaires de l’attribut ou de la classe.</span><span class="sxs-lookup"><span data-stu-id="743ed-107">The **systemFlags** attribute of **attributeSchema** and **classSchema** objects is an integer bitmask that contains flags that indicate additional system qualities of the attribute or class.</span></span> <span data-ttu-id="743ed-108">L’énumération d’énumérations [**\_ systemFlags \_ ADS**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) contient des valeurs qui correspondent aux bits que vous pouvez définir dans l’attribut **systemFlags** .</span><span class="sxs-lookup"><span data-stu-id="743ed-108">The [**ADS\_SYSTEMFLAG\_ENUM**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) enumeration contains values that correspond to the bits you can set in the **systemFlags** attribute.</span></span> <span data-ttu-id="743ed-109">Vous ne pouvez pas définir d’autres bits de **systemFlags** , tels que le bit 0x10, qui indique si l’attribut ou la classe est une catégorie 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="743ed-109">There are additional **systemFlags** bits that you cannot set, such as the 0x10 bit which indicates whether the attribute or class is category 1 or category 2.</span></span> <span data-ttu-id="743ed-110">Le bit 0x10 est défini pour les objets catégorie 1, qui sont les classes et les attributs inclus dans le schéma de base inclus dans le système.</span><span class="sxs-lookup"><span data-stu-id="743ed-110">The 0x10 bit is set for category 1 objects, which are the classes and attributes included in the base schema included with the system.</span></span> <span data-ttu-id="743ed-111">Le bit n’est pas défini pour les classes et les attributs de catégorie 2, qui sont des extensions du schéma.</span><span class="sxs-lookup"><span data-stu-id="743ed-111">The bit is not set for category 2 attributes and classes, which are extensions to the schema.</span></span> <span data-ttu-id="743ed-112">Si aucune propriété **systemFlags** n’existe sur un objet **attributeSchema** ou **classSchema** , il s’agit de la catégorie 2.</span><span class="sxs-lookup"><span data-stu-id="743ed-112">If no **systemFlags** property exists on an **attributeSchema** or **classSchema** object, it is category 2.</span></span>

<span data-ttu-id="743ed-113">Le **\_ bit de règle de correspondance LDAP \_ \_ \_ et** la règle de correspondance peuvent être utilisés pour rechercher des objets dont l’indicateur 0X10 est défini dans l’attribut **systemFlags** .</span><span class="sxs-lookup"><span data-stu-id="743ed-113">The **LDAP\_MATCHING\_RULE\_BIT\_AND** matching rule can be used to search for objects that have the 0x10 flag set in the **systemFlags** attribute.</span></span> <span data-ttu-id="743ed-114">Pour plus d’informations, consultez [syntaxe de filtre de recherche](/windows/desktop/ADSI/search-filter-syntax).</span><span class="sxs-lookup"><span data-stu-id="743ed-114">For more information, see [Search Filter Syntax](/windows/desktop/ADSI/search-filter-syntax).</span></span>

## <a name="querying-for-category-1"></a><span data-ttu-id="743ed-115">Interrogation de la catégorie 1</span><span class="sxs-lookup"><span data-stu-id="743ed-115">Querying for Category 1</span></span>

<span data-ttu-id="743ed-116">La chaîne de requête suivante recherche les attributs de catégorie 1 (objets **attributeSchema** avec le bit 0x10 défini dans la propriété **systemFlags** ).</span><span class="sxs-lookup"><span data-stu-id="743ed-116">The following query string searches for category 1 attributes (**attributeSchema** objects with the 0x10 bit set in the **systemFlags** property).</span></span>


```C++
(&(objectCategory=attributeSchema)(systemFlags:1.2.840.113556.1.4.803:=16) )
```



<span data-ttu-id="743ed-117">Sachez que, dans l’exemple ci-dessus, la syntaxe de requête LDAP requiert des valeurs décimales ; par conséquent, la valeur hexadécimale de l’indicateur doit être convertie en valeur décimale.</span><span class="sxs-lookup"><span data-stu-id="743ed-117">Be aware that, in the example above, the LDAP query syntax requires decimal values; therefore, the hex value of the flag must be converted to decimal.</span></span> <span data-ttu-id="743ed-118">Dans ce cas, la catégorie 1 bit est 0x10, de sorte que la valeur du filtre doit être spécifiée en tant que 16.</span><span class="sxs-lookup"><span data-stu-id="743ed-118">In this case, category 1 bit is 0x10 so the filter value must be specified as 16.</span></span>

## <a name="querying-for-category-2"></a><span data-ttu-id="743ed-119">Interrogation de la catégorie 2</span><span class="sxs-lookup"><span data-stu-id="743ed-119">Querying for Category 2</span></span>

<span data-ttu-id="743ed-120">La chaîne de requête suivante recherche les attributs de catégorie 2 (objets **attributeSchema** pour lesquels le bit 0x10 n’est pas défini dans la propriété **systemFlags** ).</span><span class="sxs-lookup"><span data-stu-id="743ed-120">The following query string searches for category 2 attributes (**attributeSchema** objects that do not have the 0x10 bit set in the **systemFlags** property).</span></span>


```C++
(&(objectCategory=attributeSchema)(!(systemFlags:1.2.840.113556.1.4.803:=16)))
```



<span data-ttu-id="743ed-121">Sachez que cette requête retourne également des objets **attributeSchema** qui n’ont pas de propriété **systemFlags** et, par conséquent, n’ont pas l’indicateur spécifié défini.</span><span class="sxs-lookup"><span data-stu-id="743ed-121">Be aware that this query also returns **attributeSchema** objects that do not have a **systemFlags** property, and, therefore, implicitly do not have the specified flag set.</span></span>

 

 