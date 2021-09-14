---
description: Détermination de l’activation ou non de la sécurité Role-Based
ms.assetid: b5e6ab7e-5a77-4c6f-9bec-02942bba389d
title: Détermination de l’activation ou non de la sécurité Role-Based
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90ccf6f95b9c8776a45c071f6d4ea3326eda035c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127291814"
---
# <a name="determining-whether-role-based-security-is-enabled"></a>Détermination de l’activation ou non de la sécurité Role-Based

À l’aide de la méthode [**ISecurityCallContext :: IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) disponible à partir de l’objet de contexte de l’appel de sécurité, vous pouvez déterminer si la sécurité est activée pour l’objet en cours. Vous devez appeler **IsSecurityEnabled** avant d’utiliser ISecurityCallContext ::[**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) pour vérifier l’appartenance à un rôle, car **IsCallerInRole** retourne la valeur true si la sécurité n’est pas activée.

les développeurs Microsoft Visual Basic appellent [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) pour obtenir une référence à un objet [**SecurityCallContext**](securitycallcontext.md) , puis appeler [**IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled), comme illustré dans l’exemple suivant :


```VB
Dim objSecCallCtx As SecurityCallContext
Dim boolSecEn As Boolean
Set objSecCallCtx = GetSecurityCallContext()
boolSecEn = objSecCallCtx.IsSecurityEnabled()
 
```



Microsoft Visual C++ développeurs peuvent appeler [**ISecurityCallContext :: IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) en appelant [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) pour obtenir un pointeur vers [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) , puis en appelant **IsSecurityEnabled**. Voici un bref exemple :


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



Bien que la meilleure façon d’appeler [**IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) est d’utiliser l’objet de contexte d’appel de sécurité, vous pouvez également appeler **IsSecurityEnabled** via le contexte de l’objet. (Pour plus d’informations, consultez [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) ou [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) .)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Accès aux informations de contexte de l’appel de sécurité](accessing-security-call-context-information.md)
</dt> <dt>

[Vérification de l’appartenance au rôle](checking-role-membership.md)
</dt> <dt>

[Sécurité des composants de programmation](programmatic-component-security.md)
</dt> </dl>

 

 
