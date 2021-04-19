---
description: Vous pouvez filtrer les instances d’une classe de vue de jointure en affectant une requête WQL au qualificateur PostJoinFilter.
ms.assetid: 926a7262-ea6b-4a5a-8aa7-6ec0ae389031
ms.tgt_platform: multiple
title: Qualificateur PostJoinFilter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PostJoinFilter
api_type:
- NA
api_location: ''
ms.openlocfilehash: ac86aeafefc8057a1612c5007e55e7633c655c59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534642"
---
# <a name="postjoinfilter-qualifier"></a><span data-ttu-id="b72ad-103">Qualificateur PostJoinFilter</span><span class="sxs-lookup"><span data-stu-id="b72ad-103">PostJoinFilter Qualifier</span></span>

<span data-ttu-id="b72ad-104">Vous pouvez filtrer les instances d’une classe de vue de jointure en affectant une requête WQL au qualificateur **PostJoinFilter** .</span><span class="sxs-lookup"><span data-stu-id="b72ad-104">You can filter the instances of a join view class by assigning a WQL query to the **PostJoinFilter** qualifier.</span></span> <span data-ttu-id="b72ad-105">La valeur de la requête WQL est appliquée aux instances de la classe de vue de jointure.</span><span class="sxs-lookup"><span data-stu-id="b72ad-105">The value of the WQL query is applied to the instances of the join view class.</span></span> <span data-ttu-id="b72ad-106">Vous pouvez utiliser ce qualificateur pour limiter les instances de votre classe d’affichage à celles qui répondent à des conditions spécifiques.</span><span class="sxs-lookup"><span data-stu-id="b72ad-106">You can use this qualifier to restrict the instances of your view class to those that meet specific conditions.</span></span> <span data-ttu-id="b72ad-107">La requête WQL suivante filtre les instances d’une classe join appelée en fonction des instances de [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span><span class="sxs-lookup"><span data-stu-id="b72ad-107">The following WQL query filters instances of a join class called based on instances of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span></span>


```C++
PostJoinFilter("SELECT * FROM JoinDrive" +
    " WHERE FreeSpace > 1000000" +
    " and Description = \"3 1/2 Inch Floppy Drive\"")
```



<span data-ttu-id="b72ad-108">L’utilisation de ce qualificateur présente plusieurs restrictions :</span><span class="sxs-lookup"><span data-stu-id="b72ad-108">There are several restrictions to the use of this qualifier:</span></span>

-   <span data-ttu-id="b72ad-109">**PostJoinFilter** est disponible uniquement pour les classes de vue de jointure.</span><span class="sxs-lookup"><span data-stu-id="b72ad-109">**PostJoinFilter** is only available to join view classes.</span></span>
-   <span data-ttu-id="b72ad-110">Le nom de la classe et les noms de propriété spécifiés dans la requête font référence aux propriétés de la classe d’affichage, et non à la classe source.</span><span class="sxs-lookup"><span data-stu-id="b72ad-110">The class name and property names specified in the query refer to the properties of the view class, not the source class.</span></span>
-   <span data-ttu-id="b72ad-111">Aucune exclusion de propriétés n’est autorisée ; seules `SELECT *` les requêtes de type sont autorisées.</span><span class="sxs-lookup"><span data-stu-id="b72ad-111">No exclusion of properties is permitted; only `SELECT *` type queries are allowed.</span></span>

## <a name="requirements"></a><span data-ttu-id="b72ad-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b72ad-112">Requirements</span></span>



| <span data-ttu-id="b72ad-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b72ad-113">Requirement</span></span> | <span data-ttu-id="b72ad-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="b72ad-114">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="b72ad-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b72ad-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b72ad-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b72ad-116">Windows Vista</span></span><br/>       |
| <span data-ttu-id="b72ad-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b72ad-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b72ad-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b72ad-118">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b72ad-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b72ad-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b72ad-120">**Qualificateurs spécifiques au fournisseur de vues**</span><span class="sxs-lookup"><span data-stu-id="b72ad-120">**Qualifiers Specific to the View Provider**</span></span>](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

