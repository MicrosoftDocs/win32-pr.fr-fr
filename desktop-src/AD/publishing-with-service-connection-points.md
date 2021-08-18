---
title: Publication avec des points de connexion de service
description: Le schéma Active Directory définit une classe d’objet serviceConnectionPoint (SCP) pour permettre à un service de publier facilement des données spécifiques au service dans l’annuaire.
ms.assetid: 3544aa64-ecb0-48a1-ae49-05247a983842
ms.tgt_platform: multiple
keywords:
- Publication avec les points de connexion de service AD
- points de connexion de service AD
- points de connexion de service AD, publication avec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058c0a0e1f488ecdb50c14eb04788470b6bc25a0a3442457f1c57ced4b13efd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118184943"
---
# <a name="publishing-with-service-connection-points"></a>Publication avec des points de connexion de service

Le schéma Active Directory définit une classe d’objet **serviceConnectionPoint** (SCP) pour permettre à un service de publier facilement des données spécifiques au service dans l’annuaire. Les clients du service utilisent les données d’un SCP pour rechercher, se connecter à une instance de votre service et l’authentifier.

Cette section fournit une vue d’ensemble des points de connexion de service et des exemples de code qui montrent comment une application client/service utilise les SCP.

L’exemple de code suit ces étapes pour implémenter la publication de service avec SCP.

Pour plus d’informations et pour obtenir un exemple de code qui effectue ces étapes, consultez [création d’un point de connexion de service](creating-a-service-connection-point.md).

**Pour créer des SCP dans le répertoire lors de l’installation du service**

1.  Établissez une liaison avec l’objet ordinateur pour l’ordinateur hôte sur lequel l’instance de service est installée.
2.  Créez un objet SCP en tant qu’enfant de l’objet ordinateur, en spécifiant les valeurs initiales des attributs du SCP.
3.  Définissez des entrées de contrôle d’accès (ACE) dans le descripteur de sécurité de l’objet SCP pour permettre au service de modifier les propriétés SCP au moment de l’exécution.
4.  Mettez en cache l' **objectGUID** du SCP dans le registre sur l’ordinateur hôte du service.

Pour plus d’informations et pour obtenir un exemple de code qui effectue ces étapes, consultez [mise à jour d’un point de connexion de service](updating-a-service-connection-point.md).

**Pour mettre à jour les attributs SCP au démarrage du service**

1.  Récupérez l' **objectGUID** à partir du Registre et utilisez-le pour établir une liaison avec le SCP.
2.  Récupérez les attributs, tels que **servicednsname** et **serviceBindingInformation**, à partir du SCP. Comparez ces valeurs aux valeurs actuelles et mettez à jour le SCP si nécessaire.

Pour plus d’informations et pour obtenir un exemple de code qui effectue ces étapes, consultez [Comment les clients recherchent et utilisent un point de connexion de service](how-clients-find-and-use-a-service-connection-point.md).

**Pour rechercher et utiliser un SCP par une application cliente**

1.  Établissez une liaison avec le catalogue global et recherchez des objets dont l’attribut **Keywords** correspond au GUID du produit du service. Chaque objet trouvé est une instance du service. Sélectionnez une instance et récupérez le nom unique du SCP.
2.  Utilisez le nom unique pour effectuer une liaison au point de connexion de service.
3.  Récupérez les valeurs de différents attributs du SCP, par exemple **servicednsname** et **serviceBindingInformation**. Utilisez ces valeurs pour la connexion et l'authentification auprès de l'instance de service.

Pour plus d’informations sur les rôles qui peuvent créer et mettre à jour un SCP, consultez [problèmes de sécurité pour la publication de service](security-issues-for-service-publication.md).

Pour plus d’informations sur l’emplacement de la création d’un SCP, consultez [où créer un point de connexion de service](where-to-create-a-service-connection-point.md).

Pour plus d’informations sur le type de données à stocker dans un SCP, consultez [Propriétés du point de connexion de service](service-connection-point-properties.md).

Pour plus d’informations sur la façon dont un programme d’installation de service et le service fonctionnent ensemble pour gérer les données actuelles dans un SCP, consultez [création et gestion d’un point de connexion de service](creating-and-maintaining-a-service-connection-point.md).

 

 




