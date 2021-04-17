---
description: Filtres de mot de passe
ms.assetid: 777edb4d-1fb4-4269-8382-8fe73c0c3b23
title: Filtres de mot de passe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14f76aad9bb2bb722fe7f84b13dc6b5a6bdb7eb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210426"
---
# <a name="password-filters"></a><span data-ttu-id="504f6-103">Filtres de mot de passe</span><span class="sxs-lookup"><span data-stu-id="504f6-103">Password Filters</span></span>

<span data-ttu-id="504f6-104">Les filtres de mot de passe vous permettent d’implémenter une stratégie de mot de passe et une notification de modification.</span><span class="sxs-lookup"><span data-stu-id="504f6-104">Password filters provide a way for you to implement password policy and change notification.</span></span>

<span data-ttu-id="504f6-105">Quand une demande de modification de mot de passe est effectuée, l' [*autorité de sécurité locale*](/windows/desktop/SecGloss/l-gly) (LSA) appelle les filtres de mot de passe inscrits sur le système.</span><span class="sxs-lookup"><span data-stu-id="504f6-105">When a password change request is made, the [*Local Security Authority*](/windows/desktop/SecGloss/l-gly) (LSA) calls the password filters registered on the system.</span></span> <span data-ttu-id="504f6-106">Chaque filtre de mot de passe est appelé deux fois : tout d’abord pour valider le nouveau mot de passe, puis, une fois que tous les filtres ont validé le nouveau mot de passe, pour informer les filtres que la modification a été apportée.</span><span class="sxs-lookup"><span data-stu-id="504f6-106">Each password filter is called twice: first to validate the new password and then, after all filters have validated the new password, to notify the filters that the change has been made.</span></span> <span data-ttu-id="504f6-107">L'illustration ci-dessous montre ce processus.</span><span class="sxs-lookup"><span data-stu-id="504f6-107">The following illustration shows this process.</span></span>

![demande de modification de mot de passe](images/pswdfilte.png)

<span data-ttu-id="504f6-109">La notification de modification de mot de passe est utilisée pour synchroniser les modifications de mot de passe dans les bases de données de comptes.</span><span class="sxs-lookup"><span data-stu-id="504f6-109">Password change notification is used to synchronize password changes to foreign account databases.</span></span>

<span data-ttu-id="504f6-110">Les filtres de mot de passe sont utilisés pour appliquer la stratégie de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="504f6-110">Password filters are used to enforce password policy.</span></span> <span data-ttu-id="504f6-111">Les filtres valident les nouveaux mots de passe et indiquent si le nouveau mot de passe est conforme à la stratégie de mot de passe implémentée.</span><span class="sxs-lookup"><span data-stu-id="504f6-111">Filters validate new passwords and indicate whether the new password conforms to the implemented password policy.</span></span>

<span data-ttu-id="504f6-112">Pour une vue d’ensemble de l’utilisation des filtres de mot de passe, consultez [utilisation de filtres de mot de passe](using-password-filters.md).</span><span class="sxs-lookup"><span data-stu-id="504f6-112">For an overview of using password filters, see [Using Password Filters](using-password-filters.md).</span></span>

<span data-ttu-id="504f6-113">Pour obtenir la liste des fonctions de filtre de mot de passe, consultez [fonctions de filtre de mot de passe](management-functions.md).</span><span class="sxs-lookup"><span data-stu-id="504f6-113">For a list of password filter functions, see [Password Filter Functions](management-functions.md).</span></span>

<span data-ttu-id="504f6-114">Les rubriques suivantes fournissent des informations supplémentaires sur les filtres de mot de passe :</span><span class="sxs-lookup"><span data-stu-id="504f6-114">The following topics provide more information about password filters:</span></span>

-   [<span data-ttu-id="504f6-115">Considérations sur la programmation du filtre de mot de passe</span><span class="sxs-lookup"><span data-stu-id="504f6-115">Password Filter Programming Considerations</span></span>](password-filter-programming-considerations.md)
-   [<span data-ttu-id="504f6-116">Mise en œuvre des mots de passe forts et Passfilt.dll</span><span class="sxs-lookup"><span data-stu-id="504f6-116">Strong Password Enforcement and Passfilt.dll</span></span>](strong-password-enforcement-and-passfilt-dll.md)

 

 
