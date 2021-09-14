---
description: Comment les certificats numériques fournissent des communications sécurisées et comment utiliser CryptoAPI pour utiliser et gérer ces certificats.
ms.assetid: e523b335-0156-4f47-b55c-b80495587c4f
title: Certificats numériques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 161d200a0f8cab61594872f5182786a3e6597187
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127233375"
---
# <a name="digital-certificates"></a>Certificats numériques

L’authentification est essentielle pour sécuriser les communications. Les utilisateurs doivent être en mesure de prouver leur identité à ceux avec lesquels ils communiquent et doivent être en mesure de vérifier l’identité des autres utilisateurs. L’authentification de l’identité sur un réseau est une opération complexe, car les parties qui communiquent ne se rencontrent pas physiquement lors de la communication. Un utilisateur malveillant peut ainsi intercepter des messages ou emprunter l’identité d’une autre personne ou entité. Une méthode doit être utilisée pour maintenir le niveau de confiance nécessaire dans le processus de communication.

Le [*certificat numérique*](../secgloss/c-gly.md) est une information d’identification courante qui fournit un moyen de vérifier l’identité. Cette section fournit une vue d’ensemble de la façon dont les certificats fournissent des communications sécurisées et comment utiliser CryptoAPI pour utiliser et gérer ces certificats.

Un certificat est un ensemble de données qui identifie une entité. Une organisation approuvée affecte un certificat à une personne ou à une entité qui associe une clé publique à la personne. L’individu ou l’entité à qui un certificat est émis est appelé objet de ce certificat. L’organisation approuvée qui émet le certificat est une [*autorité de certification*](../secgloss/c-gly.md) (ca) et porte le nom d’émetteur du certificat. Une autorité de certification digne de confiance n’émet un certificat qu’après avoir vérifié l’identité de l’objet du certificat.

Les certificats utilisent des techniques de chiffrement pour résoudre le problème de l’absence de contact physique entre ceux qui communiquent. L’utilisation de ces techniques limite la possibilité pour une personne non éthique d’intercepter, de modifier ou de contrefaire des messages. Ces techniques de chiffrement rendent les certificats difficiles à modifier. Par conséquent, il est difficile pour une entité d’emprunter l’identité d’une autre personne.

Les données d’un certificat incluent la clé de chiffrement publique de la [*paire de clés publique/privée*](../secgloss/p-gly.md)du sujet du certificat. Un message signé avec la clé privée de son expéditeur peut uniquement être récupéré par le destinataire du message à l’aide de la clé publique de l’expéditeur. Cette clé se trouve sur une copie du certificat de l’expéditeur. La récupération d’une signature avec une [*clé publique*](../secgloss/p-gly.md) à partir d’un certificat prouve que la signature a été générée à l’aide de la [*clé privée*](../secgloss/p-gly.md)du sujet du certificat. Si l’expéditeur a fait ses vigilance et a conservé le secret de la clé privée, le destinataire peut être sûr de l’identité de l’expéditeur du message.

Sur un réseau, il existe souvent une application approuvée appelée serveur de [*certificats*](../secgloss/c-gly.md). Une autorité de certification s’exécutant sur un ordinateur sécurisé gère le serveur de certificats. Cette application a accès à la clé publique de tous ses clients. Les serveurs de certificats distribuent des messages appelés certificats, chacun contenant la clé publique de l’un de ses utilisateurs client. Chaque certificat est signé avec la clé privée de l’autorité de certification. Le récepteur d’un tel certificat peut donc vérifier qu’une autorité de certification spécifiée l’a envoyé.

Les certificats numériques incluent également des extensions et des propriétés étendues qui fournissent des informations supplémentaires sur l’objet du certificat, telles que l’adresse de messagerie du sujet et les activités que le sujet du certificat peut effectuer.

 

 
