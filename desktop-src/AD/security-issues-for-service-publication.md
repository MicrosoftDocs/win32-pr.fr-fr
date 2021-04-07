---
title: Problèmes de sécurité pour la publication de service
description: Le système limite la possibilité de créer, de modifier ou de supprimer des objets de point de connexion. Tenez compte de ces restrictions lorsque vous publiez un service.
ms.assetid: 38e20a47-738d-4951-ad74-249039afeb52
ms.tgt_platform: multiple
keywords:
- Problèmes de sécurité pour la publication de service AD
- Active Directory, utilisation, sécurité, problèmes de sécurité liés à la publication de services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fee5be89c490fa938cdc9c7cf3d7d72434a3dffa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671234"
---
# <a name="security-issues-for-service-publication"></a>Problèmes de sécurité pour la publication de service

Le système limite la possibilité de créer, de modifier ou de supprimer des objets de point de connexion. Tenez compte de ces restrictions lorsque vous publiez un service.

Les clients doivent être en mesure d’approuver les données publiées dans un objet de point de connexion dans l’annuaire. Pour cette raison, l’autorisation de créer un objet point de connexion est généralement limitée aux utilisateurs privilégiés, tels que les administrateurs de domaine. Cela empêche les utilisateurs non autorisés des clients conclure en créant des points de connexion non valides pour les services connus.

Les services ne doivent pas s’exécuter avec des privilèges d’administrateur de domaine. Cela signifie qu’un service ne peut généralement pas créer son propre point de connexion. Au lieu de cela, vous fournissez une application de configuration ou d’installation de service qui crée le point de connexion. Ce programme d’installation doit être exécuté par un utilisateur disposant des privilèges nécessaires.

Bien qu’un service ne puisse pas généralement créer son point de connexion, il doit être en mesure de mettre à jour les propriétés du point de connexion au moment de l’exécution. Les propriétés des points de connexion contiennent les données de liaison utilisées par les clients pour se connecter au service. Si les données de liaison changent, le service doit mettre à jour le point de connexion ; dans le cas contraire, les clients ne peuvent pas utiliser le service. Cela signifie que le programme d’installation doit également modifier le descripteur de sécurité sur l’objet de point de connexion pour permettre au service de lire et d’écrire les propriétés appropriées au moment de l’exécution. Pour plus d’informations et pour obtenir un exemple de code, consultez [activation du compte de service pour accéder aux propriétés SCP](enabling-service-account-to-access-scp-properties.md).

Un service s’exécutant sous le compte LocalSystem peut créer un point de connexion en tant qu’objet enfant sous son propre objet ordinateur dans le répertoire. Un tel service est une exception à la règle de services qui ne crée pas leurs propres points de connexion. Un service LocalSystem a également l’autorisation de modifier les propriétés des objets de point de connexion sous son propre objet ordinateur. N’oubliez pas qu’un service doit s’exécuter sous le compte LocalSystem uniquement si cela est absolument nécessaire. Pour plus d’informations, consultez [instructions de sélection d’un compte d’ouverture de session de service](guidelines-for-selecting-a-service-logon-account.md).

L’application qui crée un objet point de connexion, ou tout objet, doit avoir les autorisations créer des enfants pour la classe d’objet à créer dans le conteneur où l’objet sera créé. Pour supprimer un objet, le processus qui effectue l’opération doit avoir les autorisations supprimer les enfants pour la classe d’objet à supprimer sur le conteneur contenant l’objet, ou disposer des autorisations de suppression sur l’objet lui-même. Pour mettre à jour un point de connexion, le processus effectuant l’opération doit disposer d’un accès en écriture aux propriétés à mettre à jour sur l’objet.

 

 




