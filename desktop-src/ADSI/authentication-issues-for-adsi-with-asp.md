---
title: Problèmes d’authentification pour ADSI avec ASP
description: Selon la configuration de votre intranet, des problèmes d’authentification peuvent se produire lorsque le code ADSI est exécuté à partir d’une page ASP.
ms.assetid: 287e2e19-7da9-497b-bf46-595ff4755261
ms.tgt_platform: multiple
keywords:
- ADSI, pages ASP, problèmes d’authentification
- ADSI, authentification, problèmes ASP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423d1aa39006f89ca366423da9d135e00af45693
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730204"
---
# <a name="authentication-issues-for-adsi-with-asp"></a>Problèmes d’authentification pour ADSI avec ASP

Selon la configuration de votre intranet, des problèmes d’authentification peuvent se produire lorsque le code ADSI est exécuté à partir d’une page ASP.

L’authentification pour accéder au contrôleur de domaine peut être fournie à l’aide de la délégation. La délégation permet à un service d’agir en tant qu’utilisateur, afin qu’il puisse accéder à une ressource réseau à l’aide des informations d’identification de cet utilisateur. Si votre intranet suit cette configuration, vous devez configurer IIS pour qu’il utilise la délégation. Définissez le mécanisme d’authentification IIS comme anonyme ou NTLM. Si vous choisissez anonyme, votre contexte de sécurité sera mappé au compte d' \_ ordinateur IUSR. Si vous sélectionnez NTLM, le contexte de sécurité sera modifié, en fonction de l’utilisateur qui se connecte à votre site Web. Pour plus d’informations et pour obtenir des instructions sur la configuration du serveur IIS pour la délégation, consultez le [Kit de ressources Windows 2000](https://support.microsoft.com/kb/927229).

Si vous utilisez un serveur IIS qui utilise le challenge/réponse NT ou un client de navigateur qui ne prend pas en charge Kerberos, l’authentification à double saut n’est pas prise en charge. L’authentification à double saut signifie que les informations d’identification de l’utilisateur sont transmises du client du navigateur au serveur IIS, puis le serveur IIS transmet les informations d’identification au serveur principal. Dans ce cas, vous pouvez utiliser l’une des solutions suivantes pour autoriser l’accès à l’annuaire à partir de la page ASP :

-   Utilisez [**IADsOpenDSObject :: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) ou [**ADsOpenObject**](binding-with-adsopenobject-and-iadsopendsobject-opendsobject.md) pour transmettre les informations d’identification à Active Directory. La page Web authentifie l’utilisateur connecté sur le serveur IIS. Lorsque l’utilisateur a été authentifié, la page Web peut utiliser OpenDSObject ou ADsOpenObject pour transmettre un nom d’utilisateur et un mot de passe au service d’annuaire pour obtenir l’authentification auprès du serveur principal. La page Web peut ensuite accéder aux données à partir de l’annuaire.
-   Ajoutez votre code à un objet COM et placez cet objet dans une [application com+](../cossdk/com--application-overview.md) (précédemment appelée package MTS). L’application COM+ peut ensuite être exécutée en tant que [compte d’utilisateur de domaine](/windows/desktop/AD/domain-user-accounts).
-   Utilisez plusieurs pages ASP, où une page authentifie le client et une autre page transmet les informations d’identification au répertoire à l’aide de l’authentification anonyme sur un compte d’utilisateur de domaine.

Ces méthodes impliquent l’authentification du client Web, puis la modification des informations d’identification lors du contact avec le répertoire, car l’authentification à double saut, avec les mêmes informations d’identification, n’est pas possible.

 

 