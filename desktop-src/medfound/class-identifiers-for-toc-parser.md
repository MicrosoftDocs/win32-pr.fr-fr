---
description: Les classes suivantes sont déclarées et associées à des identificateurs de classe (CLSID) dans wmcodecdsp. h.
ms.assetid: f82d92dc-fbce-4274-a10f-72fa8dd776cc
title: Identificateurs de classe pour l’analyseur de table des matières (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5108855c687085e77ce36aa14b3424732e25572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514967"
---
# <a name="class-identifiers-for-table-of-contents-parser"></a><span data-ttu-id="9d80f-103">Identificateurs de classe pour l’analyseur de table des matières</span><span class="sxs-lookup"><span data-stu-id="9d80f-103">Class Identifiers for Table of Contents Parser</span></span>

<span data-ttu-id="9d80f-104">Les classes suivantes sont déclarées et associées à des identificateurs de classe (CLSID) dans wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="9d80f-104">The following classes are declared and associated with class identifiers (CLSIDs) in wmcodecdsp.h.</span></span>



| <span data-ttu-id="9d80f-105">Nom de classe</span><span class="sxs-lookup"><span data-stu-id="9d80f-105">Class name</span></span>       | <span data-ttu-id="9d80f-106">Nom convivial de l’objet</span><span class="sxs-lookup"><span data-stu-id="9d80f-106">Friendly object name</span></span> |
|------------------|----------------------|
| <span data-ttu-id="9d80f-107">CTocEntry</span><span class="sxs-lookup"><span data-stu-id="9d80f-107">CTocEntry</span></span>        | <span data-ttu-id="9d80f-108">Entrée de la table des matières</span><span class="sxs-lookup"><span data-stu-id="9d80f-108">TOC Entry</span></span>            |
| <span data-ttu-id="9d80f-109">CTocEntryList</span><span class="sxs-lookup"><span data-stu-id="9d80f-109">CTocEntryList</span></span>    | <span data-ttu-id="9d80f-110">Liste des entrées de la table des matières</span><span class="sxs-lookup"><span data-stu-id="9d80f-110">TOC Entry List</span></span>       |
| <span data-ttu-id="9d80f-111">CToc</span><span class="sxs-lookup"><span data-stu-id="9d80f-111">CToc</span></span>             | <span data-ttu-id="9d80f-112">Table des matières</span><span class="sxs-lookup"><span data-stu-id="9d80f-112">TOC</span></span>                  |
| <span data-ttu-id="9d80f-113">CTocCollection</span><span class="sxs-lookup"><span data-stu-id="9d80f-113">CTocCollection</span></span>   | <span data-ttu-id="9d80f-114">Collection TOC</span><span class="sxs-lookup"><span data-stu-id="9d80f-114">TOC Collection</span></span>       |
| <span data-ttu-id="9d80f-115">CTocParser</span><span class="sxs-lookup"><span data-stu-id="9d80f-115">CTocParser</span></span>       | <span data-ttu-id="9d80f-116">Analyseur de table des matières</span><span class="sxs-lookup"><span data-stu-id="9d80f-116">TOC Parser</span></span>           |
| <span data-ttu-id="9d80f-117">CTocGeneratorDmo</span><span class="sxs-lookup"><span data-stu-id="9d80f-117">CTocGeneratorDmo</span></span> | <span data-ttu-id="9d80f-118">Générateur de table des matières</span><span class="sxs-lookup"><span data-stu-id="9d80f-118">TOC Generator</span></span>        |



 

<span data-ttu-id="9d80f-119">Le tableau précédent fournit un nom d’objet convivial pour chaque classe.</span><span class="sxs-lookup"><span data-stu-id="9d80f-119">The preceding table gives a friendly object name for each class.</span></span> <span data-ttu-id="9d80f-120">Cette documentation utilise ces noms conviviaux pour faire référence aux instances des classes.</span><span class="sxs-lookup"><span data-stu-id="9d80f-120">This documentation uses those friendly names to refer to instances of the classes.</span></span> <span data-ttu-id="9d80f-121">Par exemple, la documentation fait référence à une instance de la classe CTocEntry en tant qu’objet d’entrée de table des matières.</span><span class="sxs-lookup"><span data-stu-id="9d80f-121">For example, the documentation refers to an instance of the CTocEntry class as a TOC Entry object.</span></span>

<span data-ttu-id="9d80f-122">Dans le code, vous pouvez utiliser **\_ \_ uuidof** pour faire référence aux CLSID.</span><span class="sxs-lookup"><span data-stu-id="9d80f-122">In code, you can use **\_\_uuidof** to refer to the CLSIDs.</span></span> <span data-ttu-id="9d80f-123">Par exemple, vous pouvez utiliser le code suivant pour faire référence au CLSID pour CTocGeneratorDmo.</span><span class="sxs-lookup"><span data-stu-id="9d80f-123">For example, you can use the following code to refer to the CLSID for CTocGeneratorDmo.</span></span>


```C++
__uuidof(CTocGeneratorDmo)
```



### <a name="clsid-constants-defined-in-wmcodecdsph"></a><span data-ttu-id="9d80f-124">Constantes CLSID définies dans Wmcodecdsp. h</span><span class="sxs-lookup"><span data-stu-id="9d80f-124">CLSID Constants Defined in Wmcodecdsp.h</span></span>

<span data-ttu-id="9d80f-125">Au lieu d’utiliser **\_ \_ uuidof**, vous pouvez utiliser des constantes pour faire référence aux CLSID.</span><span class="sxs-lookup"><span data-stu-id="9d80f-125">As an alternative to using **\_\_uuidof**, you can use constants to refer to the CLSIDs.</span></span> <span data-ttu-id="9d80f-126">Les constantes suivantes sont définies dans wmcodecdsp. h</span><span class="sxs-lookup"><span data-stu-id="9d80f-126">The following constants are defined in wmcodecdsp.h</span></span>



| <span data-ttu-id="9d80f-127">Nom de classe</span><span class="sxs-lookup"><span data-stu-id="9d80f-127">Class name</span></span>     | <span data-ttu-id="9d80f-128">CLSID, constante</span><span class="sxs-lookup"><span data-stu-id="9d80f-128">CLSID constant</span></span>        |
|----------------|-----------------------|
| <span data-ttu-id="9d80f-129">CTocEntry</span><span class="sxs-lookup"><span data-stu-id="9d80f-129">CTocEntry</span></span>      | <span data-ttu-id="9d80f-130">CLSID \_ CTocEntry</span><span class="sxs-lookup"><span data-stu-id="9d80f-130">CLSID\_CTocEntry</span></span>      |
| <span data-ttu-id="9d80f-131">CTocEntryList</span><span class="sxs-lookup"><span data-stu-id="9d80f-131">CTocEntryList</span></span>  | <span data-ttu-id="9d80f-132">CLSID \_ CTocEntryList</span><span class="sxs-lookup"><span data-stu-id="9d80f-132">CLSID\_CTocEntryList</span></span>  |
| <span data-ttu-id="9d80f-133">CToc</span><span class="sxs-lookup"><span data-stu-id="9d80f-133">CToc</span></span>           | <span data-ttu-id="9d80f-134">CLSID \_ CToc</span><span class="sxs-lookup"><span data-stu-id="9d80f-134">CLSID\_CToc</span></span>           |
| <span data-ttu-id="9d80f-135">CTocCollection</span><span class="sxs-lookup"><span data-stu-id="9d80f-135">CTocCollection</span></span> | <span data-ttu-id="9d80f-136">CLSID \_ CTocCollection</span><span class="sxs-lookup"><span data-stu-id="9d80f-136">CLSID\_CTocCollection</span></span> |
| <span data-ttu-id="9d80f-137">CTocParser</span><span class="sxs-lookup"><span data-stu-id="9d80f-137">CTocParser</span></span>     | <span data-ttu-id="9d80f-138">CLSID \_ CTocParser</span><span class="sxs-lookup"><span data-stu-id="9d80f-138">CLSID\_CTocParser</span></span>     |



 

### <a name="clsid-constants-defined-in-wmcodecdspuuidlib"></a><span data-ttu-id="9d80f-139">Constantes CLSID définies dans Wmcodecdspuuid. lib</span><span class="sxs-lookup"><span data-stu-id="9d80f-139">CLSID Constants Defined in Wmcodecdspuuid.lib</span></span>

<span data-ttu-id="9d80f-140">La constante CLSID suivante est déclarée, mais pas définie, dans wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="9d80f-140">The following CLSID constant is declared, but not defined, in wmcodecdsp.h.</span></span> <span data-ttu-id="9d80f-141">Pour l’utiliser dans le code, vous devez effectuer une liaison par rapport à wmcodecdspuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="9d80f-141">To use it in code, you must link against wmcodecdspuuid.lib.</span></span>



| <span data-ttu-id="9d80f-142">Nom de classe</span><span class="sxs-lookup"><span data-stu-id="9d80f-142">Class name</span></span>       | <span data-ttu-id="9d80f-143">CLSID, constante</span><span class="sxs-lookup"><span data-stu-id="9d80f-143">CLSID constant</span></span>          |
|------------------|-------------------------|
| <span data-ttu-id="9d80f-144">CTocGeneratorDmo</span><span class="sxs-lookup"><span data-stu-id="9d80f-144">CTocGeneratorDmo</span></span> | <span data-ttu-id="9d80f-145">CLSID \_ CTocGeneratorDmo</span><span class="sxs-lookup"><span data-stu-id="9d80f-145">CLSID\_CTocGeneratorDmo</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="9d80f-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d80f-146">Requirements</span></span>



| <span data-ttu-id="9d80f-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d80f-147">Requirement</span></span> | <span data-ttu-id="9d80f-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d80f-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d80f-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d80f-149">Minimum supported client</span></span><br/> | <span data-ttu-id="9d80f-150">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9d80f-150">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="9d80f-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d80f-151">Minimum supported server</span></span><br/> | <span data-ttu-id="9d80f-152">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9d80f-152">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9d80f-153">En-tête</span><span class="sxs-lookup"><span data-stu-id="9d80f-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d80f-154"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d80f-154"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="9d80f-155">DLL</span><span class="sxs-lookup"><span data-stu-id="9d80f-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d80f-156"><dt>Wmvdspa.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d80f-156"><dt>Wmvdspa.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="9d80f-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d80f-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d80f-158">Objets de l’analyseur de table des matières</span><span class="sxs-lookup"><span data-stu-id="9d80f-158">Table of Contents Parser Objects</span></span>](toc-parser-objects.md)
</dt> </dl>

 

 




