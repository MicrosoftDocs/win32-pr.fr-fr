---
description: Toutes les classes d’affichage doivent avoir un qualificateur de tableau de chaînes appelé ViewSources.
ms.assetid: aefa8cda-962f-4f6c-92a0-a8825d48db60
ms.tgt_platform: multiple
title: Qualificateur ViewSources
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ViewSources
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1f39146f8065401052c352472b28c4946cca6b98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757761"
---
# <a name="viewsources-qualifier"></a><span data-ttu-id="aab2b-103">Qualificateur ViewSources</span><span class="sxs-lookup"><span data-stu-id="aab2b-103">ViewSources Qualifier</span></span>

<span data-ttu-id="aab2b-104">Toutes les classes d’affichage doivent avoir un qualificateur de tableau de chaînes appelé **ViewSources**.</span><span class="sxs-lookup"><span data-stu-id="aab2b-104">All view classes must have a string array qualifier called **ViewSources**.</span></span> <span data-ttu-id="aab2b-105">Le qualificateur **ViewSources** contient les requêtes source qui définissent les instances source utilisées dans la classe de vue.</span><span class="sxs-lookup"><span data-stu-id="aab2b-105">The **ViewSources** qualifier contains the source queries that define the source instances used in the view class.</span></span> <span data-ttu-id="aab2b-106">La valeur du qualificateur **ViewSources** est un tableau de chaînes contenant des requêtes [*langage de requêtes WMI (WQL) (WQL)*](gloss-w.md) .</span><span class="sxs-lookup"><span data-stu-id="aab2b-106">The value of the **ViewSources** qualifier is a string array containing [*WMI Query Language (WQL)*](gloss-w.md) queries.</span></span> <span data-ttu-id="aab2b-107">Vous pouvez définir des classes sources et restreindre les instances sources que votre classe de vue utilise avec la[clause](where-clause.md) d' [interrogation avec WQL](querying-with-wql.md)pour créer une vue filtrée.</span><span class="sxs-lookup"><span data-stu-id="aab2b-107">You can define source classes and restrict the source instances your view class uses with the [Querying with WQL](querying-with-wql.md)[WHERE Clause](where-clause.md) to create a filtered view.</span></span>

<span data-ttu-id="aab2b-108">Le [fournisseur de vues](view-provider.md) met en correspondance les requêtes sources du qualificateur **ViewSources** avec les espaces de noms répertoriés dans le [qualificateur ViewSpaces](viewspaces-qualifier.md) dans l’ordre dans lequel les requêtes et les espaces de noms sont répertoriés.</span><span class="sxs-lookup"><span data-stu-id="aab2b-108">The [View Provider](view-provider.md) matches the source queries in the **ViewSources** qualifier to the namespaces listed in the [ViewSpaces qualifier](viewspaces-qualifier.md) in the order the queries and namespaces are listed.</span></span> <span data-ttu-id="aab2b-109">Le nombre de requêtes source doit correspondre au nombre d’espaces de noms figurant dans le qualificateur ViewSpaces.</span><span class="sxs-lookup"><span data-stu-id="aab2b-109">The number of source queries must match the number of namespaces listed in the ViewSpaces qualifier.</span></span> <span data-ttu-id="aab2b-110">L’ordre dans lequel vous répertoriez les requêtes source détermine les espaces de noms à partir desquels les instances source sont dessinées.</span><span class="sxs-lookup"><span data-stu-id="aab2b-110">The order in which you list the source queries determines the namespaces from which the source instances are drawn.</span></span>

<span data-ttu-id="aab2b-111">L’exemple suivant sélectionne uniquement les instances de la classe **LocalDisk** où la valeur de la propriété **FileSystem** est « NTFS » et les instances de la classe **RemoteDisk** où la valeur de la propriété **FreeSpace** est supérieure à 45 mégaoctets :</span><span class="sxs-lookup"><span data-stu-id="aab2b-111">The following example selects only instances of the **LocalDisk** class where the value of the **FileSystem** property is "NTFS" and instances of the **RemoteDisk** class where the value of the **FreeSpace** property is greater than 45 megabytes:</span></span>


```sql
ViewSources{
"SELECT __Namespace, 
   Description, 
   DeviceID, 
   FileSystem, 
   FreeSpace, 
   VolumeName FROM LocalDisk 
 WHERE FileSystem = \"NTFS\"", 
   "SELECT __Namespace, 
   Description,
   DeviceID, 
   FileSystem, 
   FreeSpace, 
   VolumeName FROM RemoteDisk 
 WHERE FreeSpace > 45000000"}
```



> [!Note]  
> <span data-ttu-id="aab2b-112">Le nombre de requêtes sources que vous pouvez définir pour les classes de vue de jointure dépend du nombre d’instances retournées par ces requêtes et du nombre de façons dont ces instances peuvent être jointes.</span><span class="sxs-lookup"><span data-stu-id="aab2b-112">The number of source queries you can define for join view classes depends on the number of instances these queries return and how many ways these instances can be joined.</span></span> <span data-ttu-id="aab2b-113">Le nombre de combinaisons possibles d’instances source pour les classes d’affichage augmente de façon exponentielle, donc gardez les requêtes source pour les classes de vue de jointure aussi simples que possible.</span><span class="sxs-lookup"><span data-stu-id="aab2b-113">The number of possible combinations of source instances for view classes grows exponentially, so keep source queries for join view classes as simple as possible.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="aab2b-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aab2b-114">Requirements</span></span>



| <span data-ttu-id="aab2b-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aab2b-115">Requirement</span></span> | <span data-ttu-id="aab2b-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="aab2b-116">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="aab2b-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aab2b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="aab2b-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aab2b-118">Windows Vista</span></span><br/>       |
| <span data-ttu-id="aab2b-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aab2b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="aab2b-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aab2b-120">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="aab2b-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aab2b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aab2b-122">**Qualificateurs spécifiques au fournisseur de vues**</span><span class="sxs-lookup"><span data-stu-id="aab2b-122">**Qualifiers Specific to the View Provider**</span></span>](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

 




