---
description: Le qualificateur ViewSpaces définit les noms et l’emplacement des espaces de noms où se trouvent les instances source. Vous pouvez spécifier n’importe quelle combinaison d’espaces de noms sur des ordinateurs locaux ou distants.
ms.assetid: 15d71bb6-842d-4f5a-b2e3-e9f60f0aea3b
ms.tgt_platform: multiple
title: Qualificateur ViewSpaces
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ViewSpaces
api_type:
- NA
api_location: ''
ms.openlocfilehash: 683f5596497f3c1e1ad0f2b85eaaa1460177a0ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210538"
---
# <a name="viewspaces-qualifier"></a><span data-ttu-id="8dd4b-104">Qualificateur ViewSpaces</span><span class="sxs-lookup"><span data-stu-id="8dd4b-104">ViewSpaces Qualifier</span></span>

<span data-ttu-id="8dd4b-105">Le **qualificateur ViewSpaces** définit les noms et l’emplacement des espaces de noms où se trouvent les instances source.</span><span class="sxs-lookup"><span data-stu-id="8dd4b-105">The **ViewSpaces qualifier** defines the names and location of the namespaces where the source instances are located.</span></span> <span data-ttu-id="8dd4b-106">Vous pouvez spécifier n’importe quelle combinaison d’espaces de noms sur des ordinateurs locaux ou distants.</span><span class="sxs-lookup"><span data-stu-id="8dd4b-106">You can specify any combination of namespaces on local or remote computers.</span></span>

<span data-ttu-id="8dd4b-107">L’exemple suivant répertorie deux espaces de noms sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="8dd4b-107">The following example lists two namespaces on the local computer.</span></span>


```mof
ViewSpaces{"\\\\.\\root\\LocalNamespace",
     "\\\\.\\root\\RemoteNamespace"}
```



<span data-ttu-id="8dd4b-108">Le [fournisseur de vues](view-provider.md) met en correspondance les requêtes sources du [qualificateur ViewSources](viewsources-qualifier.md) avec les espaces de noms répertoriés dans le qualificateur **ViewSpaces** dans l’ordre dans lequel les requêtes et les espaces de noms sont répertoriés.</span><span class="sxs-lookup"><span data-stu-id="8dd4b-108">The [View provider](view-provider.md) matches the source queries in the [ViewSources qualifier](viewsources-qualifier.md) to the namespaces listed in the **ViewSpaces** qualifier in the order the queries and namespaces are listed.</span></span> <span data-ttu-id="8dd4b-109">Normalement, il existe une relation un-à-un entre le nombre d’espaces de noms figurant dans le qualificateur **ViewSpaces** et les requêtes listées dans le qualificateur **ViewSources** .</span><span class="sxs-lookup"><span data-stu-id="8dd4b-109">Normally, there is a one-to-one relationship between the number of namespaces listed in the **ViewSpaces** qualifier and the queries listed in the **ViewSources** qualifier.</span></span> <span data-ttu-id="8dd4b-110">Dans certains cas, vous souhaiterez peut-être que les requêtes listées dans le qualificateur ViewSources s’exécutent sur deux espaces de noms ou plus.</span><span class="sxs-lookup"><span data-stu-id="8dd4b-110">In some cases, you may want the queries listed in the ViewSources qualifier to execute against two or more namespaces.</span></span> <span data-ttu-id="8dd4b-111">Vous pouvez utiliser un double deux-points «  :: » pour séparer plusieurs espaces de noms qui seront évalués par l’une des requêtes dans le tableau **ViewSources** .</span><span class="sxs-lookup"><span data-stu-id="8dd4b-111">You can use a double colon "::" to separate multiple namespaces that will be evaluated by one of the queries in the **ViewSources** array.</span></span>

<span data-ttu-id="8dd4b-112">Dans l’exemple suivant, la première requête du tableau [**ViewSources**](viewsources-qualifier.md) est exécutée sur l’espace de noms dans la première paire de guillemets, la deuxième requête sur les trois espaces de noms dans la deuxième paire de guillemets, et la troisième pour les deux espaces de noms dans la troisième paire de guillemets.</span><span class="sxs-lookup"><span data-stu-id="8dd4b-112">In the following example, the first query in the [**ViewSources**](viewsources-qualifier.md) array will be run against the namespace in the first pair of quotes, the second query against the three namespaces in the second pair of quotes, and the third query against the two namespaces in the third pair of quotes.</span></span>


```mof
ViewSpaces
    {
    "\\\\.\\root\\LocalNamespace",

    "\\\\.\\root\\RemoteNamespace1::
        \\\\.\\root\\RemoteNamespace2::
        \\\\.\\root\\RemoteNamespace3",

    "\\\\.\\root\\RemoteNamespace1::
        \\\\.\\root\\RemoteNamespace3"
    }
```



## <a name="requirements"></a><span data-ttu-id="8dd4b-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8dd4b-113">Requirements</span></span>



| <span data-ttu-id="8dd4b-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8dd4b-114">Requirement</span></span> | <span data-ttu-id="8dd4b-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="8dd4b-115">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="8dd4b-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8dd4b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8dd4b-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8dd4b-117">Windows Vista</span></span><br/>       |
| <span data-ttu-id="8dd4b-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8dd4b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8dd4b-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8dd4b-119">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8dd4b-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8dd4b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8dd4b-121">**Qualificateurs spécifiques au fournisseur de vues**</span><span class="sxs-lookup"><span data-stu-id="8dd4b-121">**Qualifiers Specific to the View Provider**</span></span>](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

 




