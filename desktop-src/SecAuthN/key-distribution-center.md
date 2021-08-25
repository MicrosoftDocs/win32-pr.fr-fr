---
description: Le centre de distribution de clés (KDC) est implémenté en tant que service de domaine. Elle utilise le Active Directory en tant que base de données de compte et le catalogue global pour diriger les références vers les KDC dans d’autres domaines.
ms.assetid: f2a7c87c-9be7-4fd8-8ecd-4edf1f2336ef
title: centre de distribution de clés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eef410ccb9289d30507708dc35000e1c15d5d4c9998b28b33a2e51d1a15b1e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013339"
---
# <a name="key-distribution-center"></a>centre de distribution de clés

Le centre de distribution de clés (KDC) est implémenté en tant que service de domaine. Elle utilise le Active Directory en tant que base de données de compte et le catalogue global pour diriger les références vers les KDC dans d’autres domaines.

Comme dans d’autres implémentations du [*protocole Kerberos*](../secgloss/k-gly.md), le KDC est un processus unique qui fournit deux services :

-   Service d’authentification (AS)

    Ce service émet des tickets TGT (Ticket-Granting tickets) pour la connexion au service d’accord de tickets dans son propre domaine ou dans un domaine approuvé. Avant qu’un client puisse demander un ticket à un autre ordinateur, il doit demander un ticket TGT au service d’authentification dans le domaine du compte du client. Le service d’authentification renvoie un ticket TGT pour le service d’accord de tickets dans le domaine de l’ordinateur cible. Le TGT peut être réutilisé jusqu’à ce qu’il expire, mais le premier accès au service d’octroi de ticket d’un domaine requiert toujours un voyage vers le service d’authentification dans le domaine du compte du client.

-   Service de Ticket-Granting (TGS)

    Ce service émet des tickets pour la connexion aux ordinateurs dans son propre domaine. Lorsque les clients veulent accéder à un ordinateur, ils contactent le service d’accord de tickets dans le domaine de l’ordinateur cible, présentent un ticket TGT et demandent un ticket à l’ordinateur. Le ticket peut être réutilisé jusqu’à ce qu’il expire, mais le premier accès à un ordinateur requiert toujours un voyage vers le service d’accord de tickets dans le domaine du compte de l’ordinateur cible.

Le KDC d’un domaine se trouve sur un contrôleur de domaine, comme le Active Directory pour le domaine. Les deux services sont démarrés automatiquement par l' [*autorité de sécurité locale*](../secgloss/l-gly.md) (LSA) du contrôleur de domaine et exécutés dans le cadre du processus de LSA. Aucun service ne peut être arrêté. Si le KDC n’est pas disponible pour les clients réseau, le Active Directory est également indisponible et le contrôleur de domaine ne contrôle plus le domaine. Le système garantit la disponibilité de ces services de domaine et d’autres en permettant à chaque domaine d’avoir plusieurs contrôleurs de domaine, tous pairs. N’importe quel contrôleur de domaine peut accepter des demandes d’authentification et des demandes d’accord de tickets adressées au KDC du domaine.

Le nom de [*principal de sécurité*](../secgloss/s-gly.md) utilisé par le KDC dans un domaine est « krbtgt », comme spécifié par [RFC 4120](https://www.ietf.org/rfc/rfc4120.txt). Un compte pour ce principal de sécurité est créé automatiquement lors de la création d’un nouveau domaine. Le compte ne peut pas être supprimé et le nom ne peut pas être modifié. Une valeur de mot de passe aléatoire est affectée automatiquement au compte par le système lors de la création du domaine. Le mot de passe du compte du KDC est utilisé pour dériver une clé de chiffrement pour chiffrer et déchiffrer les TGT émis. Le mot de passe d’un compte d’approbation de domaine est utilisé pour dériver une clé inter-domaines pour le chiffrement des tickets de référence.

Toutes les instances du KDC au sein d’un domaine utilisent le compte de domaine pour le principal de sécurité « krbtgt ». Les clients adressent des messages au KDC d’un domaine en incluant le nom principal du service, « krbtgt » et le nom du domaine. Les deux éléments d’information sont également utilisés dans les tickets pour identifier l’autorité émettrice. Pour plus d’informations sur les formats de noms et les conventions d’adressage, consultez [RFC 4120](https://www.ietf.org/rfc/rfc4120.txt).

 

 
