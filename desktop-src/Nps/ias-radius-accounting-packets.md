---
title: Journalisation avec le serveur NPS
description: Journalisation avec le serveur NPS
ms.assetid: 903d89bd-c223-4f29-9eaf-1dc28d27a32a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5117ce15731ea656913b47525387a48a39aa414c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315839"
---
# <a name="logging-with-network-policy-server"></a>Journalisation avec le serveur NPS

> [!Note]  
> Le service d’authentification Internet (IAS) a été renommé serveur NPS (Network Policy Server) à partir de Windows Server 2008. Le contenu de cette rubrique s’applique à IAS et à NPS. Dans le texte, NPS est utilisé pour faire référence à toutes les versions du service, y compris les versions initialement appelées IAS.

 

Le tableau suivant décrit uniquement les aspects les plus importants des paquets de gestion de comptes RADIUS. Le document demande de commentaires de gestion des comptes RADIUS ([RFC 2866](https://www.ietf.org/rfc/rfc2866.txt)) fournit des informations détaillées sur ces paquets.

Les paquets de gestion des comptes RADIUS peuvent être répartis dans les catégories suivantes.



| Paquet de comptabilité  | Description                                                                                                                                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Accounting-On      | Envoyé par le serveur d’accès réseau (NAS) pour indiquer qu’il a redémarré.<br/> Contient NAS-identifier/IPAddress.<br/>                                                                                        |
| Accounting-Off     | Envoyé par le NAS pour indiquer qu’il est en cours d’arrêt.<br/> Contient NAS-identifier/IPAddress.<br/>                                                                                                            |
| Accounting-Start   | Envoyé par le NAS, après que l’utilisateur a été authentifié et autorisé, pour indiquer le début d’une session utilisateur. <br/> Contient UserID, NAS-identifier/IPAddress, ainsi que d’autres informations reçues du NAS.<br/> |
| Accounting-Stop    | Envoyé par le NAS pour indiquer la fin d’une session utilisateur.<br/> Contient UserID, NAS-identifier/IPAddress, ainsi que d’autres informations reçues du NAS.<br/>                                                      |
| Accounting-Interim | Peut être envoyé régulièrement par le NAS pour chaque utilisateur qui est connecté au NAS. <br/> Cette fonctionnalité est généralement prise en charge dans les versions plus récentes de NAS.<br/>                                                     |



 

Les problèmes suivants sont importants à prendre en compte lors de la collecte des informations de comptabilité mises à disposition via RADIUS :

-   Dans de rares cas, les paquets peuvent être perdus pendant la transmission et peuvent ne jamais atteindre le serveur RADIUS.
-   Le serveur RADIUS n’est pas notifié si le NAS est abandonné.
-   RNIS prend en charge plusieurs sessions et chaque session génère une paire de paquets de début/fin de compte. Il existe un attribut comptabilité appelé identificateur de session multiple qui identifie clairement de tels paquets de plusieurs sessions. Vérifiez l’identificateur de session multiple en plus de l’identificateur de session pour calculer le nombre de sessions.

## <a name="requests-logged-by-nps"></a>Demandes journalisées par NPS

Par défaut, NPS n’enregistre aucune donnée. Le serveur NPS peut être configuré à l’aide de l’interface utilisateur NPS (NPS. msc) pour enregistrer les requêtes suivantes.



| Paquet journalisé          | Description                                                                                                                                  |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Demande de comptabilité     | N’importe quel paquet comptable décrit dans le tableau précédent.<br/>                                                                    |
| Demande d’authentification | Envoyé par le NAS pour le compte de l’utilisateur qui se connecte.<br/> Les entrées de journal contiennent uniquement des attributs entrants.<br/>                    |
| Acceptation de l’authentification  | Envoyé par le serveur NPS pour indiquer que la connexion utilisateur doit être acceptée.<br/> Les entrées de journal contiennent uniquement des attributs sortants.<br/> |
| Rejet de l’authentification  | Envoyé par le serveur NPS pour indiquer que la connexion utilisateur doit être rejetée.<br/> Les entrées de journal contiennent uniquement des attributs sortants.<br/> |



 

Les données consignées par NPS peuvent accéder à un fichier texte sur le serveur NPS ou à une base de données SQL centrale. Pour plus d’informations sur la journalisation SQL NPS, consultez [programmabilité SQL](sql-programmability.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Service d’authentification Internet et serveur NPS (Network Policy Server)](internet-authentication-service-vs-network-policy-server.md)
</dt> <dt>

[Authentification, autorisation et gestion des comptes RADIUS](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[Utilisation d’un serveur d’État](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

 

