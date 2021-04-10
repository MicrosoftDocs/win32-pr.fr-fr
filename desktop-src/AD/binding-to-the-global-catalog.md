---
title: Liaison au catalogue global
description: Le catalogue global est un espace de noms qui contient des données d’annuaire pour tous les domaines d’une forêt.
ms.assetid: c3c131c7-d9dd-4dbd-a909-abd0ffd9f375
ms.tgt_platform: multiple
keywords:
- Liaison à l’AD du catalogue global
- AD du catalogue global, liaison à
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08fe40b944130f66617b0c111b361ca51cbef126
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104031051"
---
# <a name="binding-to-the-global-catalog"></a><span data-ttu-id="65479-105">Liaison au catalogue global</span><span class="sxs-lookup"><span data-stu-id="65479-105">Binding to the Global Catalog</span></span>

<span data-ttu-id="65479-106">Le catalogue global est un espace de noms qui contient des données d’annuaire pour tous les domaines d’une forêt.</span><span class="sxs-lookup"><span data-stu-id="65479-106">The Global Catalog is a namespace that contains directory data for all domains in a forest.</span></span> <span data-ttu-id="65479-107">Le catalogue global contient un réplica partiel de chaque répertoire de domaine.</span><span class="sxs-lookup"><span data-stu-id="65479-107">The Global Catalog contains a partial replica of every domain directory.</span></span> <span data-ttu-id="65479-108">Elle contient une entrée pour chaque objet de la forêt d’entreprise, mais elle ne contient pas toutes les propriétés de chaque objet.</span><span class="sxs-lookup"><span data-stu-id="65479-108">It contains an entry for every object in the enterprise forest, but does not contain all the properties of each object.</span></span> <span data-ttu-id="65479-109">Au lieu de cela, elle contient uniquement les propriétés spécifiées pour l’inclusion dans le catalogue global.</span><span class="sxs-lookup"><span data-stu-id="65479-109">Instead, it contains only the properties specified for inclusion in the Global Catalog.</span></span>

<span data-ttu-id="65479-110">Le catalogue global est stocké sur des serveurs spécifiques au sein de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="65479-110">The Global Catalog is stored on specific servers throughout the enterprise.</span></span> <span data-ttu-id="65479-111">Seuls les contrôleurs de domaine peuvent servir de serveurs de catalogue global.</span><span class="sxs-lookup"><span data-stu-id="65479-111">Only domain controllers can serve as Global Catalog servers.</span></span> <span data-ttu-id="65479-112">Les administrateurs indiquent si un contrôleur de domaine donné contient un catalogue global à l’aide du gestionnaire de sites et de services Active Directory.</span><span class="sxs-lookup"><span data-stu-id="65479-112">Administrators indicate whether a given domain controller holds a Global Catalog by using the Active Directory Sites and Services Manager.</span></span>

<span data-ttu-id="65479-113">Pour effectuer une liaison au catalogue global avec ADSI, utilisez le moniker « GC : ».</span><span class="sxs-lookup"><span data-stu-id="65479-113">To bind to the Global Catalog with ADSI, use the "GC:" moniker.</span></span>

<span data-ttu-id="65479-114">Il existe deux façons de lier le catalogue global pour effectuer une recherche dans une forêt :</span><span class="sxs-lookup"><span data-stu-id="65479-114">There are two ways to bind to the Global Catalog to perform a search in a forest:</span></span>

