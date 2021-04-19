---
description: L’action RegisterTypeLibraries enregistre les bibliothèques de types avec le système. Cette action est appliquée à chaque fichier référencé dans la table TypeLib qui est planifiée pour l’installation.
ms.assetid: 374450bb-316c-4fe6-abb1-cd8a8a31f284
title: Action RegisterTypeLibraries
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 469cc18fc2842a3258804fc012c48a49085f1598
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106541206"
---
# <a name="registertypelibraries-action"></a><span data-ttu-id="b4e49-104">Action RegisterTypeLibraries</span><span class="sxs-lookup"><span data-stu-id="b4e49-104">RegisterTypeLibraries Action</span></span>

<span data-ttu-id="b4e49-105">L’action RegisterTypeLibraries enregistre les bibliothèques de types avec le système.</span><span class="sxs-lookup"><span data-stu-id="b4e49-105">The RegisterTypeLibraries action registers type libraries with the system.</span></span> <span data-ttu-id="b4e49-106">Cette action est appliquée à chaque fichier référencé dans la [table Typelib](typelib-table.md) qui est planifiée pour l’installation.</span><span class="sxs-lookup"><span data-stu-id="b4e49-106">This action is applied to each file referred to in the [TypeLib table](typelib-table.md) that is scheduled for install.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="b4e49-107">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="b4e49-107">Sequence Restrictions</span></span>

<span data-ttu-id="b4e49-108">L’action RegisterTypeLibraries doit venir après l’action [InstallFiles](installfiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="b4e49-108">The RegisterTypeLibraries action must come after the [InstallFiles](installfiles-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="b4e49-109">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="b4e49-109">ActionData Messages</span></span>



| <span data-ttu-id="b4e49-110">Champ</span><span class="sxs-lookup"><span data-stu-id="b4e49-110">Field</span></span> | <span data-ttu-id="b4e49-111">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="b4e49-111">Description of action data</span></span>                   |
|-------|----------------------------------------------|
| <span data-ttu-id="b4e49-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="b4e49-112">\[1\]</span></span> | <span data-ttu-id="b4e49-113">[GUID](guid.md) de la bibliothèque de types inscrite.</span><span class="sxs-lookup"><span data-stu-id="b4e49-113">[GUID](guid.md) of registered type library.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b4e49-114">Notes</span><span class="sxs-lookup"><span data-stu-id="b4e49-114">Remarks</span></span>

<span data-ttu-id="b4e49-115">L’action RegisterTypeLibraries nécessite que le langage de la bibliothèque de types soit correctement créé dans le champ Language de la table TypeLib.</span><span class="sxs-lookup"><span data-stu-id="b4e49-115">The RegisterTypeLibraries action requires that the type library language be correctly authored in the Language field of the TypeLib table.</span></span> <span data-ttu-id="b4e49-116">Une création incorrecte du champ Language peut provoquer l’échec de l’inscription d’une bibliothèque de types valide dans le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="b4e49-116">Incorrect authoring of the Language field can cause the installer to fail to register an otherwise valid type library.</span></span>

 

 



