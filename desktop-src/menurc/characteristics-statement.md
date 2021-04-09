---
title: Instruction de caractéristiques
description: Définit des informations sur une ressource qui peut être utilisée par les outils qui lisent et écrivent les fichiers de définition de ressource.
ms.assetid: 07834b02-a36e-40cc-8907-bff6631842f3
keywords:
- Menus de l’instruction caractéristiques et autres ressources
topic_type:
- apiref
api_name:
- CHARACTERISTICS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de681785fa2ec815b1edbdda913dd8032f8feb8e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030216"
---
# <a name="characteristics-statement"></a><span data-ttu-id="24609-104">Instruction de caractéristiques</span><span class="sxs-lookup"><span data-stu-id="24609-104">CHARACTERISTICS statement</span></span>

<span data-ttu-id="24609-105">Définit des informations sur une ressource qui peut être utilisée par les outils qui lisent et écrivent les fichiers de définition de ressource.</span><span class="sxs-lookup"><span data-stu-id="24609-105">Defines information about a resource that can be used by tools that read and write resource-definition files.</span></span> <span data-ttu-id="24609-106">La valeur **DWORD** spécifiée s’affiche avec la ressource dans le fichier. res compilé.</span><span class="sxs-lookup"><span data-stu-id="24609-106">The specified **DWORD** value appears with the resource in the compiled .res file.</span></span> <span data-ttu-id="24609-107">Toutefois, la valeur n’est pas stockée dans le fichier exécutable et n’a pas d’importance pour le système.</span><span class="sxs-lookup"><span data-stu-id="24609-107">However, the value is not stored in the executable file and has no significance to the system.</span></span>

<span data-ttu-id="24609-108">L’instruction **Characteristics** s’affiche avant le début du corps d’une définition de ressource [**accélérateurs**](accelerators-resource.md), [**boîte de dialogue**](dialog-resource.md), [**menu**](menu-resource.md), [**RCDATA**](rcdata-resource.md)ou [**STRINGTABLE**](stringtable-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="24609-108">The **CHARACTERISTICS** statement appears before the beginning of the body of an [**ACCELERATORS**](accelerators-resource.md), [**DIALOG**](dialog-resource.md), [**MENU**](menu-resource.md), [**RCDATA**](rcdata-resource.md), or [**STRINGTABLE**](stringtable-resource.md) resource definition.</span></span> <span data-ttu-id="24609-109">La valeur spécifiée s’applique uniquement à cette ressource.</span><span class="sxs-lookup"><span data-stu-id="24609-109">The specified value applies only to that resource.</span></span>

``` syntax
CHARACTERISTICS dword
```

<dl> <dt>

<span data-ttu-id="24609-110"><span id="dword"></span><span id="DWORD"></span>*grande*</span><span class="sxs-lookup"><span data-stu-id="24609-110"><span id="dword"></span><span id="DWORD"></span>*dword*</span></span>
</dt> <dd>

<span data-ttu-id="24609-111">Valeur **DWORD** définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="24609-111">User-defined **DWORD** value.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="24609-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="24609-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24609-113">**ACCÉLÉRATEURS**</span><span class="sxs-lookup"><span data-stu-id="24609-113">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="24609-114">**DIALOGUE**</span><span class="sxs-lookup"><span data-stu-id="24609-114">**DIALOG**</span></span>](dialog-resource.md)
</dt> <dt>

[<span data-ttu-id="24609-115">**SOUS**</span><span class="sxs-lookup"><span data-stu-id="24609-115">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="24609-116">**MENUS**</span><span class="sxs-lookup"><span data-stu-id="24609-116">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="24609-117">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="24609-117">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="24609-118">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="24609-118">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> </dl>

 

 