-   <span data-ttu-id="65479-115">Établissez une liaison avec l’objet racine d’entreprise pour effectuer une recherche dans tous les domaines de la forêt.</span><span class="sxs-lookup"><span data-stu-id="65479-115">Bind to the enterprise root object to search across all domains in the forest.</span></span>
-   <span data-ttu-id="65479-116">Effectuer une liaison à un objet spécifique pour rechercher cet objet et ses enfants.</span><span class="sxs-lookup"><span data-stu-id="65479-116">Bind to a specific object to search that object and its children.</span></span> <span data-ttu-id="65479-117">Par exemple, si vous établissez une liaison à un domaine qui a deux domaines sous celui-ci dans une arborescence de domaine de la forêt, vous pouvez effectuer une recherche dans ces trois domaines.</span><span class="sxs-lookup"><span data-stu-id="65479-117">For example, if you bind to a domain that has two domains beneath it in a domain tree in the forest, you can search across those three domains.</span></span> <span data-ttu-id="65479-118">N’oubliez pas que le nom unique de l’objet à lier est exactement le même que le nom unique utilisé pour la liaison à l’espace de noms « LDAP : ».</span><span class="sxs-lookup"><span data-stu-id="65479-118">Be aware that the distinguished name for the object to bind to is exactly the same as the distinguished name used to bind to the "LDAP:" namespace.</span></span> <span data-ttu-id="65479-119">Rappelez-vous que « LDAP : » est un réplica complet d’un domaine unique et que « GC : » est un réplica partiel de tous les domaines de la forêt.</span><span class="sxs-lookup"><span data-stu-id="65479-119">Recall that "LDAP:" is a full replica of a single domain and that "GC:" is a partial replica of all domains in the forest.</span></span>

<span data-ttu-id="65479-120">Comme avec le moniker « LDAP : », vous pouvez utiliser une liaison sans serveur ou établir une liaison avec un serveur de catalogue global spécifique.</span><span class="sxs-lookup"><span data-stu-id="65479-120">As with the "LDAP:" moniker, you can use serverless binding or bind to a specific Global Catalog server.</span></span> <span data-ttu-id="65479-121">Si vous recherchez dans la forêt Active, utilisez une liaison sans serveur.</span><span class="sxs-lookup"><span data-stu-id="65479-121">If searching in the current forest, use serverless binding.</span></span> <span data-ttu-id="65479-122">Toutefois, si vous effectuez une recherche dans une autre forêt, spécifiez un nom de domaine ou un serveur de catalogue global à lier, comme illustré dans les exemples suivants.</span><span class="sxs-lookup"><span data-stu-id="65479-122">However, if searching in another forest, specify either a domain name or a Global Catalog server to bind to, such as shown in the following examples.</span></span>

<span data-ttu-id="65479-123">Liez à l’aide du nom de domaine :</span><span class="sxs-lookup"><span data-stu-id="65479-123">Bind using the domain name:</span></span>

``` syntax
GC://fabrikam.com
```

<span data-ttu-id="65479-124">Liez à l’aide du nom du serveur :</span><span class="sxs-lookup"><span data-stu-id="65479-124">Bind using the server name:</span></span>

``` syntax
GC://servername
```

<span data-ttu-id="65479-125">Vous pouvez également effectuer une liaison à un objet spécifique dans le catalogue global.</span><span class="sxs-lookup"><span data-stu-id="65479-125">You can also bind to a specific object within the Global Catalog.</span></span> <span data-ttu-id="65479-126">Pour effectuer une liaison à l’objet Sales dans le domaine fabrikam, utilisez le format suivant.</span><span class="sxs-lookup"><span data-stu-id="65479-126">To bind to the sales object in the fabrikam domain, use the following format.</span></span>

``` syntax
GC://fabrikam.com/DC=sales,DC=fabrikam,DC=com
```

<span data-ttu-id="65479-127">Ou, pour effectuer une liaison à l’objet Sales sur le serveur, utilisez le format suivant.</span><span class="sxs-lookup"><span data-stu-id="65479-127">Or, to bind to the sales object on the server, use the following format.</span></span>

``` syntax
GC://servername.fabrikam.com/DC=sales,DC=fabrikam,DC=com
```

<span data-ttu-id="65479-128">**Pour effectuer une recherche dans l’ensemble de la forêt**</span><span class="sxs-lookup"><span data-stu-id="65479-128">**To search the entire forest**</span></span>

