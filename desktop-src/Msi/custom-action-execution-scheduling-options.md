---
description: Étant donné qu’une action personnalisée peut être planifiée dans les tables d’interface utilisateur et d’exécution, et qu’elle peut être exécutée dans le processus du service ou du client, une action personnalisée peut potentiellement s’exécuter plusieurs fois.
ms.assetid: a3ffeecb-cdd6-43af-a3fe-48e3e843ec8b
title: Options de planification de l’exécution des actions personnalisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bfa5aee44f3ad357eefc6f9dd9c5ee5ae45797c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518732"
---
# <a name="custom-action-execution-scheduling-options"></a><span data-ttu-id="10391-103">Options de planification de l’exécution des actions personnalisées</span><span class="sxs-lookup"><span data-stu-id="10391-103">Custom Action Execution Scheduling Options</span></span>

<span data-ttu-id="10391-104">Étant donné qu’une action personnalisée peut être planifiée dans les tables d’interface utilisateur et d’exécution, et qu’elle peut être exécutée dans le processus du service ou du client, une action personnalisée peut potentiellement s’exécuter plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="10391-104">Because a custom action can be scheduled in both the UI and execute sequence tables, and can be executed either in the service or client process, a custom action can potentially execute multiple times.</span></span>

<span data-ttu-id="10391-105">Notez que le programme d’installation :</span><span class="sxs-lookup"><span data-stu-id="10391-105">Note that the installer:</span></span>

-   <span data-ttu-id="10391-106">Exécute des actions dans une table de séquences immédiatement par défaut.</span><span class="sxs-lookup"><span data-stu-id="10391-106">Executes actions in a sequence table immediately by default.</span></span>
-   <span data-ttu-id="10391-107">N’exécute pas d’action si le champ expression conditionnelle de la table Sequence prend la valeur false.</span><span class="sxs-lookup"><span data-stu-id="10391-107">Does not execute an action if the conditional expression field of the sequence table evaluates to False.</span></span>
-   <span data-ttu-id="10391-108">Traite la table de séquence d’interface utilisateur dans le processus client si le niveau d’interface de l’utilisateur interne est défini sur le mode d’interface utilisateur complet (consultez [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) pour obtenir une description des niveaux de l’interface utilisateur).</span><span class="sxs-lookup"><span data-stu-id="10391-108">Processes the UI sequence table in the client process if the internal user's interface level is set to the full UI mode (see [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) for a description of UI levels).</span></span>
-   <span data-ttu-id="10391-109">Est un service inscrit par défaut lors de l’utilisation de Windows 2000 et, dans ce cas, la table d’exécution des séquences est traitée dans le service d’installation.</span><span class="sxs-lookup"><span data-stu-id="10391-109">Is a service registered by default when using Windows 2000 and, in this case, the execute sequence table is processed in the installer service.</span></span>

