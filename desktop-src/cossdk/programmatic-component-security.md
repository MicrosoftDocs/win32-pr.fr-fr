---
description: Lorsque vous utilisez la sécurité basée sur les rôles dans l’application COM+ qui contient votre composant, vous avez accès aux fonctionnalités de sécurité par programmation à partir de votre composant.
ms.assetid: 6117970c-5dbd-485e-978e-3aa96e42b359
title: Sécurité des composants de programmation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31622608e4d4f54aeb53b403b5d8711ff9c6a9af
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515937"
---
# <a name="programmatic-component-security"></a><span data-ttu-id="e5314-103">Sécurité des composants de programmation</span><span class="sxs-lookup"><span data-stu-id="e5314-103">Programmatic Component Security</span></span>

<span data-ttu-id="e5314-104">Lorsque vous utilisez la sécurité basée sur les rôles dans l’application COM+ qui contient votre composant, vous avez accès aux fonctionnalités de sécurité par programmation à partir de votre composant.</span><span class="sxs-lookup"><span data-stu-id="e5314-104">When you use role-based security in the COM+ application that contains your component, you have access to programmatic security functionality from within your component.</span></span> <span data-ttu-id="e5314-105">Vous pouvez vérifier l’appartenance à un rôle pour déterminer si certaines sections de code sont exécutées, vous pouvez accéder à des informations de sécurité à l’aide de l’objet de contexte d’appel de sécurité et vous pouvez déterminer si la sécurité est activée pour l’appel en cours.</span><span class="sxs-lookup"><span data-stu-id="e5314-105">You can check role membership to determine whether particular sections of code are executed, you can access security information using the security call context object, and you can determine whether security is enabled for the current call.</span></span> <span data-ttu-id="e5314-106">Vous pouvez effectuer toutes ces tâches à l’aide d’une référence à un objet [**SecurityCallContext**](securitycallcontext.md) (pour les applications Microsoft Visual Basic) ou d’un pointeur vers l’interface [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) (pour les applications C et Microsoft Visual C++).</span><span class="sxs-lookup"><span data-stu-id="e5314-106">You can perform all of these tasks by using a reference to a [**SecurityCallContext**](securitycallcontext.md) object (for Microsoft Visual Basic applications) or a pointer to the [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) interface (for C and Microsoft Visual C++ applications).</span></span>

<span data-ttu-id="e5314-107">Pour plus d’informations sur la sécurité basée sur les rôles par programmation, consultez les rubriques suivantes dans cette section :</span><span class="sxs-lookup"><span data-stu-id="e5314-107">For more information regarding programmatic role-based security, see the following topics in this section:</span></span>

-   [<span data-ttu-id="e5314-108">Vérification de l’appartenance au rôle</span><span class="sxs-lookup"><span data-stu-id="e5314-108">Checking Role Membership</span></span>](checking-role-membership.md)
-   [<span data-ttu-id="e5314-109">Détermination de l’activation ou non de la sécurité Role-Based</span><span class="sxs-lookup"><span data-stu-id="e5314-109">Determining Whether Role-Based Security Is Enabled</span></span>](determining-whether-role-based-security-is-enabled.md)
-   [<span data-ttu-id="e5314-110">Accès aux informations de contexte de l’appel de sécurité</span><span class="sxs-lookup"><span data-stu-id="e5314-110">Accessing Security Call Context Information</span></span>](accessing-security-call-context-information.md)

## <a name="impersonation-and-com-security-features"></a><span data-ttu-id="e5314-111">Emprunt d’identité et fonctionnalités de sécurité COM</span><span class="sxs-lookup"><span data-stu-id="e5314-111">Impersonation and COM Security Features</span></span>

<span data-ttu-id="e5314-112">Si votre composant est utilisé dans une application COM+ qui n’utilise pas la sécurité basée sur les rôles, la vérification des rôles par programme et les informations de contexte d’appel de sécurité ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="e5314-112">If your component is used in a COM+ application that does not use role-based security, programmatic role checking and security call context information are not available.</span></span> <span data-ttu-id="e5314-113">Toutefois, vous pouvez utiliser la fonctionnalité de sécurité par programme fournie par COM.</span><span class="sxs-lookup"><span data-stu-id="e5314-113">However, you can use the programmatic security functionality provided by COM.</span></span> <span data-ttu-id="e5314-114">Pour plus d’informations, consultez [sécurité dans com](/windows/desktop/com/security-in-com).</span><span class="sxs-lookup"><span data-stu-id="e5314-114">For more information, see [Security in COM](/windows/desktop/com/security-in-com).</span></span>

<span data-ttu-id="e5314-115">Bien que vous puissiez utiliser la plupart des fonctionnalités de sécurité fournies par COM, vous ne pouvez pas appeler [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) à partir d’un composant qui fait partie d’une application com+, car **CoInitializeSecurity** est appelé par le substitut dans lequel l’application com+ s’exécute.</span><span class="sxs-lookup"><span data-stu-id="e5314-115">Although you can use most of the security functionality provided by COM, you cannot call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) from a component that is part of a COM+ application because **CoInitializeSecurity** is called by the surrogate that the COM+ application runs in.</span></span> <span data-ttu-id="e5314-116">Toutefois, vous pouvez appeler d’autres fonctions de sécurité, telles que [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket), qui récupère des informations sur le client.</span><span class="sxs-lookup"><span data-stu-id="e5314-116">However, you can call other security functions, such as [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket), which retrieves information about the client.</span></span>

