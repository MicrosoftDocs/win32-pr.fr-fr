---
description: De nombreuses formes d’authentification sont basées sur l’idée qu’une entité peut prouver son identité si elle peut prouver qu’elle connaît une clé, telle qu’un mot de passe, que seul elle peut connaître.
ms.assetid: e17e4eb7-133e-46a0-8247-00a58b88bf61
title: Authentification par clé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deaadfdb61340955209ded22b5302e5436271ccc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203178"
---
# <a name="key-authentication"></a>Authentification par clé

De nombreuses formes d’authentification sont basées sur l’idée qu’une entité peut prouver son identité si elle peut prouver qu’elle connaît une clé, telle qu’un mot de passe, que seul elle peut connaître.

Les techniques d’authentification qui reposent sur un secret, tel qu’un mot de passe, doivent avoir un moyen de faire en sorte que le secret ne devienne pas une connaissance publique. Le propriétaire d’un mot de passe ne peut pas aller à une porte et fournir le mot de passe. Une personne autre que le doorkeeper peut être à l’écoute ; ou il s’agit peut-être d’une mauvaise porte. Afin de garder un secret, il doit exister un moyen de prouver qu’un utilisateur connaît le mot de passe sans révéler le mot de passe. C’est l’idée qui sous-tend l’authentification par clé secrète, une méthode de vérification utilisée dans le [*protocole Kerberos*](../secgloss/k-gly.md).

Notez que le « secret » dans l’authentification par clé secrète est que le processus d’authentification a lieu « en secret », autrement dit, sans jamais révéler réellement le contenu de la clé.

Pour que l’authentification par clé secrète fonctionne, les deux parties à une transaction doivent partager une [*clé de session*](../secgloss/s-gly.md) de chiffrement qui est également secrète, connue uniquement de celles-ci et pour aucune autre. La clé est [*symétrique*](../secgloss/s-gly.md); autrement dit, il s’agit d’une clé unique utilisée pour le chiffrement et le déchiffrement. L’une des parties du processus d’authentification prouve sa connaissance de la clé en chiffrant un message. L’autre partie prouve sa connaissance de la clé en déchiffrant le message.

 

 
