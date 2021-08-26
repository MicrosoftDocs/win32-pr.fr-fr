---
description: 'Il existe deux types distincts d’applications réseau de socket : serveur et client.'
ms.assetid: 05e42384-1746-462d-82c7-8df848b4525e
title: À propos des serveurs et des clients
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07e6d8016d1fc9c23b901a03a924cd0e3ade3982dc2e1bf0db277eac47170d89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898639"
---
# <a name="about-servers-and-clients"></a>À propos des serveurs et des clients

Il existe deux types distincts d’applications réseau de socket : serveur et client.

Les serveurs et les clients ont des comportements différents ; par conséquent, le processus de création de ces éléments est différent. Ce qui suit est le modèle général pour la création d’un serveur et d’un client TCP/IP de streaming.

## <a name="server"></a>Serveur

1.  Initialisez Winsock.
2.  Créer un Socket.
3.  Liez le Socket.
4.  Écoute sur le socket pour un client.
5.  Accepter une connexion à partir d’un client.
6.  Recevoir et envoyer des données.
7.  Se déconnecter.

## <a name="client"></a>Client

1.  Initialisez Winsock.
2.  Créer un Socket.
3.  Connecter au serveur.
4.  Envoyer et recevoir des données.
5.  Se déconnecter.

> [!Note]  
> Certaines étapes sont identiques pour un client et un serveur. Ces étapes sont implémentées presque exactement de la même façon. Certaines étapes de ce guide sont spécifiques au type d’application en cours de création.

 

Première étape : [création d’une application Winsock de base](creating-a-basic-winsock-application.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en main avec Winsock](getting-started-with-winsock.md)
</dt> </dl>

 

 



