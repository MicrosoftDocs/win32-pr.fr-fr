---
description: Le Windows Installer traite les actions personnalisées en tant que thread distinct de l’installation principale.
ms.assetid: 6451029c-87f4-44ee-aa2b-cc9a1c25bcc0
title: Actions personnalisées synchrones et asynchrones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 067c5b40840269f3a0393faee8fe670f5e522c7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517723"
---
# <a name="synchronous-and-asynchronous-custom-actions"></a><span data-ttu-id="0f8f3-103">Actions personnalisées synchrones et asynchrones</span><span class="sxs-lookup"><span data-stu-id="0f8f3-103">Synchronous and Asynchronous Custom Actions</span></span>

<span data-ttu-id="0f8f3-104">Le Windows Installer traite les actions personnalisées en tant que thread distinct de l’installation principale.</span><span class="sxs-lookup"><span data-stu-id="0f8f3-104">The Windows Installer processes custom actions as a separate thread from the main installation.</span></span> <span data-ttu-id="0f8f3-105">Pendant l’exécution synchrone d’une action personnalisée, le programme d’installation attend que le thread de l’action personnalisée se termine avant de poursuivre l’installation principale.</span><span class="sxs-lookup"><span data-stu-id="0f8f3-105">During synchronous execution of a custom action, the installer waits for the thread of the custom action to complete before continuing the main installation.</span></span> <span data-ttu-id="0f8f3-106">Pendant l’exécution asynchrone, le programme d’installation exécute l’action personnalisée simultanément lorsque l’installation actuelle se poursuit.</span><span class="sxs-lookup"><span data-stu-id="0f8f3-106">During asynchronous execution, the installer runs the custom action simultaneously as the current installation continues.</span></span> <span data-ttu-id="0f8f3-107">Les auteurs des actions personnalisées doivent donc connaître les threads asynchrones qui peuvent apporter des modifications à la base de données d’installation entre les appels de fonction.</span><span class="sxs-lookup"><span data-stu-id="0f8f3-107">Authors of custom actions must therefore be aware of any asynchronous threads that may be making changes to the installation database between function calls.</span></span>

<span data-ttu-id="0f8f3-108">En particulier, les appels à [**MsiGetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) et [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha) doivent être évités dans les actions personnalisées asynchrones.</span><span class="sxs-lookup"><span data-stu-id="0f8f3-108">In particular, calls to [**MsiGetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) and [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha) should be avoided in asynchronous custom actions.</span></span> <span data-ttu-id="0f8f3-109">Utilisez plutôt [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) pour obtenir un chemin d’accès cible.</span><span class="sxs-lookup"><span data-stu-id="0f8f3-109">Instead use [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) to obtain a target path.</span></span> <span data-ttu-id="0f8f3-110">Les opérations de base de données en bloc, telles que les opérations d’importation, d’exportation et de transformation, doivent être évitées dans n’importe quel type d’action personnalisée.</span><span class="sxs-lookup"><span data-stu-id="0f8f3-110">Bulk database operations such as import, export, and transform operations should be avoided in any type of custom action.</span></span>

<span data-ttu-id="0f8f3-111">Les indicateurs d’option peuvent être définis dans le champ type de la [table CustomAction](customaction-table.md) pour spécifier que les threads d’action principal et personnalisé s’exécutent de façon synchrone ou asynchrone.</span><span class="sxs-lookup"><span data-stu-id="0f8f3-111">Option flags can be set in the Type field of the [CustomAction table](customaction-table.md) to specify that the main and custom action threads run synchronously or asynchronously.</span></span> <span data-ttu-id="0f8f3-112">Consultez [options de traitement des retours d’actions personnalisées](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="0f8f3-112">See [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

<span data-ttu-id="0f8f3-113">Le programme d’installation peut uniquement exécuter des actions [personnalisées Rollback](rollback-custom-actions.md) et des actions d' [installation simultanées](concurrent-installations.md) en tant qu’actions personnalisées synchrones.</span><span class="sxs-lookup"><span data-stu-id="0f8f3-113">The installer can only execute [Rollback Custom Actions](rollback-custom-actions.md) and [Concurrent Installation](concurrent-installations.md) actions as synchronous custom actions.</span></span>

 

 