1.  <span data-ttu-id="65479-129">Liez à la racine de l’espace de noms de catalogue global.</span><span class="sxs-lookup"><span data-stu-id="65479-129">Bind to the root of the Global Catalog namespace.</span></span>
2.  <span data-ttu-id="65479-130">Énumérez le conteneur de catalogue global.</span><span class="sxs-lookup"><span data-stu-id="65479-130">Enumerate the Global Catalog container.</span></span> <span data-ttu-id="65479-131">Le conteneur de catalogue global contient un seul objet que vous pouvez utiliser pour effectuer une recherche dans l’ensemble de la forêt.</span><span class="sxs-lookup"><span data-stu-id="65479-131">The Global Catalog container contains a single object that you can use to search the entire forest.</span></span>
3.  <span data-ttu-id="65479-132">Utilisez l’objet dans le conteneur pour effectuer la recherche.</span><span class="sxs-lookup"><span data-stu-id="65479-132">Use the object in the container to perform the search.</span></span> <span data-ttu-id="65479-133">En C/C++, appelez [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour recevoir un pointeur [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) sur l’objet afin de pouvoir utiliser l’interface **IDirectorySearch** pour effectuer la recherche.</span><span class="sxs-lookup"><span data-stu-id="65479-133">In C/C++, call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to get an [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) pointer on the object so that you can use the **IDirectorySearch** interface to perform the search.</span></span> <span data-ttu-id="65479-134">Dans Visual Basic, utilisez l’objet retourné par l’énumération dans votre requête ADO.</span><span class="sxs-lookup"><span data-stu-id="65479-134">In Visual Basic, use the object returned from the enumeration in your ADO query.</span></span>

<span data-ttu-id="65479-135">Pour énumérer les serveurs de catalogue global d’un site, effectuez une recherche de sous-arborescence LDAP de « CN = <yoursite> , CN = sites <DN of the configurationNamingContext> », à l’aide de la chaîne de filtrage suivante.</span><span class="sxs-lookup"><span data-stu-id="65479-135">To enumerate the Global Catalog servers in a site, perform an LDAP subtree search of "cn=<yoursite>,cn=sites,<DN of the configurationNamingContext>", using the following filter string.</span></span>

``` syntax
(&(objectCategory=nTDSDSA)(options:1.2.840.113556.1.4.803:=1))
```

<span data-ttu-id="65479-136">Ce filtre utilise le **\_ bit de règle de correspondance LDAP \_ \_ \_ et** l’opérateur de règle de correspondance (1.2.840.113556.1.4.803) pour rechercher les objets **nTDSDSA** dont le bit de poids faible est défini dans le masque de bits de l’attribut **options** .</span><span class="sxs-lookup"><span data-stu-id="65479-136">This filter uses the **LDAP\_MATCHING\_RULE\_BIT\_AND** matching rule operator (1.2.840.113556.1.4.803) to find **nTDSDSA** objects that have the low-order bit set in the bitmask of the **options** attribute.</span></span> <span data-ttu-id="65479-137">Le bit de poids faible, qui correspond à la constante de la valeur de l’option **nTDSDSA \_ OPT \_ is \_ GC** constant définie dans ntdsapi. h, identifie l’objet **nTDSDSA** d’un serveur de catalogue global.</span><span class="sxs-lookup"><span data-stu-id="65479-137">The low-order bit, which corresponds to the **NTDSDSA\_OPT\_IS\_GC** constant defined in Ntdsapi.h, identifies the **nTDSDSA** object of a Global Catalog server.</span></span> <span data-ttu-id="65479-138">Pour plus d’informations sur les règles de correspondance, consultez [syntaxe de filtre de recherche](/windows/desktop/ADSI/search-filter-syntax).</span><span class="sxs-lookup"><span data-stu-id="65479-138">For more information about matching rules, see [Search Filter Syntax](/windows/desktop/ADSI/search-filter-syntax).</span></span>

<span data-ttu-id="65479-139">Le parent de l’objet **nTDSDSA** est l’objet serveur et la propriété **dNSHostName** de l’objet Server est le nom DNS du serveur de catalogue global.</span><span class="sxs-lookup"><span data-stu-id="65479-139">The parent of the **nTDSDSA** object is the server object, and the **dNSHostName** property of the server object is the DNS name of the Global Catalog server.</span></span>

<span data-ttu-id="65479-140">Vous ne pouvez pas utiliser \# définir des constantes telles que **nTDSDSA \_ OPT \_ est \_** un **bit de règle de correspondance LDAP et LDAP \_ \_ \_ \_ et** directement dans une chaîne de filtre de recherche.</span><span class="sxs-lookup"><span data-stu-id="65479-140">You cannot use \#define constants such as **NTDSDSA\_OPT\_IS\_GC** and **LDAP\_MATCHING\_RULE\_BIT\_AND** directly in a search filter string.</span></span> <span data-ttu-id="65479-141">Toutefois, vous pouvez utiliser ces constantes comme arguments d’une fonction telle que [**swprintf \_ s**](/windows/win32/api/winuser/nf-winuser-wsprintfa) pour insérer les valeurs de constante dans une chaîne de filtrage.</span><span class="sxs-lookup"><span data-stu-id="65479-141">However, you could use these constants as arguments to a function such as [**swprintf\_s**](/windows/win32/api/winuser/nf-winuser-wsprintfa) to insert the constant values into a filter string.</span></span>

<span data-ttu-id="65479-142">Le catalogue global ne représente pas l’intégralité de l’arborescence de la forêt.</span><span class="sxs-lookup"><span data-stu-id="65479-142">The global catalog does not represent the entire forest tree structure.</span></span> <span data-ttu-id="65479-143">Par exemple, vous pouvez vous attendre à ce que l’exemple de code suivant énumère tous les domaines de la forêt et tous les objets enfants de chaque domaine.</span><span class="sxs-lookup"><span data-stu-id="65479-143">For example, you might expect that the following code example would enumerate all of the domains in the forest and all child objects of each domain.</span></span> <span data-ttu-id="65479-144">En réalité, ce qu’il fait, c’est d’énumérer tous les domaines de la forêt, mais aucun des objets de domaine énumérés ne contient d’enfants.</span><span class="sxs-lookup"><span data-stu-id="65479-144">In reality, what it actually does is enumerate all of the domains in the forest, but none of the enumerated domain objects contain any children.</span></span> <span data-ttu-id="65479-145">Il s’agit d’une limitation du catalogue global.</span><span class="sxs-lookup"><span data-stu-id="65479-145">This is a limitation of the global catalog.</span></span>


```VB
Dim oGC As IADs
Dim oDomain As IADs
Dim oChild As IADs

Set oGC = GetObject("GC:")
For Each oDomain In oGC
    ' Print the name of the domain.
    Debug.Print oDomain.Name
    
    ' Enumerate the child objects of the domain.
    For Each oChild In oDomain
        Debug.Print oChild.Name
    Next
Next
```



<span data-ttu-id="65479-146">Pour résoudre ce cas, il est nécessaire de lier à chaque objet de domaine, puis d’énumérer les objets enfants de chaque domaine.</span><span class="sxs-lookup"><span data-stu-id="65479-146">To correct this, it is necessary to bind to each domain object and then enumerate the child objects of each domain.</span></span> <span data-ttu-id="65479-147">La technique appropriée est présentée dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="65479-147">The proper technique is shown in the following code example.</span></span>


```VB
Dim oGC As IADs
Dim oDomainEnum As IADs
Dim oDomainBind As IADs
Dim oChild As IADs

Set oGC = GetObject("GC:")
For Each oDomainEnum In oGC
    ' Print the name of the domain.
    Debug.Print oDomainEnum.Name
    
    ' Bind to the domain.
    Set oDomainBind = GetObject("LDAP://" + oDomainEnum.Name)
    
    ' Enumerate the child objects of the domain.
    For Each oChild In oDomainBind
        Debug.Print oChild.Name
    Next
Next
```



<span data-ttu-id="65479-148">Pour plus d’informations et des exemples de code qui montrent comment effectuer une recherche dans une forêt entière, consultez l' [exemple de code pour la recherche d’une forêt](example-code-for-searching-a-forest.md).</span><span class="sxs-lookup"><span data-stu-id="65479-148">For more information and code examples that show how to search an entire forest, see [Example Code for Searching a Forest](example-code-for-searching-a-forest.md).</span></span>

 

 