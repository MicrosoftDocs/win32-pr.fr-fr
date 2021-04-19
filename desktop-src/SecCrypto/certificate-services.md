---
description: Les services de certificats, un service s’exécutant sur un système d’exploitation Windows Server, reçoivent des demandes de nouveaux certificats numériques sur des transports tels que RPC ou HTTP.
ms.assetid: 4c0098be-6b1b-4ce0-b3a0-942c1290b5b4
title: Services de certificats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1a3f25972f98a79a208719eb2bcb08de07d7894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521307"
---
# <a name="certificate-services"></a>Services de certificats

Les [*services de certificats*](../secgloss/c-gly.md), un service s’exécutant sur un système d’exploitation Windows Server, reçoivent des demandes de nouveaux certificats numériques sur des transports tels que RPC ou http. Il vérifie chaque demande par rapport à des stratégies personnalisées ou spécifiques à un site, définit des propriétés facultatives pour un certificat à émettre et émet le certificat. Les services de certificats permettent aux administrateurs d’ajouter des éléments à une [*liste de révocation de certificats*](../secgloss/c-gly.md) (CRL) et de publier des listes de révocation de certificats signées régulièrement.

Les services de certificats incluent des interfaces programmables pour la création d’une prise en charge pour les transports, les stratégies et les propriétés et formats de certificat supplémentaires.

Dans Windows Server 2003, les services de certificats 2,0 peuvent être installés à partir du **panneau de configuration** en cliquant sur Ajout/ **Suppression de programmes** , puis en cliquant sur **Ajouter/supprimer des composants Windows** pour installer ou désinstaller des services de certificats.

Les concepts des services de certificats sont détaillés dans les sections suivantes. Le contenu est destiné à vous aider à développer des applications qui interagissent avec les services de certificats.



| Content                                                                                                                                                           | Section                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| Description des fonctionnalités des services de certificats                                                                                                               | [Fonctionnalités des services de certificats](certificate-services-features.md)         |
| Vue d’ensemble de l’architecture des services de certificats                                                                                                                     | [Architecture des services de certificats](certificate-services-architecture.md) |
| Relation entre un certificat, le sujet du certificat et la [ *clé publique* du sujet](../secgloss/p-gly.md) | [Certificats et clés publiques](certificates-and-public-keys.md)           |
| Informations sur les propriétés de la demande de certificat                                                                                                              | [Instructions relatives aux demandes de certificat](certificate-request-guidelines.md)       |
| Détails sur la façon dont un certificat est traité par les services de certificats                                                                                                 | [À propos des certificats](about-certificates.md)                               |
| Description du processus de renouvellement de l' [*autorité de certification*](../secgloss/c-gly.md)        | [Renouvellement de l’autorité de certification](certification-authority-renewal.md)     |



 

Les rubriques utiles supplémentaires suivantes sont également incluses.



| Content                                                                                                                                             | Section                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| Documentation sur le contrôle d’inscription de certificats, qui fournit des services pour créer des demandes de certificat, y compris des demandes pour les utilisateurs de carte à puce. | [Contrôle d’inscription de certificat](certificate-enrollment-control.md) |
| Documentation sur l’interface de programmation d’applications de chiffrement Microsoft, qui fournit des services de sécurité basés sur la cryptographie.                | [Principes fondamentaux du chiffrement](cryptography-essentials.md)               |
| Documentation sur la carte à puce, qui fournit des services pour le développement et l’utilisation des systèmes de carte à puce.                                                   | [Carte à puce](../secauthn/smart-card-authentication.md)                     |
| Propriétés de nom des certificats et des demandes de certificat.                                                                                           | [Propriétés du nom](name-properties.md)                               |
| Liste et descriptions des propriétés du certificat [*X. 509*](../secgloss/x-gly.md) .                                  | [Propriétés du certificat](certificate-properties.md)                 |



 

 

 
