---
description: Informations de contexte de l’appel de sécurité
ms.assetid: 8b170c17-f095-4c25-9ee2-480681b7e5f6
title: Informations de contexte de l’appel de sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 213e21d684d004ed18e5b9aa536e03ae8292307e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201119"
---
# <a name="security-call-context-information"></a><span data-ttu-id="0f831-103">Informations de contexte de l’appel de sécurité</span><span class="sxs-lookup"><span data-stu-id="0f831-103">Security Call Context Information</span></span>

<span data-ttu-id="0f831-104">La sécurité basée sur les rôles repose sur un mécanisme général qui vous permet de récupérer des informations de sécurité concernant tous les appelants en amont dans la chaîne d’appels à votre composant.</span><span class="sxs-lookup"><span data-stu-id="0f831-104">Role-based security is built on a general mechanism that enables you to retrieve security information regarding all upstream callers in the chain of calls to your component.</span></span> <span data-ttu-id="0f831-105">Ces informations sont disponibles uniquement si vous avez activé la vérification des rôles au niveau du composant.</span><span class="sxs-lookup"><span data-stu-id="0f831-105">This information is available only when you have component-level role checking enabled.</span></span> <span data-ttu-id="0f831-106">Pour plus d’informations sur la façon de définir la sécurité au niveau du composant, consultez [définition d’un niveau de sécurité pour les vérifications d’accès](setting-a-security-level-for-access-checks.md).</span><span class="sxs-lookup"><span data-stu-id="0f831-106">For details about how to set component-level security, see [Setting a Security Level for Access Checks](setting-a-security-level-for-access-checks.md).</span></span>

<span data-ttu-id="0f831-107">Vous pouvez utiliser l’interface [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) pour accéder aux informations de contexte de l’appel de sécurité par programme.</span><span class="sxs-lookup"><span data-stu-id="0f831-107">You can use the [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) interface to access security call context information programmatically.</span></span> <span data-ttu-id="0f831-108">Pour obtenir une description, consultez [sécurité des composants de programmation](programmatic-component-security.md).</span><span class="sxs-lookup"><span data-stu-id="0f831-108">For a description, see [Programmatic Component Security](programmatic-component-security.md).</span></span>

<span data-ttu-id="0f831-109">Le contexte de l’appel de sécurité est passé chaque fois qu’une limite de sécurité est franchie.</span><span class="sxs-lookup"><span data-stu-id="0f831-109">Security call context is passed along every time a security boundary is crossed.</span></span> <span data-ttu-id="0f831-110">Pour les appels entre les composants d’une application, qui résident dans la même limite de sécurité, aucune information de contexte d’appel n’est transmise.</span><span class="sxs-lookup"><span data-stu-id="0f831-110">For calls between components within an application, which reside within the same security boundary, no call context information is passed.</span></span> <span data-ttu-id="0f831-111">Pour les appels entre des processus ou entre des applications au sein d’un processus, appelez le flux d’informations de contexte.</span><span class="sxs-lookup"><span data-stu-id="0f831-111">For calls between processes or between applications within a process, call context information flows along.</span></span>

<span data-ttu-id="0f831-112">Cette fonctionnalité est particulièrement utile si vous souhaitez effectuer un audit et une journalisation détaillés.</span><span class="sxs-lookup"><span data-stu-id="0f831-112">This facility is particularly useful if you wish to do detailed auditing and logging.</span></span> <span data-ttu-id="0f831-113">Vous pouvez récupérer et enregistrer des informations de sécurité pour chaque appelant en amont.</span><span class="sxs-lookup"><span data-stu-id="0f831-113">You can retrieve and record security information for every upstream caller.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0f831-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0f831-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f831-115">Conception efficace des rôles</span><span class="sxs-lookup"><span data-stu-id="0f831-115">Designing Roles Effectively</span></span>](designing-roles-effectively.md)
</dt> <dt>

[<span data-ttu-id="0f831-116">Limites de sécurité</span><span class="sxs-lookup"><span data-stu-id="0f831-116">Security Boundaries</span></span>](security-boundaries.md)
</dt> <dt>

[<span data-ttu-id="0f831-117">Propriété de contexte de sécurité</span><span class="sxs-lookup"><span data-stu-id="0f831-117">Security Context Property</span></span>](security-context-property.md)
</dt> <dt>

[<span data-ttu-id="0f831-118">Utilisation de rôles pour l’autorisation du client</span><span class="sxs-lookup"><span data-stu-id="0f831-118">Using Roles for Client Authorization</span></span>](using-roles-for-client-authorization.md)
</dt> </dl>

 

 



