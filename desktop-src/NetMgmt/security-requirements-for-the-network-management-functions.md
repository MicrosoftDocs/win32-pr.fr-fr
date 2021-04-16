---
title: Exigences de sécurité pour la fonction de gestion de réseau
description: L’appel de certaines fonctions de gestion de réseau ne nécessite pas d’appartenance de groupe spéciale.
ms.assetid: 846a5b81-d5bf-4275-a898-38e6ba308b8f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b5b0987509294f03b8737aae5e721abf5dbdd90
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104508081"
---
# <a name="network-management-function-security-requirements"></a><span data-ttu-id="69cfd-103">Exigences de sécurité pour la fonction de gestion de réseau</span><span class="sxs-lookup"><span data-stu-id="69cfd-103">Network management function security requirements</span></span>

<span data-ttu-id="69cfd-104">L’appel de certaines fonctions de gestion de réseau ne nécessite pas d’appartenance de groupe spéciale.</span><span class="sxs-lookup"><span data-stu-id="69cfd-104">Calling some of the network management functions does not require special group membership.</span></span> <span data-ttu-id="69cfd-105">D’autres fonctions requièrent que les utilisateurs disposent d’un niveau de privilège spécifique pour s’exécuter avec succès.</span><span class="sxs-lookup"><span data-stu-id="69cfd-105">Other functions require that users have a specific privilege level to execute successfully.</span></span> <span data-ttu-id="69cfd-106">Le cas échéant, la section Notes sur la page de référence d’une fonction indique le niveau de privilège qu’un utilisateur doit avoir pour exécuter la fonction particulière.</span><span class="sxs-lookup"><span data-stu-id="69cfd-106">When applicable, the Remarks section on a function's reference page indicates the privilege level a user must have to execute the particular function.</span></span>

<span data-ttu-id="69cfd-107">Les exigences de sécurité qui s’appliquent à Active Directory contrôleurs de domaine peuvent différer de celles qui s’appliquent aux serveurs et aux stations de travail.</span><span class="sxs-lookup"><span data-stu-id="69cfd-107">Security requirements that apply to Active Directory domain controllers can differ from those that apply to servers and workstations.</span></span>

<span data-ttu-id="69cfd-108">Pour plus d’informations et pour obtenir la liste des fonctions affectées, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="69cfd-108">For more information, and a list of affected functions, see the following topics:</span></span>

-   [<span data-ttu-id="69cfd-109">Configuration requise pour les fonctions de gestion de réseau sur les contrôleurs de domaine Active Directory</span><span class="sxs-lookup"><span data-stu-id="69cfd-109">Requirements for Network Management functions on Active Directory domain controllers</span></span>](requirements-for-network-management-functions-on-active-directory-domain-controllers.md)
-   [<span data-ttu-id="69cfd-110">Configuration requise pour les fonctions de gestion de réseau sur les serveurs et les stations de travail</span><span class="sxs-lookup"><span data-stu-id="69cfd-110">Requirements for Network Management functions on servers and workstations</span></span>](requirements-for-network-management-functions-on-servers-and-workstations.md)

<span data-ttu-id="69cfd-111">Pour plus d’informations sur le contrôle de l’accès aux objets sécurisables, consultez [Access Control](/windows/desktop/SecAuthZ/access-control), [privilèges](/windows/desktop/SecAuthZ/privileges)et [objets sécurisables](/windows/desktop/SecAuthZ/securable-objects).</span><span class="sxs-lookup"><span data-stu-id="69cfd-111">For more information about controlling access to securable objects, see [Access Control](/windows/desktop/SecAuthZ/access-control), [Privileges](/windows/desktop/SecAuthZ/privileges), and [Securable Objects](/windows/desktop/SecAuthZ/securable-objects).</span></span>

<span data-ttu-id="69cfd-112">Pour plus d’informations sur les descripteurs de sécurité spécifiques utilisés pendant les contrôles d’accès, consultez la page de référence des fonctions individuelles.</span><span class="sxs-lookup"><span data-stu-id="69cfd-112">For more information about specific security descriptors that are used during access checks, see the individual function reference page.</span></span> <span data-ttu-id="69cfd-113">Pour plus d’informations sur l’appel de fonctions qui requièrent des privilèges d’administrateur, consultez [exécution avec des privilèges spéciaux](/windows/desktop/SecBP/running-with-special-privileges).</span><span class="sxs-lookup"><span data-stu-id="69cfd-113">For more information about calling functions that require administrator privileges, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span>

 

 