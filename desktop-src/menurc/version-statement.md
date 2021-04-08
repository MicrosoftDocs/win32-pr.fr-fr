---
title: VERSION (instruction)
description: Définit des informations de version sur une ressource qui peut être utilisée par les outils qui lisent et écrivent des fichiers de ressources.
ms.assetid: 3a33cff3-b8b3-43f4-b43a-ff1d1728cdc1
keywords:
- Menus de l’instruction de VERSION et autres ressources
topic_type:
- apiref
api_name:
- VERSION
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 302ffcee38b287afff2697b9c5a5241fa406b55c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678541"
---
# <a name="version-statement"></a><span data-ttu-id="735a2-104">VERSION (instruction)</span><span class="sxs-lookup"><span data-stu-id="735a2-104">VERSION statement</span></span>

<span data-ttu-id="735a2-105">Définit des informations de version sur une ressource qui peut être utilisée par les outils qui lisent et écrivent des fichiers de ressources.</span><span class="sxs-lookup"><span data-stu-id="735a2-105">Defines version information about a resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="735a2-106">La valeur *DWORD* spécifiée s’affiche avec la ressource dans le compilé. Fichier RES.</span><span class="sxs-lookup"><span data-stu-id="735a2-106">The specified *dword* value appears with the resource in the compiled .RES file.</span></span> <span data-ttu-id="735a2-107">Toutefois, la valeur n’est pas stockée dans le fichier exécutable et n’a pas d’importance pour le système.</span><span class="sxs-lookup"><span data-stu-id="735a2-107">However, the value is not stored in the executable file and has no significance to the system.</span></span>

<span data-ttu-id="735a2-108">L’instruction **version** apparaît avant le début du corps d’une définition de ressource [**accélérateurs**](accelerators-resource.md), [**DIALOGEX**](dialogex-resource.md), [**menu**](menu-resource.md), [**RCDATA**](rcdata-resource.md)ou [**STRINGTABLE**](stringtable-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="735a2-108">The **VERSION** statement appears before the beginning of the body of an [**ACCELERATORS**](accelerators-resource.md), [**DIALOGEX**](dialogex-resource.md), [**MENU**](menu-resource.md), [**RCDATA**](rcdata-resource.md), or [**STRINGTABLE**](stringtable-resource.md) resource definition.</span></span> <span data-ttu-id="735a2-109">La valeur spécifiée s’applique uniquement à cette ressource.</span><span class="sxs-lookup"><span data-stu-id="735a2-109">The specified value applies only to that resource.</span></span>

``` syntax
VERSION dword
```

<dl> <dt>

<span data-ttu-id="735a2-110"><span id="dword"></span><span id="DWORD"></span>*grande*</span><span class="sxs-lookup"><span data-stu-id="735a2-110"><span id="dword"></span><span id="DWORD"></span>*dword*</span></span>
</dt> <dd>

<span data-ttu-id="735a2-111">Valeur **DWORD** définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="735a2-111">A user-defined **DWORD** value.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="735a2-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="735a2-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="735a2-113">**ACCÉLÉRATEURS**</span><span class="sxs-lookup"><span data-stu-id="735a2-113">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="735a2-114">**ATTRIBUTS**</span><span class="sxs-lookup"><span data-stu-id="735a2-114">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="735a2-115">**SOUS**</span><span class="sxs-lookup"><span data-stu-id="735a2-115">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="735a2-116">**MENUS**</span><span class="sxs-lookup"><span data-stu-id="735a2-116">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="735a2-117">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="735a2-117">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="735a2-118">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="735a2-118">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> </dl>

 

 




