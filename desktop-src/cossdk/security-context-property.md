---
description: Propriété de contexte de sécurité
ms.assetid: 7ffae145-be13-4a2c-beb1-eaa1d11ad9a7
title: Propriété de contexte de sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b061ef7c0d0d0c146b626c11fd550c48ab488a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201117"
---
# <a name="security-context-property"></a><span data-ttu-id="98baa-103">Propriété de contexte de sécurité</span><span class="sxs-lookup"><span data-stu-id="98baa-103">Security Context Property</span></span>

<span data-ttu-id="98baa-104">Comme pour chaque service automatique fourni par COM+, la vérification automatique des rôles est basée sur les propriétés incluses dans le contexte de l’objet.</span><span class="sxs-lookup"><span data-stu-id="98baa-104">As with every automatic service provided by COM+, automatic role checking is based on properties included on the object context.</span></span> <span data-ttu-id="98baa-105">La détermination du fait qu’une vérification de la sécurité doit être effectuée sur un appel dans un composant est basée sur la propriété de sécurité du contexte de l’objet créé lorsque le composant configuré est instancié.</span><span class="sxs-lookup"><span data-stu-id="98baa-105">The determination of whether a security check must be carried out on a call into a component is based on the security property on the object context created when the configured component is instantiated.</span></span>

<span data-ttu-id="98baa-106">En général, vous n’avez pas besoin de vous préoccuper de cette propriété. elle est utilisée directement par COM+, et pas par vous.</span><span class="sxs-lookup"><span data-stu-id="98baa-106">You generally don't need to be concerned with this property; it is used directly by COM+, not you.</span></span> <span data-ttu-id="98baa-107">Toutefois, dans certains cas, vous pouvez avoir besoin d’un contrôle strict sur l’activation d’un objet.</span><span class="sxs-lookup"><span data-stu-id="98baa-107">However, in some circumstances, you might want strict control over the activation of an object.</span></span> <span data-ttu-id="98baa-108">Dans ce cas, la propriété de sécurité peut affecter le contexte dans lequel votre objet est activé.</span><span class="sxs-lookup"><span data-stu-id="98baa-108">In this case, the security property can affect which context your object is activated in.</span></span> <span data-ttu-id="98baa-109">Autrement dit, si un objet a une configuration incompatible avec le contexte de son créateur, il est activé dans son propre contexte.</span><span class="sxs-lookup"><span data-stu-id="98baa-109">That is, if an object has a configuration incompatible with the context of its creator, it will be activated in its own context.</span></span> <span data-ttu-id="98baa-110">La propriété de sécurité peut influencer cela, comme peut n’importe quelle propriété du contexte de l’objet.</span><span class="sxs-lookup"><span data-stu-id="98baa-110">The security property can influence this, as can any property on the object context.</span></span>

<span data-ttu-id="98baa-111">Si vous ne souhaitez pas que les paramètres de sécurité influencent l’activation, vous pouvez choisir uniquement la vérification de l’accès au niveau du processus.</span><span class="sxs-lookup"><span data-stu-id="98baa-111">If you don't want security settings to influence activation, you can choose process-level access checking only.</span></span> <span data-ttu-id="98baa-112">Cela supprime la propriété de sécurité sur le contexte de l’objet, même si elle désactive efficacement la vérification basée sur les rôles et rend les [informations de contexte d’appel de sécurité](security-call-context-information.md) indisponibles.</span><span class="sxs-lookup"><span data-stu-id="98baa-112">This suppresses the security property on the object context, although it effectively disables role-based checking and makes [security call context information](security-call-context-information.md) unavailable.</span></span>

<span data-ttu-id="98baa-113">Pour plus d’informations sur les contrôles d’accès au niveau du processus, consultez [limites de sécurité](security-boundaries.md).</span><span class="sxs-lookup"><span data-stu-id="98baa-113">For more information about process-level access checks, see [Security Boundaries](security-boundaries.md).</span></span> <span data-ttu-id="98baa-114">Pour savoir comment définir la sécurité au niveau du processus, consultez [définition d’un niveau de sécurité pour les vérifications d’accès](setting-a-security-level-for-access-checks.md).</span><span class="sxs-lookup"><span data-stu-id="98baa-114">To see how to set process-level security, see [Setting a Security Level for Access Checks](setting-a-security-level-for-access-checks.md).</span></span>

<span data-ttu-id="98baa-115">Pour plus d’informations sur le contexte d’objet, consultez [contextes](com--contexts.md).</span><span class="sxs-lookup"><span data-stu-id="98baa-115">For more information about object context, see [Contexts](com--contexts.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="98baa-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="98baa-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98baa-117">Conception efficace des rôles</span><span class="sxs-lookup"><span data-stu-id="98baa-117">Designing Roles Effectively</span></span>](designing-roles-effectively.md)
</dt> <dt>

[<span data-ttu-id="98baa-118">Limites de sécurité</span><span class="sxs-lookup"><span data-stu-id="98baa-118">Security Boundaries</span></span>](security-boundaries.md)
</dt> <dt>

[<span data-ttu-id="98baa-119">Informations de contexte de l’appel de sécurité</span><span class="sxs-lookup"><span data-stu-id="98baa-119">Security Call Context Information</span></span>](security-call-context-information.md)
</dt> <dt>

[<span data-ttu-id="98baa-120">Utilisation de rôles pour l’autorisation du client</span><span class="sxs-lookup"><span data-stu-id="98baa-120">Using Roles for Client Authorization</span></span>](using-roles-for-client-authorization.md)
</dt> </dl>

 

 