<span data-ttu-id="e5314-117">En particulier, lorsque vous devez utiliser l’identité du client pour accéder à certaines ressources (par exemple, accéder à un fichier protégé par un descripteur de sécurité ou propager l’identité du client via vers une base de données), vous pouvez effectuer l’emprunt d’identité par programmation.</span><span class="sxs-lookup"><span data-stu-id="e5314-117">In particular, when you need to use the client's identity to access some resource—for example, accessing a file protected by a security descriptor, or propagating the client's identity through to a database—you can perform impersonation programmatically.</span></span> <span data-ttu-id="e5314-118">Pour plus d’informations sur le moment et la façon de procéder, consultez [emprunt d’identité du client et délégation](client-impersonation-and-delegation.md).</span><span class="sxs-lookup"><span data-stu-id="e5314-118">For more detail about when and how to do this, see [Client Impersonation and Delegation](client-impersonation-and-delegation.md).</span></span>

## <a name="testing-security-functionality"></a><span data-ttu-id="e5314-119">Test de la fonctionnalité de sécurité</span><span class="sxs-lookup"><span data-stu-id="e5314-119">Testing Security Functionality</span></span>

<span data-ttu-id="e5314-120">Si vous utilisez la sécurité par programmation COM+ dans votre composant, vous devez intégrer le composant dans une application COM+ lorsque vous êtes prêt à tester les fonctionnalités de sécurité du composant.</span><span class="sxs-lookup"><span data-stu-id="e5314-120">If you use COM+ programmatic security in your component, you must integrate the component into a COM+ application when you are ready to test the component's security functionality.</span></span> <span data-ttu-id="e5314-121">Si un composant qui utilise la sécurité COM+ est exécuté sans être intégré à une application COM+, les exceptions sont levées.</span><span class="sxs-lookup"><span data-stu-id="e5314-121">If a component using COM+ programmatic security is run without being integrated into a COM+ application, exceptions will be thrown.</span></span> <span data-ttu-id="e5314-122">Par conséquent, si vous souhaitez vous assurer qu’un tel composant peut également être intégré à une application qui ne fait pas partie de l’environnement COM+, vous devez vous assurer que ces exceptions sont gérées correctement.</span><span class="sxs-lookup"><span data-stu-id="e5314-122">Therefore, if you want to ensure that such a component is also capable of being successfully integrated into an application that is not part of the COM+ environment, you must ensure that these exceptions are handled appropriately.</span></span>

## <a name="documenting-security-requirements"></a><span data-ttu-id="e5314-123">Documentation des exigences de sécurité</span><span class="sxs-lookup"><span data-stu-id="e5314-123">Documenting Security Requirements</span></span>

<span data-ttu-id="e5314-124">Si vous écrivez un composant autonome pour les applications COM+ qui utilisent la sécurité basée sur les rôles, vous devez documenter le composant afin que la sécurité puisse être configurée de manière appropriée lorsque le composant est intégré à une application COM+.</span><span class="sxs-lookup"><span data-stu-id="e5314-124">If you are writing a stand-alone component for COM+ applications that use role-based security, you need to document the component so that security can be configured appropriately when the component is integrated into a COM+ application.</span></span> <span data-ttu-id="e5314-125">Par exemple, vous devez identifier les rôles qui doivent être ajoutés et expliquer à quelles méthodes et interfaces chaque rôle doit être assigné.</span><span class="sxs-lookup"><span data-stu-id="e5314-125">For example, you should identify the roles that must be added and explain which methods and interfaces each role should be assigned to.</span></span> <span data-ttu-id="e5314-126">En outre, si une méthode telle que IsCallerInRole (« Teller ») est appelée, vous devez décrire les fonctionnalités auxquelles seuls les demandeurs ont accès.</span><span class="sxs-lookup"><span data-stu-id="e5314-126">In addition, if a method such as IsCallerInRole("Teller") is called, you should describe the functionality that only Tellers have access to.</span></span> <span data-ttu-id="e5314-127">Vous devez également spécifier si un rôle est requis pour aider à protéger l’accès à l’ensemble du composant.</span><span class="sxs-lookup"><span data-stu-id="e5314-127">You should also specify whether a role is required to help protect access to the entire component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5314-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e5314-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5314-129">Authentification du client</span><span class="sxs-lookup"><span data-stu-id="e5314-129">Client Authentication</span></span>](client-authentication.md)
</dt> <dt>

[<span data-ttu-id="e5314-130">Emprunt d’identité et délégation du client</span><span class="sxs-lookup"><span data-stu-id="e5314-130">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="e5314-131">Sécurité de l’application de bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e5314-131">Library Application Security</span></span>](library-application-security.md)
</dt> <dt>

[<span data-ttu-id="e5314-132">Sécurité des applications multiniveau</span><span class="sxs-lookup"><span data-stu-id="e5314-132">Multi-Tier Application Security</span></span>](multi-tier-application-security.md)
</dt> <dt>

[<span data-ttu-id="e5314-133">Administration de la sécurité basée sur les rôles</span><span class="sxs-lookup"><span data-stu-id="e5314-133">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> <dt>

[<span data-ttu-id="e5314-134">Utilisation de la stratégie de restriction logicielle dans COM+</span><span class="sxs-lookup"><span data-stu-id="e5314-134">Using the Software Restriction Policy in COM+</span></span>](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
