---
description: Les actions personnalisées sont appelées de la même façon que les actions standard, soit par appel explicite, soit lors de l’exécution d’une table de séquences.
ms.assetid: 05f15bae-983a-4763-840d-f2590f4e2a7a
title: Appel d’actions personnalisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02f1e9a575d32cbb8fe22323d4a741eb7936ef9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527696"
---
# <a name="invoking-custom-actions"></a><span data-ttu-id="4523c-103">Appel d’actions personnalisées</span><span class="sxs-lookup"><span data-stu-id="4523c-103">Invoking Custom Actions</span></span>

<span data-ttu-id="4523c-104">Les actions personnalisées sont appelées de la même façon que les actions standard, soit par appel explicite, soit lors de l’exécution d’une table de séquences.</span><span class="sxs-lookup"><span data-stu-id="4523c-104">Custom actions are invoked in the same manner as standard actions, either by explicit invocation or during the execution of a sequence table.</span></span> <span data-ttu-id="4523c-105">Il existe deux méthodes pour appeler des actions :</span><span class="sxs-lookup"><span data-stu-id="4523c-105">There are two methods for calling actions:</span></span>

-   <span data-ttu-id="4523c-106">Vous appelez l’action spécifiée directement avec la fonction [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) .</span><span class="sxs-lookup"><span data-stu-id="4523c-106">You call the specified action directly with the [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) function.</span></span>
-   <span data-ttu-id="4523c-107">Une action de niveau supérieur appelle la table Sequence contenant l’action personnalisée.</span><span class="sxs-lookup"><span data-stu-id="4523c-107">A top-level action calls the sequence table containing the custom action.</span></span> <span data-ttu-id="4523c-108">Pour plus d’informations sur la planification d’une action personnalisée dans une table de séquences, consultez [séquencement des actions personnalisées](sequencing-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="4523c-108">For more information about scheduling a custom action in a sequence table, see [Sequencing Custom Actions](sequencing-custom-actions.md).</span></span>

<span data-ttu-id="4523c-109">Quand le programme d’installation obtient un nom d’action à partir de la fonction [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) , ou d’une table de séquence, il commence par Rechercher une action standard portant ce nom.</span><span class="sxs-lookup"><span data-stu-id="4523c-109">When the installer obtains an action name from the [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) function, or from a sequence table, it first searches for a standard action of that name.</span></span> <span data-ttu-id="4523c-110">S’il ne trouve pas l’action standard, le programme d’installation interroge la [table CustomAction](customaction-table.md) pour vérifier si l’action spécifiée est une action personnalisée.</span><span class="sxs-lookup"><span data-stu-id="4523c-110">If it cannot find the standard action, then the installer queries the [CustomAction table](customaction-table.md) to check if the specified action is a custom action.</span></span> <span data-ttu-id="4523c-111">Si l’action spécifiée n’est pas une action personnalisée, le programme d’installation interroge la [table de boîtes de dialogue](dialog-table.md) pour obtenir une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="4523c-111">If the specified action is not a custom action, then the installer queries the [Dialog table](dialog-table.md) for a dialog box.</span></span>

 

 



