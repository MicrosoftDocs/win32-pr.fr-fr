---
description: Le tableau suivant présente les différentes méthodes que l’application peut utiliser pour gérer le signe insertion, la justification et les clusters.
ms.assetid: 950a24b4-62ab-4eaf-ac15-87434d3c28c0
title: Utilisation des relations entre les positions du signe insertion, les points de justification et les clusters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d051d008a8ae991b2858be598713fe9ad1adc0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517508"
---
# <a name="working-with-relationships-among-caret-positions-justification-points-and-clusters"></a><span data-ttu-id="ca441-103">Utilisation des relations entre les positions du signe insertion, les points de justification et les clusters</span><span class="sxs-lookup"><span data-stu-id="ca441-103">Working with Relationships Among Caret Positions, Justification Points, and Clusters</span></span>

<span data-ttu-id="ca441-104">Le tableau suivant présente les différentes méthodes que l’application peut utiliser pour gérer le signe insertion, la justification et les clusters.</span><span class="sxs-lookup"><span data-stu-id="ca441-104">The following table shows the various methods that the application can use to handle the caret, justification, and clusters.</span></span>



| <span data-ttu-id="ca441-105">Tâche</span><span class="sxs-lookup"><span data-stu-id="ca441-105">Task</span></span>                             | <span data-ttu-id="ca441-106">Support Uniscribe</span><span class="sxs-lookup"><span data-stu-id="ca441-106">Uniscribe support</span></span>                                                                                                                                                                                                                                                              |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca441-107">Déplacer le signe insertion par cluster de caractères</span><span class="sxs-lookup"><span data-stu-id="ca441-107">Caret move by character cluster</span></span>  | <span data-ttu-id="ca441-108">Paramètre *pwLogClust* du membre [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) functionThe **FClusterStart** de la structure de [**script \_ VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr)</span><span class="sxs-lookup"><span data-stu-id="ca441-108">The *pwLogClust* parameter of the [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) functionThe **fClusterStart** member of the [**SCRIPT\_VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr) structure</span></span><br/> <span data-ttu-id="ca441-109">Le membre **fCharStop** de la structure de [**script \_ LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr)</span><span class="sxs-lookup"><span data-stu-id="ca441-109">The **fCharStop** member of the [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure</span></span><br/> |
| <span data-ttu-id="ca441-110">Saut de ligne entre les caractères</span><span class="sxs-lookup"><span data-stu-id="ca441-110">Line breaking between characters</span></span> | <span data-ttu-id="ca441-111">Paramètre *pwLogClust* du membre [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) functionThe **FClusterStart** de la structure de [**script \_ VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr)</span><span class="sxs-lookup"><span data-stu-id="ca441-111">The *pwLogClust* parameter of the [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) functionThe **fClusterStart** member of the [**SCRIPT\_VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr) structure</span></span><br/> <span data-ttu-id="ca441-112">Le membre **fCharStop** de la structure de [**script \_ LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr)</span><span class="sxs-lookup"><span data-stu-id="ca441-112">The **fCharStop** member of the [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure</span></span><br/> |
| <span data-ttu-id="ca441-113">Déplacer le signe insertion par mot</span><span class="sxs-lookup"><span data-stu-id="ca441-113">Caret move by word</span></span>               | <span data-ttu-id="ca441-114">Le membre **fWordStop** de la structure de [**script \_ LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr)</span><span class="sxs-lookup"><span data-stu-id="ca441-114">The **fWordStop** member of the [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="ca441-115">Saut de ligne entre les mots</span><span class="sxs-lookup"><span data-stu-id="ca441-115">Line breaking between words</span></span>      | <span data-ttu-id="ca441-116">Le membre **fWordStop** de la structure de [**script \_ LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr)</span><span class="sxs-lookup"><span data-stu-id="ca441-116">The **fWordStop** member of the [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="ca441-117">Justification</span><span class="sxs-lookup"><span data-stu-id="ca441-117">Justification</span></span>                    | <span data-ttu-id="ca441-118">Le membre **uJustification** de la structure de [**script \_ VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr)</span><span class="sxs-lookup"><span data-stu-id="ca441-118">The **uJustification** member of the [**SCRIPT\_VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr) structure</span></span>                                                                                                                                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="ca441-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ca441-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca441-120">Utilisation de Uniscribe</span><span class="sxs-lookup"><span data-stu-id="ca441-120">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 




