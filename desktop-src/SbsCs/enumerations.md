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
# <a name="side-by-side-assembly-enumerations"></a>Énumérations d’assemblys côte à côte

L’API d’assembly côte à côte utilise les énumérations suivantes.



| Énumération                                                         | Description                                                                                                                                                                                |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_indicateurs CMP \_ ASM**](/windows/win32/api/winsxs/ne-winsxs-asm_cmp_flags)                           | Utilisé par la méthode [**IsEqual**](/windows/desktop/api/winsxs/nf-winsxs-iassemblyname-isequal) pour spécifier les parties de deux noms d’assemblys à comparer.                                                                       |
| [**\_indicateurs d’affichage ASM \_**](/windows/win32/api/winsxs/ne-winsxs-asm_display_flags)                   | Utilisé par la méthode [**GetDisplayName**](/windows/desktop/api/winsxs/nf-winsxs-iassemblyname-getdisplayname) pour spécifier les parties du nom d’assembly côte à côte à inclure dans la représentation sous forme de chaîne du nom. |
| [**nom de l’ASM \_**](/windows/win32/api/winsxs/ne-winsxs-asm_name)                                      | ID de propriété pour les paires nom-valeur dans un nom d’assembly côte à côte.                                                                                                                    |
| [**CRÉER \_ des \_ \_ indicateurs obj du nom ASM \_**](/windows/win32/api/winsxs/ne-winsxs-create_asm_name_obj_flags) | Utilisé par la fonction [**CreateAssemblyNameObject,**](/windows/desktop/api/Winsxs/nf-winsxs-createassemblynameobject) pour spécifier le nom de l’assembly côte à côte.                                                               |



 

 

 



