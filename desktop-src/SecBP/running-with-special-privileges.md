---
description: Certaines fonctions requièrent des privilèges spéciaux pour s’exécuter correctement.
ms.assetid: b25db548-d5ab-4276-9b50-36d030909384
title: Exécution avec des privilèges spéciaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53be662d187ef27c7afc12b031f2d8de225d34c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541997"
---
# <a name="running-with-special-privileges"></a><span data-ttu-id="717eb-103">Exécution avec des privilèges spéciaux</span><span class="sxs-lookup"><span data-stu-id="717eb-103">Running with Special Privileges</span></span>

<span data-ttu-id="717eb-104">Certaines fonctions requièrent [des privilèges](/windows/desktop/SecAuthZ/privileges) spéciaux pour s’exécuter correctement.</span><span class="sxs-lookup"><span data-stu-id="717eb-104">Some functions require special [privileges](/windows/desktop/SecAuthZ/privileges) to run correctly.</span></span> <span data-ttu-id="717eb-105">Dans certains cas, la fonction ne peut être exécutée que par certains utilisateurs ou par les membres de certains groupes.</span><span class="sxs-lookup"><span data-stu-id="717eb-105">In some cases, the function can only be run by certain users or by members of certain groups.</span></span> <span data-ttu-id="717eb-106">L’exigence la plus courante est que l’utilisateur soit un administrateur local.</span><span class="sxs-lookup"><span data-stu-id="717eb-106">The most common requirement is that the user be a local administrator.</span></span> <span data-ttu-id="717eb-107">D’autres fonctions requièrent que le compte de l’utilisateur ait des privilèges spécifiques activés.</span><span class="sxs-lookup"><span data-stu-id="717eb-107">Other functions require the user's account to have specific privileges enabled.</span></span>

<span data-ttu-id="717eb-108">Pour réduire le risque que du code non autorisé soit en mesure d’accéder au contrôle, le système doit s’exécuter avec les privilèges minimum nécessaires.</span><span class="sxs-lookup"><span data-stu-id="717eb-108">To reduce the possibility of unauthorized code being able to get control, the system should run with the least privilege necessary.</span></span> <span data-ttu-id="717eb-109">Les applications qui doivent appeler des fonctions qui requièrent des privilèges spéciaux peuvent faire en sorte que le système soit ouvert aux attaques de pirates.</span><span class="sxs-lookup"><span data-stu-id="717eb-109">Applications that need to call functions that require special privileges can leave the system open to attack by hackers.</span></span> <span data-ttu-id="717eb-110">Ces applications doivent être conçues pour s’exécuter pendant de courtes périodes et doivent informer l’utilisateur des implications en matière de sécurité.</span><span class="sxs-lookup"><span data-stu-id="717eb-110">Such applications should be designed to run for short periods of time and should inform the user of the security implications involved.</span></span>

<span data-ttu-id="717eb-111">Pour plus d’informations sur l’exécution de en tant qu’utilisateur différent et sur l’activation des privilèges dans votre application, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="717eb-111">For information about how to run as different users and how to enable privileges in your application, see the following topics:</span></span><dl>

[<span data-ttu-id="717eb-112">Exécution avec des privilèges d’administrateur</span><span class="sxs-lookup"><span data-stu-id="717eb-112">Running with Administrator Privileges</span></span>](running-with-administrator-privileges.md)  
[<span data-ttu-id="717eb-113">Demande d’informations d’identification à l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="717eb-113">Asking the User for Credentials</span></span>](asking-the-user-for-credentials.md)  
[<span data-ttu-id="717eb-114">Modification des privilèges dans un jeton</span><span class="sxs-lookup"><span data-stu-id="717eb-114">Changing Privileges in a Token</span></span>](changing-privileges-in-a-token.md)  
[<span data-ttu-id="717eb-115">Attribution de privilèges à un compte</span><span class="sxs-lookup"><span data-stu-id="717eb-115">Assigning Privileges to an Account</span></span>](assigning-privileges-to-an-account.md)  
</dl>

 

 
