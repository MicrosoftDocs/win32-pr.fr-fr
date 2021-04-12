---
description: Lorsque la sécurité basée sur les rôles est utilisée, l’objet de contexte de l’appel de sécurité peut être utilisé pour accéder aux informations de sécurité relatives à l’appel en cours.
ms.assetid: 9fc0a9e5-934c-4510-8fbb-1fb2817aa0ea
title: Accès aux informations de contexte de l’appel de sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6d7e5160c766783b6d43822571d624e0a595c9e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201060"
---
# <a name="accessing-security-call-context-information"></a>Accès aux informations de contexte de l’appel de sécurité

Lorsque la sécurité basée sur les rôles est utilisée, l’objet de contexte de l’appel de sécurité peut être utilisé pour accéder aux informations de sécurité relatives à l’appel en cours.

Les collections de propriétés suivantes sont disponibles à partir de l’objet de contexte de l’appel de sécurité :

-   [Collection SecurityCallContext](#securitycallcontext-collection)
-   [SecurityCallers, collection](#securitycallers-collection)
-   [SecurityIdentity, collection](#securityidentity-collection)
-   [Rubriques connexes](#related-topics)

## <a name="securitycallcontext-collection"></a>Collection SecurityCallContext



| Propriété                          | Description                                                                                                                            |
|-----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| NumCallers<br/>             | Nombre d’appelants dans la chaîne d’appels.<br/>                                                                                |
| MinAuthenticationLevel<br/> | Niveau d’authentification le moins sécurisé de tous les appelants de la chaîne.<br/>                                                          |
| Appelants<br/>                | Informations sur l’identité des appelants en amont, sous la forme d’une collection [**SecurityCallers**](securitycallers.md) .<br/> |
| DirectCaller<br/>           | Appelant qui a appelé l’objet directement (sans appelants impliqués). <br/>                                                  |
| OriginalCaller<br/>         | Appelant à l’origine de la chaîne d’appels à l’objet. <br/>                                                               |



 

Pour plus d’informations sur l’utilisation de cette collection, Microsoft Visual Basic les développeurs doivent voir la classe [**SecurityCallContext**](securitycallcontext.md) . Les développeurs C et C++ doivent faire référence à [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext).

## <a name="securitycallers-collection"></a>SecurityCallers, collection

La collection [**SecurityCallers**](securitycallers.md) représente des appelants qui peuvent être récupérés à l’aide d’un index compris entre 0 et 1 inférieur à NumCallers, inclus. Chaque appelant est représenté par un objet [**SecurityIdentity**](securityidentity.md) .

Pour plus d’informations sur cette collection, Visual Basic les développeurs doivent voir la classe [**SecurityCallers**](securitycallers.md) . Les développeurs C et C++ doivent faire référence à [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll).

## <a name="securityidentity-collection"></a>SecurityIdentity, collection



| Propriété                         | Description                                                                                                                                                          |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SID<br/>                   | Identificateur de sécurité de l’appelant.<br/>                                                                                                                   |
| AccountName<br/>           | Nom de compte de l’appelant.<br/>                                                                                                                           |
| AuthenticationService<br/> | Service d’authentification utilisé, tel que NTLMSSP, Kerberos ou SSL.<br/>                                                                                       |
| AuthenticationLevel<br/>   | Niveau d’authentification utilisé, qui représente la quantité de protection utilisée lors de la communication avec l’objet.<br/>                                         |
| ImpersonationLevel<br/>    | Niveau d’emprunt d’identité défini par le client, si l’emprunt d’identité a été utilisé. Ce niveau indique la quantité d’autorité donnée au serveur par le client. <br/> |



 

Pour plus d’informations sur cette collection, Visual Basic les développeurs doivent voir la classe [**SecurityIdentity**](securityidentity.md) . Les développeurs C et C++ doivent faire référence à [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vérification de l’appartenance au rôle](checking-role-membership.md)
</dt> <dt>

[Détermination de l’activation ou non de la sécurité Role-Based](determining-whether-role-based-security-is-enabled.md)
</dt> <dt>

[Sécurité des composants de programmation](programmatic-component-security.md)
</dt> </dl>

 

 




