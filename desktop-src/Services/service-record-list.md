---
description: À mesure que chaque entrée de service est lue à partir de la base de données des services installés, le SCM crée un enregistrement de service pour le service.
ms.assetid: c0ee43e2-af9b-4578-9017-46a5ed50b938
title: Liste des enregistrements de service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ef0bdebed5e302b1dc59bea6494fd812ec506e7e6d2531634b2a6686b86bc98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888853"
---
# <a name="service-record-list"></a>Liste des enregistrements de service

À mesure que chaque entrée de service est lue à partir de la base de données des services installés, le SCM crée un enregistrement de service pour le service. Un enregistrement de service comprend les éléments suivants :

-   Nom du service
-   Type de démarrage (démarrage automatique ou à la demande)
-   État du service (voir la structure d' [**\_ État du service**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) ) <dl> Type  
    État actuel  
    Codes de contrôle acceptables  
    Code de sortie  
    Indicateur d’attente  
    </dl>
-   Pointer to dependency list

Le nom d’utilisateur et le mot de passe d’un compte sont spécifiés au moment de l’installation du service. Le SCM stocke le nom d’utilisateur dans le registre et le mot de passe dans une partie sécurisée de l’autorité de sécurité locale (LSA). L’administrateur système peut créer des comptes avec des mots de passe qui n’expirent jamais. L’administrateur système peut également créer des comptes avec des mots de passe qui expirent et gèrent les comptes en modifiant régulièrement les mots de passe.

Le SCM conserve deux copies du mot de passe d’un compte d’utilisateur, un mot de passe actuel et un mot de passe de sauvegarde. Le mot de passe spécifié lors de la première installation du service est stocké en tant que mot de passe actuel et le mot de passe de sauvegarde n’est pas initialisé. Lorsque le SCM tente d’exécuter le service dans le contexte de sécurité du compte d’utilisateur, il utilise le mot de passe actuel. Si le mot de passe actuel est correctement utilisé, il est également enregistré en tant que mot de passe de sauvegarde. Si le mot de passe est modifié à l’aide de la fonction [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) , ou du panneau de configuration services, le nouveau mot de passe est stocké en tant que mot de passe actuel et le mot de passe précédent est stocké en tant que mot de passe de sauvegarde. Si le SCM tente de démarrer le service et que le mot de passe actuel échoue, il utilise le mot de passe de sauvegarde. Si le mot de passe de sauvegarde est utilisé avec succès, il est enregistré en tant que mot de passe actuel.

Le SCM met à jour l’état du service lorsqu’un service envoie des notifications d’État à l’aide de la fonction [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) . Le SCM gère l’état d’un service de pilote en interrogeant le système d’e/s, au lieu de recevoir des notifications d’État, comme c’est le cas pour un service.

Un service peut enregistrer des informations de type supplémentaires en appelant la fonction [**SetServiceBits**](/windows/desktop/api/Lmserver/nf-lmserver-setservicebits) . Les fonctions [**NetServerGetInfo**](/windows/desktop/api/lmserver/nf-lmserver-netservergetinfo) et [**NetServerEnum**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum) obtiennent les types de service pris en charge.

 

 
