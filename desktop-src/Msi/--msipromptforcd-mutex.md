---
description: Le \_ \_ mutex MsiPromptForCD existe quand le programme d’installation invite l’utilisateur à insérer un CD-ROM.
ms.assetid: f6319cda-48ac-4351-8eb5-f326490e3aff
title: Mutex __MsiPromptForCD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e646b23a003d10cce29807297e56abaebf3d935
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544811"
---
# <a name="__msipromptforcd-mutex"></a><span data-ttu-id="7dea5-103">\_\_Mutex MsiPromptForCD</span><span class="sxs-lookup"><span data-stu-id="7dea5-103">\_\_MsiPromptForCD Mutex</span></span>

<span data-ttu-id="7dea5-104">Le \_ \_ mutex MsiPromptForCD existe quand le programme d’installation invite l’utilisateur à insérer un CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="7dea5-104">The \_\_MsiPromptForCD Mutex exists when the installer prompts the user to insert a CD-ROM.</span></span> <span data-ttu-id="7dea5-105">Les programmes de lecture automatique doivent vérifier que le \_ \_ mutex MsiPromptForCD n’est pas actuellement défini avant le démarrage.</span><span class="sxs-lookup"><span data-stu-id="7dea5-105">Autoplay programs should check that the \_\_MsiPromptForCD mutex is not currently set before starting.</span></span> <span data-ttu-id="7dea5-106">Notez qu’il est possible qu’une invite de CD-ROM se produise avant que la clé en cours ou le \_ mutex MSIExecute existe.</span><span class="sxs-lookup"><span data-stu-id="7dea5-106">Note that it is possible for a CD-ROM prompt to occur before either the InProgress key or the \_MSIExecute Mutex exist.</span></span>

 

 



