---
description: Fournit l’accès aux informations sur les appelants individuels dans une collection d’appelants. La collection représente la chaîne d’appels se terminant par l’appel en cours, et chaque appelant de la collection représente l’identité d’un appelant.
ms.assetid: 164fe12d-eeb3-402f-8aa3-e3545904d9c4
title: SecurityCallers, classe (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SecurityCallers
api_type:
- COM
ms.openlocfilehash: a494e1421e443d2a6c3663bd7fa7c15eda898079477592e8df9958a2d5b87990
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117915893"
---
# <a name="securitycallers-class"></a>SecurityCallers (classe)

Fournit l’accès aux informations sur les appelants individuels dans une collection d’appelants. La collection représente la chaîne d’appels se terminant par l’appel en cours, et chaque appelant de la collection représente l’identité d’un appelant. Seuls les appelants qui franchissent une limite où la sécurité est vérifiée sont inclus dans la chaîne d’appelants. (Dans l’environnement COM+, la sécurité est vérifiée au niveau des limites de l’application.) L’accès aux informations sur l’identité d’un appelant particulier est fourni par le biais de la classe [**SecurityIdentity**](securityidentity.md) , une collection d’identités.

Seules les applications COM+ qui utilisent la sécurité basée sur les rôles peuvent accéder à la classe **SecurityCallers** . Pour plus d’informations sur les rôles, consultez administration de la [sécurité basée sur les rôles](role-based-security-administration.md).

## <a name="when-to-implement"></a>Quand implémenter

Cette classe est implémentée par COM+.



| Condition requise | Valeur |
|------------|------------------------------------------------------|
| Interfaces | [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll) |



 

## <a name="when-to-use"></a>Quand l’utiliser

Utilisez cette classe pour accéder aux méthodes de [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll).

## <a name="remarks"></a>Remarques

Vous ne pouvez pas créer directement un objet **SecurityCallers** . Pour utiliser les méthodes de [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll), vous devez obtenir une référence à son implémentation en appelant [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), en fournissant IID \_ ISecurityCallContext pour le paramètre *riid* . Ensuite, appelez [**ISecurityCallContext :: obtenir l' \_ élément**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-get_item) qui demande un élément de contexte d’appel de sécurité qui est une collection d’identités de sécurité (par exemple, « DirectCaller » ou « OriginalCaller »).

pour utiliser cette classe à partir de Microsoft Visual Basic, ajoutez une référence à la bibliothèque de types des Services COM+. Vous ne pouvez pas créer directement un objet SecurityCallers. Pour utiliser ses propriétés, vous devez obtenir un référence à son implémentation à l’aide de [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext). Ensuite, récupérez la propriété Item de l’objet, en demandant un élément de contexte d’appel de sécurité qui est une collection d’identités de sécurité (telle que « DirectCaller » ou « OriginalCaller »).

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

[**SecurityIdentity**](securityidentity.md)
</dt> </dl>

 

