---
description: Fournit l’accès au contexte de sécurité de l’appel actuel, qui contient des informations sur les appelants d’un objet.
ms.assetid: e8ac05fb-6665-4e57-b64e-82d9799d29d4
title: SecurityCallContext, classe (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SecurityCallContext
api_type:
- COM
ms.openlocfilehash: bd15b7e0317a507a2340cc148bb927bb5d94a37b
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106545220"
---
# <a name="securitycallcontext-class"></a><span data-ttu-id="c72cc-103">Classe SecurityCallContext</span><span class="sxs-lookup"><span data-stu-id="c72cc-103">SecurityCallContext class</span></span>

<span data-ttu-id="c72cc-104">Fournit l’accès au contexte de sécurité de l’appel actuel, qui contient des informations sur les appelants d’un objet.</span><span class="sxs-lookup"><span data-stu-id="c72cc-104">Provides access to the current call's security context, which contains information about an object's callers.</span></span> <span data-ttu-id="c72cc-105">À l’aide de cette classe, vous pouvez également déterminer si l’appelant direct d’un objet est membre d’un rôle particulier et si la sécurité est activée pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="c72cc-105">Using this class, you can also find out whether an object's direct caller is a member of a particular role and whether security is enabled for the object.</span></span>

<span data-ttu-id="c72cc-106">Seules les applications COM+ qui utilisent la sécurité basée sur les rôles peuvent accéder à la classe **SecurityCallContext** .</span><span class="sxs-lookup"><span data-stu-id="c72cc-106">Only COM+ applications that use role-based security can access the **SecurityCallContext** class.</span></span> <span data-ttu-id="c72cc-107">Pour plus d’informations sur les rôles, consultez administration de la [sécurité basée sur les rôles](role-based-security-administration.md).</span><span class="sxs-lookup"><span data-stu-id="c72cc-107">For more information on roles, see [Role-Based Security Administration](role-based-security-administration.md).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="c72cc-108">Quand implémenter</span><span class="sxs-lookup"><span data-stu-id="c72cc-108">When to implement</span></span>

<span data-ttu-id="c72cc-109">Cette classe est implémentée par COM+.</span><span class="sxs-lookup"><span data-stu-id="c72cc-109">This class is implemented by COM+.</span></span>



| <span data-ttu-id="c72cc-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c72cc-110">Requirement</span></span> | <span data-ttu-id="c72cc-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="c72cc-111">Value</span></span> |
|------------|------------------------------------------------------|
| <span data-ttu-id="c72cc-112">Interfaces</span><span class="sxs-lookup"><span data-stu-id="c72cc-112">Interfaces</span></span> | [<span data-ttu-id="c72cc-113">**ISecurityCallersColl**</span><span class="sxs-lookup"><span data-stu-id="c72cc-113">**ISecurityCallersColl**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll) |



 

## <a name="when-to-use"></a><span data-ttu-id="c72cc-114">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="c72cc-114">When to use</span></span>

<span data-ttu-id="c72cc-115">Utilisez cette classe pour accéder aux méthodes de [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext).</span><span class="sxs-lookup"><span data-stu-id="c72cc-115">Use this class to access the methods of [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext).</span></span>

## <a name="remarks"></a><span data-ttu-id="c72cc-116">Notes</span><span class="sxs-lookup"><span data-stu-id="c72cc-116">Remarks</span></span>

<span data-ttu-id="c72cc-117">Vous ne pouvez pas créer directement un objet **SecurityCallContext** .</span><span class="sxs-lookup"><span data-stu-id="c72cc-117">You cannot directly create a **SecurityCallContext** object.</span></span> <span data-ttu-id="c72cc-118">Pour utiliser les méthodes de [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext), vous devez obtenir une référence à son implémentation en appelant [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), en fournissant IID \_ ISecurityCallContext pour le paramètre *riid* .</span><span class="sxs-lookup"><span data-stu-id="c72cc-118">To use the methods of [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext), you must obtain a reference to its implementation by calling [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), supplying IID\_ISecurityCallContext for the *riid* parameter.</span></span>

<span data-ttu-id="c72cc-119">Pour utiliser cette classe à partir de Microsoft Visual Basic, ajoutez une référence à la bibliothèque de types des services COM+.</span><span class="sxs-lookup"><span data-stu-id="c72cc-119">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="c72cc-120">Un objet SecurityCallContext peut être déclaré à l’aide de « COMSVCSLib. SecurityCallContext » comme nom de classe ; elle est créée en appelant [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext).</span><span class="sxs-lookup"><span data-stu-id="c72cc-120">A SecurityCallContext object can be declared using "COMSVCSLib.SecurityCallContext" as the class name; it is created by calling [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext).</span></span>

## <a name="requirements"></a><span data-ttu-id="c72cc-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c72cc-121">Requirements</span></span>



| <span data-ttu-id="c72cc-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c72cc-122">Requirement</span></span> | <span data-ttu-id="c72cc-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="c72cc-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c72cc-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c72cc-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c72cc-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c72cc-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="c72cc-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c72cc-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c72cc-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c72cc-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c72cc-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="c72cc-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c72cc-129"><dt>ComSvcs. h</dt></span><span class="sxs-lookup"><span data-stu-id="c72cc-129"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c72cc-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c72cc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c72cc-131">**GetSecurityCallContext**</span><span class="sxs-lookup"><span data-stu-id="c72cc-131">**GetSecurityCallContext**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext)
</dt> <dt>

[<span data-ttu-id="c72cc-132">**ISecurityCallContext**</span><span class="sxs-lookup"><span data-stu-id="c72cc-132">**ISecurityCallContext**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext)
</dt> <dt>

[<span data-ttu-id="c72cc-133">Sécurité des composants de programmation</span><span class="sxs-lookup"><span data-stu-id="c72cc-133">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="c72cc-134">Administration de la sécurité basée sur les rôles</span><span class="sxs-lookup"><span data-stu-id="c72cc-134">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> <dt>

[<span data-ttu-id="c72cc-135">**SecurityCallers**</span><span class="sxs-lookup"><span data-stu-id="c72cc-135">**SecurityCallers**</span></span>](securitycallers.md)
</dt> <dt>

[<span data-ttu-id="c72cc-136">**SecurityIdentity**</span><span class="sxs-lookup"><span data-stu-id="c72cc-136">**SecurityIdentity**</span></span>](securityidentity.md)
</dt> </dl>

 

