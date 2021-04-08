---
description: API de gestion des informations d’identification
ms.assetid: e393041b-f10c-4053-bc6c-65a89f40e74f
title: API de gestion des informations d’identification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f3cae5054d0a32f42616f2845dcf18ab71ad0fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757288"
---
# <a name="credential-management-api"></a><span data-ttu-id="e1d80-103">API de gestion des informations d’identification</span><span class="sxs-lookup"><span data-stu-id="e1d80-103">Credential Management API</span></span>

<span data-ttu-id="e1d80-104">Les fonctions de gestion des informations d’identification constituent l’ensemble des fonctions qu’un gestionnaire d’informations d’identification doit implémenter.</span><span class="sxs-lookup"><span data-stu-id="e1d80-104">The credential management functions constitute the set of functions that a credential manager must implement.</span></span> <span data-ttu-id="e1d80-105">Celles-ci sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="e1d80-105">These are:</span></span>

-   <span data-ttu-id="e1d80-106">[**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify), une fonction de gestionnaire d’événements que le MPR appelle lorsqu’un utilisateur ouvre une session.</span><span class="sxs-lookup"><span data-stu-id="e1d80-106">[**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify), an event-handler function that the MPR calls when a user logs on.</span></span>
-   <span data-ttu-id="e1d80-107">[**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify), une fonction de gestionnaire d’événements que MPR appelle lorsqu’un mot de passe de compte est modifié.</span><span class="sxs-lookup"><span data-stu-id="e1d80-107">[**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify), an event-handler function the MPR calls when an account password is changed.</span></span>

<span data-ttu-id="e1d80-108">Les fonctions de gestion des informations d’identification sont toujours appelées dans le contexte du système (LocalSystem) plutôt que dans le contexte de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e1d80-108">The credential management functions are always called in the system context (LocalSystem) rather than the user context.</span></span>

<span data-ttu-id="e1d80-109">Pour plus d’informations sur la création et l’inscription d’une application Gestionnaire d’informations d’identification, consultez [implémentation d’un gestionnaire d’informations d’identification](implementing-a-credential-manager.md) et [inscription des fournisseurs de réseau et des gestionnaires d’informations d’identification](registering-network-providers-and-credential-managers.md).</span><span class="sxs-lookup"><span data-stu-id="e1d80-109">For more information about how to create and register a credential manager application, see [Implementing a Credential Manager](implementing-a-credential-manager.md) and [Registering Network Providers and Credential Managers](registering-network-providers-and-credential-managers.md).</span></span>

 

 



