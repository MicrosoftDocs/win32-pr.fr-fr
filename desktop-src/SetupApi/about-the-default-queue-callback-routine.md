---
description: La routine de rappel de file d’attente par défaut gère les notifications envoyées par SetupCommitFileQueue de manière générique.
ms.assetid: 6f2b3b9f-86e5-42af-8adc-29a1c768d106
title: À propos de la routine de rappel de file d’attente par défaut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57dfd22a9fa260aa1e98a2085e0cb925ed1f3438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862378"
---
# <a name="about-the-default-queue-callback-routine"></a><span data-ttu-id="7b5fd-103">À propos de la routine de rappel de file d’attente par défaut</span><span class="sxs-lookup"><span data-stu-id="7b5fd-103">About the Default Queue Callback Routine</span></span>

<span data-ttu-id="7b5fd-104">La routine de rappel de file d’attente par défaut gère les notifications envoyées par [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) de manière générique.</span><span class="sxs-lookup"><span data-stu-id="7b5fd-104">The default queue callback routine handles notifications sent by [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) in a generic manner.</span></span> <span data-ttu-id="7b5fd-105">À l’aide de la routine par défaut, vous disposez d’une interface utilisateur prête à l’emploi pour créer des boîtes de dialogue d’installation communes.</span><span class="sxs-lookup"><span data-stu-id="7b5fd-105">By using the default routine, you get a ready-made user interface to create common setup dialog boxes.</span></span> <span data-ttu-id="7b5fd-106">Il est recommandé d’utiliser la routine de rappel de file d’attente par défaut, à la fois pour faciliter l’utilisation et pour garantir une apparence et un comportement cohérents des boîtes de dialogue générées pendant l’installation.</span><span class="sxs-lookup"><span data-stu-id="7b5fd-106">It is recommended that you use the default queue callback routine, both for ease of use, and to ensure a consistent appearance and behavior of dialog boxes generated during the installation.</span></span>

<span data-ttu-id="7b5fd-107">La routine de rappel par défaut nécessite une structure de contexte pour assurer la conservation des enregistrements internes.</span><span class="sxs-lookup"><span data-stu-id="7b5fd-107">The default callback routine requires a context structure for internal record keeping.</span></span> <span data-ttu-id="7b5fd-108">En outre, la file d’attente transmet des informations supplémentaires relatives à la notification actuelle dans un ensemble de paramètres, *param1* et *param2*.</span><span class="sxs-lookup"><span data-stu-id="7b5fd-108">In addition, the queue passes additional information relevant to the current notification in a set of parameters, *Param1* and *Param2*.</span></span>

<span data-ttu-id="7b5fd-109">Par exemple, si la file d’attente envoie une \_ notification SPFILENOTIFY NEEDMEDIA à la routine de rappel par défaut, *param1* pointe vers une structure de [**\_ média source**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a) qui contient des informations sur les supports nécessaires et *param2* pointe vers un tableau de caractères qui peut recevoir de nouvelles informations de chemin d’accès de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7b5fd-109">For example, if the queue sends an SPFILENOTIFY\_NEEDMEDIA notification to the default callback routine, *Param1* points to a [**SOURCE\_MEDIA**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a) structure that contains information about the media needed, and *Param2* points to a character array that can receive new path information from the user.</span></span>

<span data-ttu-id="7b5fd-110">La routine de rappel par défaut utilise ces informations pour inviter l’utilisateur à insérer le média source nécessaire, à spécifier un nouveau chemin d’accès, à ignorer la copie du fichier actuel ou à annuler l’opération en cours.</span><span class="sxs-lookup"><span data-stu-id="7b5fd-110">The default callback routine uses this information to prompt the user to either insert the needed source media, specify a new path, skip copying the current file, or cancel the current operation.</span></span> <span data-ttu-id="7b5fd-111">La routine de rappel de file d’attente par défaut retourne FILEOP \_ NewPath, FILEOP \_ doit, FILEOP \_ Skip ou FILEOP \_ Abort dans la file d’attente, en fonction de l’action effectuée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7b5fd-111">The default queue callback routine returns FILEOP\_NEWPATH, FILEOP\_DOIT , FILEOP\_SKIP, or FILEOP\_ABORT to the queue, depending on which action the user took.</span></span>

<span data-ttu-id="7b5fd-112">Pour plus d’informations sur la façon dont la routine de rappel de file d’attente par défaut gère chaque notification de file d’attente, consultez [files d’attente de fichiers](file-queue-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="7b5fd-112">For information on how the default queue callback routine handles each queue notification, see [File Queue Notifications](file-queue-notifications.md).</span></span>

<span data-ttu-id="7b5fd-113">Pour plus d’informations sur les routines de rappel de file d’attente personnalisées, consultez [création d’une routine de rappel de file d’attente personnalisée](creating-a-custom-queue-callback-routine.md).</span><span class="sxs-lookup"><span data-stu-id="7b5fd-113">For information on custom queue callback routines, see [Creating a Custom Queue Callback Routine](creating-a-custom-queue-callback-routine.md).</span></span>

 

 



