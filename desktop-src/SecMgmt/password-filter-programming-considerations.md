---
description: Explique les considérations relatives à l’implémentation des fonctions d’exportation du filtre de mot de passe.
ms.assetid: ec7c1e7e-844a-43d4-b756-02bc1062d7b8
title: Considérations sur la programmation du filtre de mot de passe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad13a52f66c29142248ca07179d8692887b1acb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512949"
---
# <a name="password-filter-programming-considerations"></a><span data-ttu-id="748f4-103">Considérations sur la programmation du filtre de mot de passe</span><span class="sxs-lookup"><span data-stu-id="748f4-103">Password Filter Programming Considerations</span></span>

<span data-ttu-id="748f4-104">Lorsque vous implémentez des fonctions d’exportation du [*filtre de mot de passe*](/windows/desktop/SecGloss/p-gly) , gardez à l’esprit les points suivants :</span><span class="sxs-lookup"><span data-stu-id="748f4-104">When implementing [*password filter*](/windows/desktop/SecGloss/p-gly) export functions, keep the following considerations in mind:</span></span>

-   <span data-ttu-id="748f4-105">Soyez très prudent lorsque vous utilisez des mots de passe en [*texte clair*](/windows/desktop/SecGloss/p-gly) .</span><span class="sxs-lookup"><span data-stu-id="748f4-105">Take great care when working with [*plaintext*](/windows/desktop/SecGloss/p-gly) passwords.</span></span> <span data-ttu-id="748f4-106">L’envoi de mots de passe en texte clair sur des réseaux peut compromettre la sécurité.</span><span class="sxs-lookup"><span data-stu-id="748f4-106">Sending plaintext passwords over networks could compromise security.</span></span> <span data-ttu-id="748f4-107">Le réseau « renifleurs » peut facilement surveiller le trafic de mot de passe en texte clair.</span><span class="sxs-lookup"><span data-stu-id="748f4-107">Network "sniffers" can easily watch for plaintext password traffic.</span></span>
-   <span data-ttu-id="748f4-108">Effacez toute la mémoire utilisée pour stocker les mots de passe en appelant la fonction [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) avant de libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="748f4-108">Erase all memory used to store passwords by calling the [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) function before freeing memory.</span></span>
-   <span data-ttu-id="748f4-109">Toutes les mémoires tampons transmises dans la notification de mot de passe et les routines de filtre doivent être traitées en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="748f4-109">All buffers passed into password notification and filter routines should be treated as read-only.</span></span> <span data-ttu-id="748f4-110">L’écriture de données dans ces mémoires tampons peut provoquer un comportement instable.</span><span class="sxs-lookup"><span data-stu-id="748f4-110">Writing data to these buffers may cause unstable behavior.</span></span>
-   <span data-ttu-id="748f4-111">Toutes les routines de filtrage et de notification de mot de passe doivent être thread-safe.</span><span class="sxs-lookup"><span data-stu-id="748f4-111">All password notification and filter routines should be thread-safe.</span></span> <span data-ttu-id="748f4-112">Utilisez des sections critiques ou d’autres techniques de programmation synchrones pour protéger les données le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="748f4-112">Use critical sections or other synchronous programming techniques to protect data where appropriate.</span></span>
-   <span data-ttu-id="748f4-113">La notification et le filtrage de mot de passe s’effectuent uniquement sur l’ordinateur qui héberge le compte.</span><span class="sxs-lookup"><span data-stu-id="748f4-113">Password notification and filtering take place only on the computer that houses the account.</span></span>
-   <span data-ttu-id="748f4-114">Tous les contrôleurs de domaine sont accessibles en écriture. par conséquent, les packages de filtre de mot de passe doivent être présents sur tous les contrôleurs de domaine.</span><span class="sxs-lookup"><span data-stu-id="748f4-114">All domain controllers are writeable, therefore password filter packages must be present on all domain controllers.</span></span>

    <span data-ttu-id="748f4-115">**Domaines Windows NT 4,0 :** La notification sur les comptes de domaine s’effectue uniquement sur le contrôleur de domaine principal.</span><span class="sxs-lookup"><span data-stu-id="748f4-115">**Windows NT 4.0 domains:** Notification on domain accounts takes place only on the primary domain controller.</span></span> <span data-ttu-id="748f4-116">En plus du contrôleur de domaine principal, les packages de filtre de mot de passe doivent être installés sur tous les contrôleurs de domaine de sauvegarde pour permettre aux notifications de continuer en cas de modification du rôle de serveur.</span><span class="sxs-lookup"><span data-stu-id="748f4-116">In addition to the primary domain controller, the password filter packages should be installed on all backup domain controllers to allow notifications to continue in the event of server role changes.</span></span>

-   <span data-ttu-id="748f4-117">Toutes les dll de filtre de mot de passe s’exécutent dans le [*contexte de sécurité*](/windows/desktop/SecGloss/s-gly) du compte système local.</span><span class="sxs-lookup"><span data-stu-id="748f4-117">All password filter DLLs run in the [*security context*](/windows/desktop/SecGloss/s-gly) of the local system account.</span></span>



| <span data-ttu-id="748f4-118">Pour obtenir des informations sur</span><span class="sxs-lookup"><span data-stu-id="748f4-118">For information about</span></span>                                                                                                                     | <span data-ttu-id="748f4-119">Consultez</span><span class="sxs-lookup"><span data-stu-id="748f4-119">See</span></span>                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="748f4-120">Comment installer et inscrire votre propre dll [*de filtre de mots de passe*](/windows/desktop/SecGloss/p-gly) .</span><span class="sxs-lookup"><span data-stu-id="748f4-120">How to install and register your own [*password filter*](/windows/desktop/SecGloss/p-gly) DLL.</span></span> | [<span data-ttu-id="748f4-121">Installation et inscription d’une DLL de filtre de mot de passe</span><span class="sxs-lookup"><span data-stu-id="748f4-121">Installing and Registering a Password Filter DLL</span></span>](installing-and-registering-a-password-filter-dll.md) |
| <span data-ttu-id="748f4-122">DLL de filtre de mots de passe fournie par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="748f4-122">The password filter DLL provided by Microsoft.</span></span>                                                                                            | [<span data-ttu-id="748f4-123">Mise en œuvre des mots de passe forts et Passfilt.dll</span><span class="sxs-lookup"><span data-stu-id="748f4-123">Strong Password Enforcement and Passfilt.dll</span></span>](strong-password-enforcement-and-passfilt-dll.md)         |
| <span data-ttu-id="748f4-124">Fonctions d’exportation implémentées par une DLL de filtre de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="748f4-124">Export functions implemented by a password filter DLL.</span></span>                                                                                    | [<span data-ttu-id="748f4-125">Fonctions de filtre de mot de passe</span><span class="sxs-lookup"><span data-stu-id="748f4-125">Password Filter Functions</span></span>](management-functions.md)                          |



 

 

 