<span data-ttu-id="10391-110">Vous pouvez utiliser les indicateurs d’option suivants pour contrôler plusieurs exécutions immédiates d’actions personnalisées.</span><span class="sxs-lookup"><span data-stu-id="10391-110">You can use the following option flags to control multiple immediate execution of custom actions.</span></span> <span data-ttu-id="10391-111">Pour définir une option, ajoutez la valeur de ce tableau à la valeur du champ type de la [table CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="10391-111">To set an option, add the value in this table to the value in the Type field of the [CustomAction table](customaction-table.md).</span></span> <span data-ttu-id="10391-112">Aucun des indicateurs suivants ne doit être utilisé avec des [actions personnalisées d’exécution différée](deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="10391-112">None of the following flags should be used with [deferred execution custom actions](deferred-execution-custom-actions.md).</span></span>

<dl> <dt>

<span data-ttu-id="10391-113"><span id="_default_"></span><span id="_DEFAULT_"></span>valeurs</span><span class="sxs-lookup"><span data-stu-id="10391-113"><span id="_default_"></span><span id="_DEFAULT_"></span>(default)</span></span>
</dt> <dd>

<span data-ttu-id="10391-114">Hexadécimal : 0x00000000</span><span class="sxs-lookup"><span data-stu-id="10391-114">Hexadecimal: 0x00000000</span></span>

<span data-ttu-id="10391-115">Décimal : 0</span><span class="sxs-lookup"><span data-stu-id="10391-115">Decimal: 0</span></span>

<span data-ttu-id="10391-116">Exécutez toujours.</span><span class="sxs-lookup"><span data-stu-id="10391-116">Always execute.</span></span> <span data-ttu-id="10391-117">L’action peut s’exécuter deux fois si elle est présente dans les deux tables de séquence.</span><span class="sxs-lookup"><span data-stu-id="10391-117">Action may run twice if present in both sequence tables.</span></span>

</dd> <dt>

<span data-ttu-id="10391-118"><span id="msidbCustomActionTypeFirstSequence_"></span><span id="msidbcustomactiontypefirstsequence_"></span><span id="MSIDBCUSTOMACTIONTYPEFIRSTSEQUENCE_"></span>**msidbCustomActionTypeFirstSequence**</span><span class="sxs-lookup"><span data-stu-id="10391-118"><span id="msidbCustomActionTypeFirstSequence_"></span><span id="msidbcustomactiontypefirstsequence_"></span><span id="MSIDBCUSTOMACTIONTYPEFIRSTSEQUENCE_"></span>**msidbCustomActionTypeFirstSequence**</span></span> 
</dt> <dd>

<span data-ttu-id="10391-119">Hexadécimal : 0x00000100</span><span class="sxs-lookup"><span data-stu-id="10391-119">Hexadecimal: 0x00000100</span></span>

<span data-ttu-id="10391-120">Décimal : 256</span><span class="sxs-lookup"><span data-stu-id="10391-120">Decimal: 256</span></span>

<span data-ttu-id="10391-121">Ne pas exécuter plus d’une fois si elle est présente dans les deux tables de séquence.</span><span class="sxs-lookup"><span data-stu-id="10391-121">Execute no more than once if present in both sequence tables.</span></span> <span data-ttu-id="10391-122">Ignore toujours l’action dans la séquence d’exécution si la séquence d’interface utilisateur a été exécutée.</span><span class="sxs-lookup"><span data-stu-id="10391-122">Always skips action in execute sequence if UI sequence has run.</span></span> <span data-ttu-id="10391-123">Aucun effet dans la séquence d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="10391-123">No effect in UI sequence.</span></span> <span data-ttu-id="10391-124">L’action ne doit pas obligatoirement être présente ou exécutée dans la séquence d’interface utilisateur pour être ignorée dans la séquence d’exécution.</span><span class="sxs-lookup"><span data-stu-id="10391-124">The action is not required to be present or run in the UI sequence to be skipped in the execute sequence.</span></span> <span data-ttu-id="10391-125">Non affecté par l’inscription du service d’installation.</span><span class="sxs-lookup"><span data-stu-id="10391-125">Not affected by install service registration.</span></span>

</dd> <dt>

<span data-ttu-id="10391-126"><span id="msidbCustomActionTypeOncePerProcess"></span><span id="msidbcustomactiontypeonceperprocess"></span><span id="MSIDBCUSTOMACTIONTYPEONCEPERPROCESS"></span>**msidbCustomActionTypeOncePerProcess**</span><span class="sxs-lookup"><span data-stu-id="10391-126"><span id="msidbCustomActionTypeOncePerProcess"></span><span id="msidbcustomactiontypeonceperprocess"></span><span id="MSIDBCUSTOMACTIONTYPEONCEPERPROCESS"></span>**msidbCustomActionTypeOncePerProcess**</span></span>
</dt> <dd>

<span data-ttu-id="10391-127">Hexadécimal : 0x00000200</span><span class="sxs-lookup"><span data-stu-id="10391-127">Hexadecimal: 0x00000200</span></span>

<span data-ttu-id="10391-128">Décimal : 512</span><span class="sxs-lookup"><span data-stu-id="10391-128">Decimal: 512</span></span>

<span data-ttu-id="10391-129">Exécuter une fois par processus si les deux tables de séquences.</span><span class="sxs-lookup"><span data-stu-id="10391-129">Execute once per process if in both sequence tables.</span></span> <span data-ttu-id="10391-130">Ignore l’action dans la séquence d’exécution si la séquence d’interface utilisateur a été exécutée dans le même processus, par exemple s’exécuter dans le processus client.</span><span class="sxs-lookup"><span data-stu-id="10391-130">Skips action in execute sequence if UI sequence has been run in same process, for example both run in the client process.</span></span> <span data-ttu-id="10391-131">Permet d’empêcher les actions qui modifient l’état de la session, telles que les données de la propriété et de la base de données, de s’exécuter deux fois.</span><span class="sxs-lookup"><span data-stu-id="10391-131">Used to prevent actions that modify the session state, such as property and database data, from running twice.</span></span>

</dd> <dt>

<span data-ttu-id="10391-132"><span id="msidbCustomActionTypeClientRepeat"></span><span id="msidbcustomactiontypeclientrepeat"></span><span id="MSIDBCUSTOMACTIONTYPECLIENTREPEAT"></span>**msidbCustomActionTypeClientRepeat**</span><span class="sxs-lookup"><span data-stu-id="10391-132"><span id="msidbCustomActionTypeClientRepeat"></span><span id="msidbcustomactiontypeclientrepeat"></span><span id="MSIDBCUSTOMACTIONTYPECLIENTREPEAT"></span>**msidbCustomActionTypeClientRepeat**</span></span>
</dt> <dd>

<span data-ttu-id="10391-133">Hexadécimal : 0x00000300</span><span class="sxs-lookup"><span data-stu-id="10391-133">Hexadecimal: 0x00000300</span></span>

<span data-ttu-id="10391-134">Décimal : 768</span><span class="sxs-lookup"><span data-stu-id="10391-134">Decimal: 768</span></span>

<span data-ttu-id="10391-135">S’exécute uniquement en cas d’exécution sur le client après l’exécution de la séquence d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="10391-135">Execute only if running on client after UI sequence has run.</span></span> <span data-ttu-id="10391-136">L’action s’exécute uniquement si la séquence d’exécution est exécutée sur le client suivant la séquence d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="10391-136">The action runs only if the execute sequence is run on the client following UI sequence.</span></span> <span data-ttu-id="10391-137">Peut être utilisé pour fournir une logique/ou logique, ou pour supprimer le traitement lié à l’interface utilisateur s’il est déjà fait pour la session cliente.</span><span class="sxs-lookup"><span data-stu-id="10391-137">May be used to provide either/or logic, or to suppress the UI-related processing if already done for the client session.</span></span>

</dd> </dl>

<span data-ttu-id="10391-138">Notez que pour exécuter une action personnalisée pendant deux modes d’exécution différents, créez deux entrées dans la [table CustomAction](customaction-table.md) .</span><span class="sxs-lookup"><span data-stu-id="10391-138">Note that to run a custom action during two different run modes, author two entries into the [CustomAction table](customaction-table.md) .</span></span> <span data-ttu-id="10391-139">Par exemple, pour avoir une action personnalisée qui appelle une bibliothèque de liens dynamiques (DLL) C/C++ ( [type d’action personnalisée 1](custom-action-type-1.md)) quand le mode est MSIRUNMODE \_ planifié et MSIRUNMODE \_ Rollback, placez deux entrées dans la table CustomAction qui appellent la même dll mais qui ont des types numériques différents.</span><span class="sxs-lookup"><span data-stu-id="10391-139">For example, to have a custom action that calls a C/C++ dynamic link library (DLL) ( [Custom Action Type 1](custom-action-type-1.md)) both when the mode is MSIRUNMODE\_SCHEDULED and MSIRUNMODE\_ROLLBACK, put two entries in the CustomAction table that call the same DLL but that have different numeric types.</span></span> <span data-ttu-id="10391-140">Incluez le code qui appelle [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) pour déterminer quand exécuter l’action personnalisée.</span><span class="sxs-lookup"><span data-stu-id="10391-140">Include code that calls [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) to determine when to run which custom action.</span></span>

## <a name="related-topics"></a><span data-ttu-id="10391-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="10391-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10391-142">Référence des actions personnalisées</span><span class="sxs-lookup"><span data-stu-id="10391-142">Custom Action Reference</span></span>](custom-action-reference.md)
</dt> <dt>

[<span data-ttu-id="10391-143">À propos des actions personnalisées</span><span class="sxs-lookup"><span data-stu-id="10391-143">About Custom Actions</span></span>](about-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="10391-144">Utilisation d’actions personnalisées</span><span class="sxs-lookup"><span data-stu-id="10391-144">Using Custom Actions</span></span>](using-custom-actions.md)
</dt> </dl>

 

 



