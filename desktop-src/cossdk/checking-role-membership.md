---
description: Vérification de l’appartenance au rôle
ms.assetid: 690cab3f-4476-4fce-b842-d63a4d0d5c6f
title: Vérification de l’appartenance au rôle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 777d47b36d2eea79d8b16e7025839b696c38ff87
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126923032"
---
# <a name="checking-role-membership"></a>Vérification de l’appartenance au rôle

Vous pouvez appeler la méthode [**ISecurityCallContext :: IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) pour déterminer si l’appelant direct d’un objet est membre d’un rôle particulier. Cette fonctionnalité est utile lorsque vous souhaitez vous assurer qu’un bloc de code spécifique n’est pas exécuté, sauf si l’appelant est membre d’un rôle particulier.

Par exemple, vous pouvez utiliser [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) pour vous assurer que les transactions sur une quantité spécifiée, telles que $1000, sont exécutées uniquement par les membres d’un rôle Manager. Si l’appelant n’est pas un responsable et que la transaction est supérieure à $1000, la transaction n’est pas effectuée et un message d’erreur s’affiche.

La meilleure façon d’accéder à [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) consiste à utiliser l’objet de contexte d’appel de sécurité, car vous pouvez utiliser la même référence à l’objet de contexte d’appel de sécurité pour obtenir des propriétés de sécurité. Toutefois, vous pouvez également accéder à la méthode **IsCallerInRole** à partir de l’objet **ObjectContext** . (Pour plus d’informations, consultez [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) ou [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) .)

si vous développez des composants pour une application Microsoft Visual Basic, vous appelez la fonction [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) , puis vous utilisez le contexte de l’appel de sécurité pour appeler [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole), comme illustré dans l’exemple suivant :


```VB
If (GetSecurityCallContext.IsCallerInRole("Manager")) Then
   ' Go ahead and perform the transaction.
Else
   ' Display an error message.
End If
```



Si vous développez une application C ou C++, utilisez [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) pour récupérer un pointeur vers l’interface [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) . Ensuite, vous appelez [**ISecurityCallContext :: IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole), comme indiqué dans l’exemple suivant :


```C++
ISecurityCallContext* pSecCtx;
VARIANT_BOOL bIsInRole;

HRESULT hr = CoGetCallContext(IID_ISecurityCallContext, (void**)&pSecCtx);
if (FAILED(hr)) throw(hr);
if (NULL == pSecCtx) { 
    // No security call context is available.
    // Display an error message and return.
    return E_FAIL;
}
hr = pSecCtx->IsCallerInRole(myRole, &bIsInRole);
return hr;
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Accès aux informations de contexte de l’appel de sécurité](accessing-security-call-context-information.md)
</dt> <dt>

[Détermination de l’activation ou non de la sécurité Role-Based](determining-whether-role-based-security-is-enabled.md)
</dt> <dt>

[Sécurité des composants de programmation](programmatic-component-security.md)
</dt> </dl>

 

 
