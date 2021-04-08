---
description: Fournit l’accès à une collection d’informations de sécurité représentant l’identité d’un appelant. À l’aide de cette classe, vous pouvez trouver des informations sur un appelant particulier dans une chaîne d’appelants qui fait partie du contexte de l’appel de sécurité.
ms.assetid: c6b28695-1b08-490a-8d56-eb55d82f3e7a
title: SecurityIdentity, classe (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SecurityIdentity
api_type:
- COM
ms.openlocfilehash: 6775c06bc25bfb32a1c2c247868fd2a9fbc9aade
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "103761557"
---
# <a name="securityidentity-class"></a>SecurityIdentity, classe

Fournit l’accès à une collection d’informations de sécurité représentant l’identité d’un appelant. À l’aide de cette classe, vous pouvez trouver des informations sur un appelant particulier dans une chaîne d’appelants qui fait partie du contexte de l’appel de sécurité. Pour plus d’informations sur la façon dont les informations de contexte de l’appel de sécurité sont accessibles, consultez sécurité des composants de programmation.

Seules les applications COM+ qui utilisent la sécurité basée sur les rôles peuvent accéder à la classe **SecurityIdentity** . Pour plus d’informations sur les rôles, consultez administration de la [sécurité basée sur les rôles](role-based-security-administration.md).

## <a name="when-to-implement"></a>Quand implémenter

Cette classe est implémentée par COM+.



| Condition requise | Valeur |
|------------|--------------------------------------------------------|
| Interfaces | [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll) |



 

## <a name="when-to-use"></a>Quand l’utiliser

Utilisez cette classe pour accéder aux méthodes de [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll).

## <a name="remarks"></a>Notes

Vous ne pouvez pas créer directement un objet **SecurityIdentity** . Pour utiliser les méthodes de [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll), vous devez obtenir une référence à son implémentation en appelant [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), en fournissant IID \_ ISecurityCallContext pour le paramètre *riid* . Ensuite, appelez [**ISecurityCallContext :: obtenir l' \_ élément**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-get_item) qui demande un élément de contexte d’appel de sécurité qui est une collection d’identités de sécurité (par exemple, « DirectCaller » ou « OriginalCaller »). Appelez ensuite [**ISecurityIdentityColl :: obtenir l' \_ élément**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecurityidentitycoll-get_item) pour récupérer un élément d’identité de sécurité (tel que « Name » ou « AuthenticationService »).

Pour utiliser cette classe à partir de Microsoft Visual Basic, ajoutez une référence à la bibliothèque de types des services COM+. Vous ne pouvez pas créer directement un objet SecurityIdentity. Pour utiliser ses propriétés, vous devez obtenir un référence à son implémentation à l’aide de [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext). Ensuite, récupérez la propriété Item de l’objet, en demandant un élément de contexte d’appel de sécurité qui est une collection d’identités de sécurité (telle que « DirectCaller » ou « OriginalCaller »). Ensuite, utilisez la propriété Item de l’objet SecurityIdentity pour récupérer un élément d’identité de sécurité (tel que « Name » ou « AuthenticationService »).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>ComSvcs. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext)
</dt> <dt>

[**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll)
</dt> <dt>

[Sécurité des composants de programmation](programmatic-component-security.md)
</dt> <dt>

[Administration de la sécurité basée sur les rôles](role-based-security-administration.md)
</dt> <dt>

[**SecurityCallContext**](securitycallcontext.md)
</dt> <dt>

[**SecurityCallers**](securitycallers.md)
</dt> </dl>

 

