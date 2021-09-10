---
title: Négociation de sécurité permanente
description: Négociation de sécurité permanente
ms.assetid: 5a01912d-611c-4a6e-ab9d-0243cba331f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e51407de908eaaf0f79eea452046f8e424ccf900
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363488"
---
# <a name="security-blanket-negotiation"></a>Négociation de sécurité permanente

Une couverture de sécurité est un groupe de valeurs qui décrivent les paramètres de sécurité qui s’appliquent à tous les proxies d’un processus ou uniquement à un proxy d’interface particulier. Une couverture de sécurité comprend les valeurs suivantes :

-   Service d’authentification
-   Service d’autorisation
-   Nom principal
-   Niveau d’authentification
-   Niveau d'emprunt d'identité
-   Identité d’authentification
-   Fonctionnalités
-   Liste de contrôle d’accès (ACL) (serveurs uniquement)

La négociation permanente de sécurité est le processus utilisé par COM pour choisir les paramètres de sécurité d’un proxy lors de sa création. Ce processus implique la comparaison de la couverture de sécurité du serveur avec la couverture de sécurité du client et l’utilisation de ces valeurs pour créer une couverture de sécurité par défaut appropriée pour le proxy. Les paragraphes suivants expliquent l’origine des préversions de sécurité du client et du serveur, et décrivent comment COM négocie la couverture de sécurité pour le proxy à l’aide des couvertures de sécurité du client et du serveur.

Le client et le serveur peuvent chacun appeler [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) pour spécifier leurs couvertures de sécurité respectives. Si une application n’appelle pas **CoInitializeSecurity** explicitement, com l’appelle implicitement pour l’application, en utilisant les valeurs par défaut appropriées. Pour plus d’informations sur ces valeurs par défaut, consultez valeurs [par défaut de la sécurité com](com-security-defaults.md).

Certains paramètres de [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) s’appliquent lorsque l’application est un serveur, et d’autres s’appliquent lorsque l’application est un client. Lorsque l’application agit en tant que serveur, ces paramètres sont pertinents : une liste de contrôle d’accès, une liste de tuples de service/d’autorisation d’authentification/nom de principal et un niveau d’authentification. L’appel d’un serveur à **CoInitializeSecurity**, implicite ou explicite, détermine la couverture de sécurité du serveur, qui reste fixe.

Lorsque l’application agit en tant que client, les valeurs suivantes transmises à [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) sont pertinentes : un niveau d’authentification, un niveau d’emprunt d’identité, l’identité d’authentification et des fonctionnalités. L’appel implicite ou explicite d’un client à **CoInitializeSecurity** indique la couverture de sécurité souhaitée par le client.

Lorsqu’un proxy est créé, COM utilise les valeurs spécifiées par la couverture de sécurité du serveur et la couverture de sécurité du client pour négocier une couverture de sécurité par défaut appropriée pour le proxy. COM choisit un service d’authentification qui fonctionne à la fois sur le client et sur le serveur. Le service d’autorisation et le nom principal sont choisis pour fonctionner avec le service d’authentification. Pour le niveau d’authentification, COM choisit le plus élevé des niveaux d’authentification spécifiés par le client et le serveur. Le niveau d’emprunt d’identité et les fonctionnalités choisies par COM sont ceux qui sont spécifiés par le client. L’identité d’authentification est celle spécifiée par le client pour le service d’authentification choisi.

Une fois que la couverture de sécurité par défaut a été calculée, ses valeurs sont assignées au proxy nouvellement créé. Le client peut remplacer les paramètres de sécurité du proxy en appelant [**IClientSecurity :: SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket). Les valeurs spécifiées à **SetBlanket** ne sont pas négociées ; ils sont simplement affectés au proxy spécifié. Toutefois, si les paramètres par défaut (tels que les paramètres \_ \_ \_ par défaut du niveau d’IMP RPC \_ ) sont passés à **SetBlanket**, com utilise l’algorithme de négociation permanente de sécurité décrit précédemment pour calculer les paramètres par défaut.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Sécurité dans COM](security-in-com.md)
</dt> </dl>

 

 