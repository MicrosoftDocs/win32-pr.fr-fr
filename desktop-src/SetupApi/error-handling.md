---
description: 'Trois fonctions génèrent des boîtes de dialogue pour gérer les erreurs : SetupCopyError, SetupDeleteError et SetupRenameError.'
ms.assetid: fcb310e1-5db7-47f3-b3d6-d528eb17e19a
title: Gestion des erreurs (API du programme d’installation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fb1347a3bec800200c2b6bda81e3f1eeeb866de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514220"
---
# <a name="error-handling-setup-api"></a><span data-ttu-id="98428-103">Gestion des erreurs (API du programme d’installation)</span><span class="sxs-lookup"><span data-stu-id="98428-103">Error Handling (Setup API)</span></span>

<span data-ttu-id="98428-104">Trois fonctions génèrent des boîtes de dialogue pour gérer les erreurs : [**SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora), [**SetupDeleteError**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora)et [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora).</span><span class="sxs-lookup"><span data-stu-id="98428-104">There are three functions that generate dialog boxes to handle errors: [**SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora), [**SetupDeleteError**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora), and [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora).</span></span>

<span data-ttu-id="98428-105">Les routines de rappel peuvent utiliser ces fonctions pour générer une interface utilisateur afin de gérer les notifications [**SPFILENOTIFY \_ COPYERROR**](spfilenotify-copyerror.md), [**SPFILENOTIFY \_ DELETEERROR**](spfilenotify-deleteerror.md)et [**SPFILENOTIFY \_ RENAMEERROR**](spfilenotify-renameerror.md) .</span><span class="sxs-lookup"><span data-stu-id="98428-105">Callback routines can use these functions to generate a user interface to handle [**SPFILENOTIFY\_COPYERROR**](spfilenotify-copyerror.md), [**SPFILENOTIFY\_DELETEERROR**](spfilenotify-deleteerror.md), and [**SPFILENOTIFY\_RENAMEERROR**](spfilenotify-renameerror.md) notifications.</span></span>

<span data-ttu-id="98428-106">Chacune de ces fonctions de gestion des erreurs génère une boîte de dialogue qui demande à l’utilisateur des informations sur la procédure à suivre.</span><span class="sxs-lookup"><span data-stu-id="98428-106">Each of these error-handling functions generates a dialog box that asks the user for information on how to proceed.</span></span> <span data-ttu-id="98428-107">Comme avec [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska), vous pouvez modifier la disposition et le comportement de la boîte de dialogue en spécifiant des indicateurs pendant l’appel de la fonction.</span><span class="sxs-lookup"><span data-stu-id="98428-107">As with [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska), you can modify the dialog box's layout and behavior by specifying flags during the function call.</span></span>

 

 



