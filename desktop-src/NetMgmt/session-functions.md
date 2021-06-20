---
title: Fonctions de session (gestion de réseau)
description: Passez en revue les fonctions de session, qui sont un groupe de fonctions de gestion de réseau. Ces fonctions contrôlent les sessions réseau établies entre les stations de travail et les serveurs.
ms.assetid: ef912cd9-be5c-4202-89aa-e60f275e8938
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78479391e4dc2d2aa0ced8af16a8b6cf6f3a9b05
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406122"
---
# <a name="session-functions-network-management"></a>Fonctions de session (gestion de réseau)

Les fonctions de session de gestion de réseau contrôlent les sessions réseau établies entre les stations de travail et les serveurs. Les fonctions requièrent que le service serveur soit démarré sur le serveur.

Les fonctions de session sont répertoriées ci-dessous.



| Fonction                                      | Description                                                                                       |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**NetSessionDel**](/windows/desktop/api/lmshare/nf-lmshare-netsessiondel)         | Supprime les connexions en cours entre une station de travail et un serveur. met fin à la session réseau. |
| [**NetSessionEnum**](/windows/desktop/api/lmshare/nf-lmshare-netsessionenum)       | Retourne des informations sur toutes les sessions en cours établies pour un serveur.                          |
| [**NetSessionGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo) | Retourne des informations sur une session particulière.                                                   |



 

Une *session* est un lien entre une station de travail et un serveur. Une session est établie la première fois qu’une station de travail établit une connexion à une ressource partagée sur le serveur. Jusqu’à la fin de la session, toutes les connexions supplémentaires entre la station de travail et le serveur font partie de la même session. Pour mettre fin à une session, une application sur l’extrémité serveur d’une connexion appelle la fonction [**NetSessionDel**](/windows/desktop/api/lmshare/nf-lmshare-netsessiondel) .

Les fonctions de session de gestion de réseau gèrent les informations par utilisateur avec le paramètre *username* . Étant donné qu’il peut y avoir plusieurs utilisateurs par session, ce paramètre est nécessaire pour accéder aux informations spécifiques à l’utilisateur pour la session.

Les fonctions de session sont disponibles aux niveaux d’informations suivants :

-   [**Informations de SESSION \_ \_ 0**](/windows/desktop/api/lmshare/ns-lmshare-session_info_0)
-   [**Informations de SESSION \_ \_ 1**](/windows/desktop/api/lmshare/ns-lmshare-session_info_1)
-   [**\_Informations sur la session \_ 2**](/windows/desktop/api/lmshare/ns-lmshare-session_info_2)
-   [**Informations de SESSION \_ \_ 10**](/windows/desktop/api/lmshare/ns-lmshare-session_info_10)
-   [**Informations de SESSION \_ \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-session_info_502)

Si vous programmez pour Active Directory, vous pourrez peut-être appeler certaines méthodes d’interface de service d’Active Directory (ADSI) pour obtenir les mêmes fonctionnalités que celles que vous pouvez obtenir en appelant les fonctions de session de gestion de réseau. Pour plus d’informations, consultez [**IADsSession**](/windows/desktop/api/iads/nn-iads-iadssession) et [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).

 

 
