---
description: Considérations sur la sécurité de COM+ CRM
ms.assetid: e212c847-b43b-43be-b089-82336551b89a
title: Considérations sur la sécurité de COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2ababde9f31c0c2655fbf4f0c46b216ca0cbfee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110406"
---
# <a name="com-crm-security-considerations"></a><span data-ttu-id="2975e-103">Considérations sur la sécurité de COM+ CRM</span><span class="sxs-lookup"><span data-stu-id="2975e-103">COM+ CRM Security Considerations</span></span>

<span data-ttu-id="2975e-104">Un fichier journal CRM peut contenir des informations sensibles qui doivent être sécurisées.</span><span class="sxs-lookup"><span data-stu-id="2975e-104">A CRM log file could contain sensitive information that must be secured.</span></span> <span data-ttu-id="2975e-105">Pour cette raison, si l’application serveur s’exécute sous une identité autre que l’utilisateur interactif lors de la création du fichier journal CRM, le fichier journal CRM est protégé par la sécurité pour cet utilisateur uniquement.</span><span class="sxs-lookup"><span data-stu-id="2975e-105">For this reason, if the server application is running under any identity other than Interactive User when the CRM log file is first created, the CRM log file is security protected for that user only.</span></span> <span data-ttu-id="2975e-106">Cette fonctionnalité est disponible uniquement sur le système de fichiers NTFS.</span><span class="sxs-lookup"><span data-stu-id="2975e-106">This feature is available only on the NTFS file system.</span></span> <span data-ttu-id="2975e-107">Si l’identité de l’application serveur est modifiée par la suite, les informations de sécurité du fichier journal CRM ne sont pas automatiquement modifiées.</span><span class="sxs-lookup"><span data-stu-id="2975e-107">If the identity of the server application is subsequently changed, the security information for the CRM log file is not automatically changed.</span></span> <span data-ttu-id="2975e-108">Il peut être modifié manuellement à l’aide des outils d’administration Windows existants.</span><span class="sxs-lookup"><span data-stu-id="2975e-108">It can be changed manually by using existing Windows administration tools.</span></span> <span data-ttu-id="2975e-109">L’alternative consiste simplement à supprimer le fichier journal CRM lorsqu’il est dans un état propre (ce qui est attendu après un arrêt contrôlé de l’application serveur).</span><span class="sxs-lookup"><span data-stu-id="2975e-109">The alternative is simply to delete the CRM log file when it is in a clean state (which is expected after a controlled shutdown of the server application).</span></span>

<span data-ttu-id="2975e-110">En fonctionnement normal, COM+ crée le composant CRM Compensator et appelle l’interface [**ICrmCompensator**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator) .</span><span class="sxs-lookup"><span data-stu-id="2975e-110">In normal operation, COM+ creates the CRM compensator component and calls the [**ICrmCompensator**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator) interface.</span></span> <span data-ttu-id="2975e-111">Toutefois, un utilisateur disposant de privilèges pour créer le compensateur CRM peut appeler l’interface **ICrmCompensator** à des moments inappropriés, ce qui peut entraîner des problèmes de sécurité système.</span><span class="sxs-lookup"><span data-stu-id="2975e-111">However, a user having privileges to create the CRM Compensator can call the **ICrmCompensator** interface at inappropriate times, possibly causing system security problems.</span></span> <span data-ttu-id="2975e-112">Pour vous protéger contre ces problèmes de sécurité, l’administrateur système peut utiliser la sécurité basée sur les rôles pour limiter le composant CRM Compensator aux seules identités des applications serveur dans lesquelles il s’exécute.</span><span class="sxs-lookup"><span data-stu-id="2975e-112">To help protect against these security problems, the system administrator can use role-based security to restrict the CRM Compensator component to only those identities of the server applications in which it runs.</span></span> <span data-ttu-id="2975e-113">Si le composant s’exécute dans une application de bibliothèque, cela inclut toutes les identités des applications serveur.</span><span class="sxs-lookup"><span data-stu-id="2975e-113">If the component is running in a library application, this would include all the identities of the server applications.</span></span>

> [!Note]  
> <span data-ttu-id="2975e-114">À partir de Windows Server 2003, afin d’empêcher l’activation à partir de l’extérieur de l’application serveur, il est possible de garantir un système plus sécurisé en marquant le composant CRM Compensator comme privé.</span><span class="sxs-lookup"><span data-stu-id="2975e-114">Starting with Windows Server 2003, to help prevent activation from outside the server application, it is possible to further ensure a more secure system by marking the CRM Compensator component as private.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="2975e-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2975e-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2975e-116">Concepts de Gestionnaire des ressources de compensation COM+</span><span class="sxs-lookup"><span data-stu-id="2975e-116">COM+ Compensating Resource Manager Concepts</span></span>](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



