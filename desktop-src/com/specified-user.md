---
title: Utilisateur spécifié
description: Utilisateur spécifié
ms.assetid: ec7684fb-a9f1-4ef2-a7d4-07caf24b6023
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acce63aa502a8966cd0eb53c90dcca3c4454e80b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127294323"
---
# <a name="specified-user"></a>Utilisateur spécifié

La spécification d’un utilisateur particulier (et du mot de passe de l’utilisateur) est l’identité par défaut pour les serveurs COM. La raison pour laquelle cette identité est privilégiée est que personne ne doit être connecté sur l’ordinateur sur lequel le serveur est en cours d’exécution et que chaque client communique avec la même instance du serveur si le serveur inscrit sa fabrique de classes en tant qu’utilisation multiple. Si le serveur dispose d’une interface utilisateur graphique, vous ne devez pas choisir cette identité ; Si vous le faites, l’utilisateur ne sera pas en mesure de voir l’interface utilisateur.

Ce type de serveur dispose d’un jeton principal et peut accéder aux ressources distantes dans lesquelles il est possible qu’un serveur qui a l’identité de lancement de l’utilisateur ne puisse pas. Pour plus d’informations sur l’emprunt d’identité et les jetons d’accès, consultez [niveaux d’emprunt d’identité](impersonation-levels.md) et [masquage](cloaking.md).

L’exécution en tant que compte d’utilisateur fixe est plus sécurisée que l’identité de l’utilisateur interactif, car cette identité ne peut être affectée à l’application que par une personne qui a le mot de passe de l’utilisateur spécifique.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Identité de l'application](application-identity.md)
</dt> <dt>

[Utilisateur interactif](interactive-user.md)
</dt> <dt>

[Lancement de l’utilisateur](launching-user.md)
</dt> <dt>

[Identité du service](service-identity.md)
</dt> </dl>

 

 




