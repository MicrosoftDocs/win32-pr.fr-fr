---
description: En savoir plus sur les énumérations utilisées dans l’API d’assembly côte à côte, par exemple ASM_CMP_FLAGS et CREATE_ASM_NAME_OBJ_FLAGS.
ms.assetid: e73c37e3-7879-4754-b39c-91be64fc8d73
title: Énumérations d’assemblys côte à côte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52f393ab9d8657ecaa52cad555dad5a831699687
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404742"
---
# <a name="side-by-side-assembly-enumerations"></a><span data-ttu-id="09e94-103">Énumérations d’assemblys côte à côte</span><span class="sxs-lookup"><span data-stu-id="09e94-103">Side-by-Side Assembly Enumerations</span></span>

<span data-ttu-id="09e94-104">L’API d’assembly côte à côte utilise les énumérations suivantes.</span><span class="sxs-lookup"><span data-stu-id="09e94-104">The side-by-side assembly API uses the following enumerations.</span></span>



| <span data-ttu-id="09e94-105">Énumération</span><span class="sxs-lookup"><span data-stu-id="09e94-105">Enumeration</span></span>                                                         | <span data-ttu-id="09e94-106">Description</span><span class="sxs-lookup"><span data-stu-id="09e94-106">Description</span></span>                                                                                                                                                                                |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="09e94-107">**\_indicateurs CMP \_ ASM**</span><span class="sxs-lookup"><span data-stu-id="09e94-107">**ASM\_CMP\_FLAGS**</span></span>](/windows/win32/api/winsxs/ne-winsxs-asm_cmp_flags)                           | <span data-ttu-id="09e94-108">Utilisé par la méthode [**IsEqual**](/windows/desktop/api/winsxs/nf-winsxs-iassemblyname-isequal) pour spécifier les parties de deux noms d’assemblys à comparer.</span><span class="sxs-lookup"><span data-stu-id="09e94-108">Used by the [**IsEqual**](/windows/desktop/api/winsxs/nf-winsxs-iassemblyname-isequal) method to specify which parts of two assembly names to compare.</span></span>                                                                       |
| [<span data-ttu-id="09e94-109">**\_indicateurs d’affichage ASM \_**</span><span class="sxs-lookup"><span data-stu-id="09e94-109">**ASM\_DISPLAY\_FLAGS**</span></span>](/windows/win32/api/winsxs/ne-winsxs-asm_display_flags)                   | <span data-ttu-id="09e94-110">Utilisé par la méthode [**GetDisplayName**](/windows/desktop/api/winsxs/nf-winsxs-iassemblyname-getdisplayname) pour spécifier les parties du nom d’assembly côte à côte à inclure dans la représentation sous forme de chaîne du nom.</span><span class="sxs-lookup"><span data-stu-id="09e94-110">Used by the [**GetDisplayName**](/windows/desktop/api/winsxs/nf-winsxs-iassemblyname-getdisplayname) method to specify which portions of the side-by-side assembly name to include in the string representation of the name.</span></span> |
| [<span data-ttu-id="09e94-111">**nom de l’ASM \_**</span><span class="sxs-lookup"><span data-stu-id="09e94-111">**ASM\_NAME**</span></span>](/windows/win32/api/winsxs/ne-winsxs-asm_name)                                      | <span data-ttu-id="09e94-112">ID de propriété pour les paires nom-valeur dans un nom d’assembly côte à côte.</span><span class="sxs-lookup"><span data-stu-id="09e94-112">Property IDs for the name-value pairs in an side-by-side assembly name.</span></span>                                                                                                                    |
| [<span data-ttu-id="09e94-113">**CRÉER \_ des \_ \_ indicateurs obj du nom ASM \_**</span><span class="sxs-lookup"><span data-stu-id="09e94-113">**CREATE\_ASM\_NAME\_OBJ\_FLAGS**</span></span>](/windows/win32/api/winsxs/ne-winsxs-create_asm_name_obj_flags) | <span data-ttu-id="09e94-114">Utilisé par la fonction [**CreateAssemblyNameObject,**](/windows/desktop/api/Winsxs/nf-winsxs-createassemblynameobject) pour spécifier le nom de l’assembly côte à côte.</span><span class="sxs-lookup"><span data-stu-id="09e94-114">Used by the [**CreateAssemblyNameObject**](/windows/desktop/api/Winsxs/nf-winsxs-createassemblynameobject) function to specify the side-by-side assembly name.</span></span>                                                               |



 

 

 



