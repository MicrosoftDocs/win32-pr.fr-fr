---
description: La certification numérique implique un processus de signature du certificat. Ce processus est décrit.
ms.assetid: bb0382fd-2924-429f-933b-84ab61debf20
title: Certification numérique X.509
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2f737a658e3e2c44876a23206f23a3d45ff3e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203033"
---
# <a name="x509-digital-certification"></a>Certification numérique X.509

Une tâche principale d’un [*certificat numérique*](../secgloss/d-gly.md) consiste à fournir l’accès à la [*clé publique*](../secgloss/p-gly.md)du sujet. Le certificat confirme également que la clé publique du certificat appartient au sujet du certificat. Par exemple, une [*autorité de certification*](../secgloss/c-gly.md) (ca) peut signer numériquement un message spécial (les informations de certificat) qui contient le nom d’un utilisateur, par exemple « Alice » et sa clé publique. Cela doit être fait de manière à ce que tout le monde puisse vérifier que le certificat a été émis et signé par l’autorité de certification. Si l’autorité de certification est approuvée et qu’il est possible de vérifier que le certificat d’Alice a été émis par cette autorité de certification, tout récepteur du certificat d’Alice peut faire confiance à la clé publique d’Alice à partir de ce certificat.

L’implémentation classique de la certification numérique implique un processus de signature du certificat.

Le processus se présente comme suit :

1.  Alice envoie une [*demande de certificat*](../secgloss/c-gly.md) signée contenant son nom, sa clé publique et éventuellement des informations supplémentaires à une autorité de certification.
2.  L’autorité de certification crée un message, *m*, à partir de la demande d’Alice. L’autorité de certification signe le message avec sa clé privée, en créant un message de signature distinct, *SIG*. L’autorité de certification renvoie le message, *m* et la signature, *SIG*, à Alice. Ensemble, *m* et *SIG* forment le certificat d’Alice.
3.  Alice envoie les deux parties de son certificat à Bob pour lui permettre d’accéder à sa clé publique.
4.  Bob vérifie la signature, *SIG* à l’aide de la clé publique de l’autorité de certification. Si la signature est valide, elle accepte la clé publique dans le certificat en tant que clé publique d’Alice.

Comme pour toute [*signature numérique*](../secgloss/d-gly.md), tout récepteur ayant accès à la clé publique de l’autorité de certification peut déterminer si une autorité de certification spécifique a signé le certificat. Ce processus ne nécessite pas d’accès à des informations confidentielles. Le scénario que nous venons de présenter suppose que Bob a accès à la clé publique de l’autorité de certification. Bob aura accès à cette clé s’il dispose d’une copie du certificat de l’autorité de certification qui contient cette clé publique.

Les certificats numériques [*X. 509*](../secgloss/x-gly.md) incluent non seulement le nom et la clé publique d’un utilisateur, mais également d’autres informations sur celui-ci. Ces certificats sont plus que des partages dans une hiérarchie numérique de confiance. Ils permettent à l’autorité de certification de donner au destinataire d’un certificat un moyen d’approuver non seulement la clé publique du sujet du certificat, mais également d’autres informations sur le sujet du certificat. Ces informations peuvent inclure, entre autres, une adresse de messagerie, une autorisation de signer des documents d’une valeur donnée, ou l’autorisation de devenir une autorité de certification et de signer d’autres certificats.

Les certificats X. 509 et de nombreux autres certificats ont une durée valide. Un certificat peut expirer et ne plus être valide. Une autorité de certification peut révoquer un certificat pour plusieurs raisons. Pour gérer les révocations, une autorité de certification gère et distribue une liste de certificats révoqués appelée [*liste de révocation de certificats*](../secgloss/c-gly.md) (CRL). Les utilisateurs du réseau accèdent à la liste de révocation pour déterminer la validité d’un certificat.

 

 
