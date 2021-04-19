---
description: L’action LaunchConditions interroge la table LaunchCondition et évalue chaque instruction conditionnelle enregistrée ici. Si l’une de ces instructions conditionnelles échoue, un message d’erreur s’affiche pour l’utilisateur et l’installation est interrompue.
ms.assetid: b356987d-3efe-4a57-a745-91a1b34222e9
title: Action LaunchConditions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f6bb3eaf2a98c630bb9cacd18ff449083eb9c1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543456"
---
# <a name="launchconditions-action"></a><span data-ttu-id="1d745-104">Action LaunchConditions</span><span class="sxs-lookup"><span data-stu-id="1d745-104">LaunchConditions Action</span></span>

<span data-ttu-id="1d745-105">L’action LaunchConditions interroge la [table LaunchCondition](launchcondition-table.md) et évalue chaque instruction conditionnelle enregistrée ici.</span><span class="sxs-lookup"><span data-stu-id="1d745-105">The LaunchConditions action queries the [LaunchCondition table](launchcondition-table.md) and evaluates each conditional statement recorded there.</span></span> <span data-ttu-id="1d745-106">Si l’une de ces instructions conditionnelles échoue, un message d’erreur s’affiche pour l’utilisateur et l’installation est interrompue.</span><span class="sxs-lookup"><span data-stu-id="1d745-106">If any of these conditional statements fail, an error message is displayed to the user and the installation is terminated.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="1d745-107">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="1d745-107">Sequence Restrictions</span></span>

<span data-ttu-id="1d745-108">L’action LaunchConditions est facultative.</span><span class="sxs-lookup"><span data-stu-id="1d745-108">The LaunchConditions action is optional.</span></span> <span data-ttu-id="1d745-109">Cette action est normalement la première dans la séquence, mais l' [action AppSearch](appsearch-action.md) peut être séquencée avant l’action LaunchConditions.</span><span class="sxs-lookup"><span data-stu-id="1d745-109">This action is normally the first in the sequence, but the [AppSearch Action](appsearch-action.md) may be sequenced before the LaunchConditions action.</span></span> <span data-ttu-id="1d745-110">Si des conditions de lancement ne s’appliquent pas à tous les modes d’installation, la propriété du mode d’installation appropriée doit être utilisée dans une expression conditionnelle dans la table de séquences appropriée.</span><span class="sxs-lookup"><span data-stu-id="1d745-110">If there are launch conditions that do not apply to all installation modes, the appropriate installation mode property should be used in a conditional expression in the appropriate sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="1d745-111">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="1d745-111">ActionData Messages</span></span>

<span data-ttu-id="1d745-112">Il n’y a aucun message ActionData.</span><span class="sxs-lookup"><span data-stu-id="1d745-112">There are no ActionData messages.</span></span>

 

 



