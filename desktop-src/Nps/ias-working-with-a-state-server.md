---
title: Utilisation d’un serveur d’État
description: NPS effectue l’authentification à l’aide d’une base de données configurée sur le site du serveur NPS.
ms.assetid: 8313ba91-5ed1-44d0-80db-cfb82c641100
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d79ff46802d53109c7bb8b40fe3a2db2480949e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511081"
---
# <a name="working-with-a-state-server"></a>Utilisation d’un serveur d’État

> [!Note]  
> Le service d’authentification Internet (IAS) a été renommé serveur NPS (Network Policy Server) à partir de Windows Server 2008. Le contenu de cette rubrique s’applique à IAS et à NPS. Dans le texte, NPS est utilisé pour faire référence à toutes les versions du service, y compris les versions initialement appelées IAS.

 

NPS effectue l’authentification à l’aide d’une base de données configurée sur le site du serveur NPS. Cette base de données d’authentification peut être la base de données utilisateur d’un domaine Windows, ou elle peut créer les informations utilisateur obtenues à partir du Active Directory Windows. Le diagramme suivant illustre une configuration classique qui montre comment NPS interagit avec les bases de données d’authentification, telles qu’une base de données utilisateur de domaine Windows ou Active Directory. Le diagramme montre également comment NPS peut interagir avec un serveur d’état fourni par un tiers. L’objectif principal d’un serveur d’État est de limiter le nombre de sessions d’ouverture de session simultanées qu’un seul utilisateur peut exécuter.

![NPS qui interagit avec le serveur d’État et les bases de données d’authentification](images/ias02.png)

Il existe deux points d’interaction entre NPS et le serveur d’État. Une interaction a lieu lorsque NPS reçoit une demande d’authentification du NAS. Le serveur d’État fournit des informations à partir de sa base de données pour déterminer s’il faut accepter ou refuser la demande. L’autre interaction a lieu lorsque NPS reçoit des demandes de gestion de compte du NAS. Le serveur d’État utilise ces informations pour mettre à jour sa base de données.

Pour plus d’informations sur les serveurs d’État, consultez :

-   [Considérations relatives à la conception du serveur d’État](/windows/desktop/Nps/ias-state-server-design-considerations)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Service d’authentification Internet et serveur NPS (Network Policy Server)](internet-authentication-service-vs-network-policy-server.md)
</dt> <dt>

[Authentification, autorisation et gestion des comptes RADIUS](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[Journalisation avec le serveur NPS](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> </dl>

 

 