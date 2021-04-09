---
description: L’action DisableRollback désactive la restauration pour le reste de l’installation.
ms.assetid: 5510b393-1f2e-44ba-97f5-663674d55b20
title: Action DisableRollback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 740e838a6dca2d97db616703faf24c590ab69bc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113866"
---
# <a name="disablerollback-action"></a><span data-ttu-id="d2ef7-103">Action DisableRollback</span><span class="sxs-lookup"><span data-stu-id="d2ef7-103">DisableRollback Action</span></span>

<span data-ttu-id="d2ef7-104">L’action DisableRollback désactive la [restauration](rollback-installation.md) pour le reste de l’installation.</span><span class="sxs-lookup"><span data-stu-id="d2ef7-104">The DisableRollback Action disables [rollback](rollback-installation.md) for the remainder of the installation.</span></span> <span data-ttu-id="d2ef7-105">La restauration est désactivée uniquement pour les actions qui sont séquencées après l’action DisableRollback dans les tables de séquence.</span><span class="sxs-lookup"><span data-stu-id="d2ef7-105">Rollback is disabled only for the actions that are sequenced after the DisableRollback action in the sequence tables.</span></span> <span data-ttu-id="d2ef7-106">La restauration est désactivée pour l’ensemble de l’installation si l’action DisableRollback est séquencée avant l' [action InstallInitialize](installinitialize-action.md).</span><span class="sxs-lookup"><span data-stu-id="d2ef7-106">Rollback is disabled for the entire installation if the DisableRollback action is sequenced before the [InstallInitialize action](installinitialize-action.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="d2ef7-107">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="d2ef7-107">Sequence Restrictions</span></span>

<span data-ttu-id="d2ef7-108">Il n’existe aucune restriction de séquence.</span><span class="sxs-lookup"><span data-stu-id="d2ef7-108">There are no sequence restrictions.</span></span>

## <a name="actiondata-message"></a><span data-ttu-id="d2ef7-109">Message ActionData</span><span class="sxs-lookup"><span data-stu-id="d2ef7-109">ActionData Message</span></span>

<span data-ttu-id="d2ef7-110">Il n’y a aucun message ActionData.</span><span class="sxs-lookup"><span data-stu-id="d2ef7-110">There are no ActionData messages.</span></span>

 

 



