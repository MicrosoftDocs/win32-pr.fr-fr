---
description: Dans un contrôle d’accès, le système compare les informations de sécurité dans le jeton d’accès threads aux informations de sécurité contenues dans le descripteur de sécurité des objets.
ms.assetid: 40871179-d383-43d0-810d-0805c88dbbd6
title: Interaction entre les threads et les objets sécurisables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f3e2b18f707ece4d651eeca1c6897bb67aad334
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867809"
---
# <a name="interaction-between-threads-and-securable-objects"></a><span data-ttu-id="5d2a8-103">Interaction entre les threads et les objets sécurisables</span><span class="sxs-lookup"><span data-stu-id="5d2a8-103">Interaction Between Threads and Securable Objects</span></span>

<span data-ttu-id="5d2a8-104">Quand un thread tente d’utiliser un [objet sécurisable](securable-objects.md), le système effectue une vérification d’accès avant d’autoriser le thread à continuer.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-104">When a thread attempts to use a [securable object](securable-objects.md), the system performs an access check before allowing the thread to proceed.</span></span> <span data-ttu-id="5d2a8-105">Dans un contrôle d’accès, le système compare les informations de sécurité dans le [*jeton d’accès*](/windows/desktop/SecGloss/a-gly) du thread aux informations de sécurité dans le [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly)de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-105">In an access check, the system compares the security information in the thread's [*access token*](/windows/desktop/SecGloss/a-gly) against the security information in the object's [*security descriptor*](/windows/desktop/SecGloss/s-gly).</span></span>

-   <span data-ttu-id="5d2a8-106">Le jeton d’accès contient des [*identificateurs de sécurité*](/windows/desktop/SecGloss/s-gly) (SID) qui identifient l’utilisateur associé au thread.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-106">The access token contains [*security identifiers*](/windows/desktop/SecGloss/s-gly) (SIDs) that identify the user associated with the thread.</span></span>
-   <span data-ttu-id="5d2a8-107">Le descripteur de sécurité identifie le propriétaire de l’objet et contient une liste de contrôle d’accès discrétionnaire (DACL, [*Discretionary Access Control List*](/windows/desktop/SecGloss/d-gly) ).</span><span class="sxs-lookup"><span data-stu-id="5d2a8-107">The security descriptor identifies the object's owner and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL).</span></span> <span data-ttu-id="5d2a8-108">La liste DACL contient des [*entrées de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACE), chacune spécifiant les droits d’accès accordés ou refusés à un utilisateur ou à un groupe spécifique.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-108">The DACL contains [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs), each of which specify the access rights allowed or denied to a specific user or group.</span></span>

<span data-ttu-id="5d2a8-109">Le système vérifie la liste DACL de l’objet, en recherchant les entrées de contrôle d’accès qui s’appliquent aux SID d’utilisateur et de groupe à partir du jeton d’accès du thread.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-109">The system checks the object's DACL, looking for ACEs that apply to the user and group SIDs from the thread's access token.</span></span> <span data-ttu-id="5d2a8-110">Le système vérifie chaque ACE jusqu’à ce que l’accès soit accordé ou refusé, ou jusqu’à ce qu’il n’y ait plus de ACE à vérifier.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-110">The system checks each ACE until access is either granted or denied or until there are no more ACEs to check.</span></span> <span data-ttu-id="5d2a8-111">En théorie, une [*liste de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACL) peut avoir plusieurs entrées de contrôle d’accès (ACE) qui s’appliquent aux SID du jeton.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-111">Conceivably, an [*access control list*](/windows/desktop/SecGloss/a-gly) (ACL) could have several ACEs that apply to the token's SIDs.</span></span> <span data-ttu-id="5d2a8-112">Et, si cela se produit, les droits d’accès accordés par chaque ACE s’accumulent.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-112">And, if this occurs, the access rights granted by each ACE accumulate.</span></span> <span data-ttu-id="5d2a8-113">Par exemple, si une entrée de contrôle d’accès accorde l’accès en lecture à un groupe et qu’une autre entrée de contrôle d’accès accorde l’accès en écriture à un utilisateur membre du groupe, l’utilisateur peut avoir un accès en lecture et en écriture à l’objet.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-113">For example, if one ACE grants read access to a group and another ACE grants write access to a user who is a member of the group, the user can have both read and write access to the object.</span></span>

<span data-ttu-id="5d2a8-114">L’illustration suivante montre la relation entre ces blocs d’informations de sécurité :</span><span class="sxs-lookup"><span data-stu-id="5d2a8-114">The following illustration shows the relationship between these blocks of security information:</span></span>

![relations entre les processus, les ACE et les DACL](images/cssec-02.png)

 

 
