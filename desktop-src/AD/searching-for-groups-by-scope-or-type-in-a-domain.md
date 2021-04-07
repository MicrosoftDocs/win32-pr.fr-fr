---
title: Recherche de groupes par portée ou par type dans un domaine
description: Dans les domaines Windows 2000, il existe une seule classe appelée groupe pour toutes les étendues de groupe (domaine local, global, universel) et types (sécurité, distribution).
ms.assetid: e32629d9-aa62-4953-aa49-43af726b7deb
ms.tgt_platform: multiple
keywords:
- Recherche de groupes par étendue ou type dans un domaine AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ee9aae5e2c7be7b9cba590f9bc80f0517bca918
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724428"
---
# <a name="searching-for-groups-by-scope-or-type-in-a-domain"></a><span data-ttu-id="4edf8-104">Recherche de groupes par portée ou par type dans un domaine</span><span class="sxs-lookup"><span data-stu-id="4edf8-104">Searching for Groups by Scope or Type in a Domain</span></span>

<span data-ttu-id="4edf8-105">Dans les domaines Windows 2000, il existe une seule classe appelée [**groupe**](/windows/desktop/ADSchema/c-group) pour toutes les étendues de groupe (domaine local, global, universel) et types (sécurité, distribution).</span><span class="sxs-lookup"><span data-stu-id="4edf8-105">In Windows 2000 domains, there is single class called [**group**](/windows/desktop/ADSchema/c-group) for all group scopes (Domain Local, Global, Universal) and types (security, distribution).</span></span> <span data-ttu-id="4edf8-106">L’attribut [**GroupType**](/windows/desktop/ADSchema/a-grouptype) de l’objet Group spécifie le type de groupe et l’étendue.</span><span class="sxs-lookup"><span data-stu-id="4edf8-106">The [**groupType**](/windows/desktop/ADSchema/a-grouptype) attribute of the group object specifies the group type and scope.</span></span>

<span data-ttu-id="4edf8-107">Pour utiliser le type ou l’étendue pour rechercher des groupes sur les domaines Windows 2000, utilisez un filtre qui contient une règle de correspondance pour l’attribut [**GroupType**](/windows/desktop/ADSchema/a-grouptype) .</span><span class="sxs-lookup"><span data-stu-id="4edf8-107">To use type or scope to search for groups on Windows 2000 domains, use a filter that contains a matching rule for the [**groupType**](/windows/desktop/ADSchema/a-grouptype) attribute.</span></span> <span data-ttu-id="4edf8-108">Pour plus d’informations sur les règles de correspondance, consultez [syntaxe de filtre de recherche](/windows/desktop/ADSI/search-filter-syntax).</span><span class="sxs-lookup"><span data-stu-id="4edf8-108">For more information about matching rules, see [Search Filter Syntax](/windows/desktop/ADSI/search-filter-syntax).</span></span>

<span data-ttu-id="4edf8-109">Pour plus d’informations et pour obtenir un exemple de code qui montre comment rechercher des groupes dans un domaine, consultez l' [exemple de code pour rechercher des groupes dans un domaine](example-code-for-performing-a-query-in-a-domain.md).</span><span class="sxs-lookup"><span data-stu-id="4edf8-109">For more information and a code example that shows how to search for groups in a domain, see [Example Code for Searching for Groups in a Domain](example-code-for-performing-a-query-in-a-domain.md).</span></span>

## <a name="example-ldap-query-strings"></a><span data-ttu-id="4edf8-110">Exemples de chaînes de requête LDAP</span><span class="sxs-lookup"><span data-stu-id="4edf8-110">Example LDAP Query Strings</span></span>

<span data-ttu-id="4edf8-111">Les exemples de chaînes de requête suivants montrent comment construire une chaîne de requête LDAP utilisée pour rechercher ou filtrer des types de groupes spécifiques.</span><span class="sxs-lookup"><span data-stu-id="4edf8-111">The following query string examples show how to construct an LDAP query string used to search for or filter specific group types.</span></span>

<span data-ttu-id="4edf8-112">La chaîne de requête suivante recherche des groupes de sécurité.</span><span class="sxs-lookup"><span data-stu-id="4edf8-112">The following query string will search for security groups.</span></span> <span data-ttu-id="4edf8-113">Cet exemple utilise « -2147483648 » comme équivalent décimal de l’indicateur **de \_ sécurité de type groupe ADS \_ \_ \_ activé** .</span><span class="sxs-lookup"><span data-stu-id="4edf8-113">This example uses "-2147483648" as the decimal equivalent of the **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** flag.</span></span>


```C++
(&(objectCategory=group)(groupType:1.2.840.113556.1.4.803:=-2147483648))
```



<span data-ttu-id="4edf8-114">La chaîne de requête suivante recherche les groupes de distribution universels ; autrement dit, les groupes qui contiennent l’indicateur de **\_ \_ \_ \_ groupe universel du type de groupe ADS** et ne contiennent pas l’indicateur de sécurité de **\_ type groupe ADS \_ \_ \_ activé** .</span><span class="sxs-lookup"><span data-stu-id="4edf8-114">The following query string will search for universal distribution groups; that is, groups that contain the **ADS\_GROUP\_TYPE\_UNIVERSAL\_GROUP** flag and do not contain the **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** flag.</span></span> <span data-ttu-id="4edf8-115">Cet exemple utilise « 8 » comme équivalent décimal du type de groupe **ad \_ \_ \_ \_ groupe universel** et « -2147483648 » comme équivalent décimal du type de **\_ groupe ADS \_ \_ \_ activée** pour la sécurité.</span><span class="sxs-lookup"><span data-stu-id="4edf8-115">This example uses "8" as the decimal equivalent of **ADS\_GROUP\_TYPE\_UNIVERSAL\_GROUP** and "-2147483648" as the decimal equivalent of the **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** flag.</span></span>


```C++
(&(objectCategory=group)((&(groupType:1.2.840.113556.1.4.803:=8)(!(groupType:1.2.840.113556.1.4.803:=-2147483648)))))
```



 

 