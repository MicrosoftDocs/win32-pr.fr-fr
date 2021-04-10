---
description: Détermination de l’activation ou non de la sécurité Role-Based
ms.assetid: b5e6ab7e-5a77-4c6f-9bec-02942bba389d
title: Détermination de l’activation ou non de la sécurité Role-Based
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90ccf6f95b9c8776a45c071f6d4ea3326eda035c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111435"
---
# <a name="determining-whether-role-based-security-is-enabled"></a><span data-ttu-id="62626-103">Détermination de l’activation ou non de la sécurité Role-Based</span><span class="sxs-lookup"><span data-stu-id="62626-103">Determining Whether Role-Based Security Is Enabled</span></span>

<span data-ttu-id="62626-104">À l’aide de la méthode [**ISecurityCallContext :: IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) disponible à partir de l’objet de contexte de l’appel de sécurité, vous pouvez déterminer si la sécurité est activée pour l’objet en cours.</span><span class="sxs-lookup"><span data-stu-id="62626-104">By using the [**ISecurityCallContext::IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) method available from the security call context object, you can determine whether security is enabled for the current object.</span></span> <span data-ttu-id="62626-105">Vous devez appeler **IsSecurityEnabled** avant d’utiliser ISecurityCallContext ::[**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) pour vérifier l’appartenance à un rôle, car **IsCallerInRole** retourne la valeur true si la sécurité n’est pas activée.</span><span class="sxs-lookup"><span data-stu-id="62626-105">You should call **IsSecurityEnabled** before you use ISecurityCallContext::[**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) to check role membership because **IsCallerInRole** returns True if security is not enabled.</span></span>

<span data-ttu-id="62626-106">Les développeurs Microsoft Visual Basic appellent [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) pour obtenir une référence à un objet [**SecurityCallContext**](securitycallcontext.md) , puis appeler [**IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled), comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="62626-106">Microsoft Visual Basic developers call [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) to obtain a reference to a [**SecurityCallContext**](securitycallcontext.md) object and then call [**IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled), as shown in the following example:</span></span>


```VB
Dim objSecCallCtx As SecurityCallContext
Dim boolSecEn As Boolean
Set objSecCallCtx = GetSecurityCallContext()
boolSecEn = objSecCallCtx.IsSecurityEnabled()
 
```



<span data-ttu-id="62626-107">Microsoft Visual C++ développeurs peuvent appeler [**ISecurityCallContext :: IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) en appelant [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) pour obtenir un pointeur vers [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) , puis en appelant **IsSecurityEnabled**.</span><span class="sxs-lookup"><span data-stu-id="62626-107">Microsoft Visual C++ developers can call [**ISecurityCallContext::IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) by calling [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) to obtain a pointer to [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) and then calling **IsSecurityEnabled**.</span></span> <span data-ttu-id="62626-108">Voici un bref exemple :</span><span class="sxs-lookup"><span data-stu-id="62626-108">A brief example follows:</span></span>


```C++
ISecurityCallContext* pSecCtx;
VARIANT_BOOL bIsEnabled;

HRESULT hr1 = CoGetCallContext(IID_ISecurityCallContext, (void**)&pSecCtx);
if (FAILED(hr1)) throw(hr1);
if (NULL == pSecCtx) {
    // Display error message.
    return E_FAIL;
}

HRESULT hr2 = pSecCtx->IsSecurityEnabled(&bIsEnabled);
return hr2;
```



<span data-ttu-id="62626-109">Bien que la meilleure façon d’appeler [**IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) est d’utiliser l’objet de contexte d’appel de sécurité, vous pouvez également appeler **IsSecurityEnabled** via le contexte de l’objet.</span><span class="sxs-lookup"><span data-stu-id="62626-109">Although the preferred way to call [**IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) is by using the security call context object, you can also call **IsSecurityEnabled** through the object context.</span></span> <span data-ttu-id="62626-110">(Pour plus d’informations, consultez [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) ou [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) .)</span><span class="sxs-lookup"><span data-stu-id="62626-110">(See [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) or [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) for more information.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="62626-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="62626-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62626-112">Accès aux informations de contexte de l’appel de sécurité</span><span class="sxs-lookup"><span data-stu-id="62626-112">Accessing Security Call Context Information</span></span>](accessing-security-call-context-information.md)
</dt> <dt>

[<span data-ttu-id="62626-113">Vérification de l’appartenance au rôle</span><span class="sxs-lookup"><span data-stu-id="62626-113">Checking Role Membership</span></span>](checking-role-membership.md)
</dt> <dt>

[<span data-ttu-id="62626-114">Sécurité des composants de programmation</span><span class="sxs-lookup"><span data-stu-id="62626-114">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> </dl>

 

 
