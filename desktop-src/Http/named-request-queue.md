---
title: File d’attente des demandes nommées
description: File d’attente des demandes nommées
ms.assetid: d0686a9b-fc3d-4b69-b083-d04b35ce5b50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d2174044f23f30470f3285e3c8fcf9bd2dbd474b10c306df7f2fbb215b992eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078342"
---
# <a name="named-request-queue"></a>File d’attente des demandes nommées

La fonctionnalité de la file d’attente des demandes du serveur HTTP version 2,0 autorise plusieurs applications, fonctionnant sous des processus et des comptes d’utilisateur distincts, à accéder à la file d’attente des demandes. La file d’attente des demandes est ouverte par nom et sécurisée à l’aide de listes de Access Control (ACL) pour s’assurer que les applications ne sont pas en mesure d’accéder aux données des autres. Un processus unique crée la file d’attente de demandes et accorde l’autorisation à d’autres processus d’utiliser la file d’attente des demandes. Ainsi, d’autres processus sur l’ordinateur accèdent à la file d’attente des demandes avec les privilèges minimum nécessaires pour traiter les demandes. Les dommages possibles au service HTTP, en raison de vulnérabilités dans le code tiers, sont minimisés lorsque les applications s’exécutent avec des privilèges minimum.

La file d’attente des demandes nommées est créée avec la fonction [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) . Lorsque la file d’attente de demandes est créée, l’application spécifie la liste de contrôle d’accès dans le paramètre *pSecurityAttribute* . La liste de contrôle d’accès, qui peut être définie uniquement lorsque la file d’attente des demandes est créée, permet aux processus de travail d’ouvrir la file d’attente des demandes, de recevoir des demandes et d’envoyer des réponses. Par défaut, les processus ne sont pas autorisés à ouvrir une file d’attente de demandes, sauf s’ils ont reçu l’autorisation dans la liste de contrôle d’accès. Les applications ne requièrent pas de privilèges d’administrateur pour créer la file d’attente des demandes.

La file d’attente des demandes doit être créée avec un nom spécifié dans le paramètre *pname* de [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) pour permettre à d’autres processus d’ouvrir la file d’attente des demandes. Si *pname* a la **valeur null**, une file d’attente de demandes sans nom est créée et aucun autre processus ne peut l’ouvrir.

## <a name="creator-and-controller-processes"></a>Processus de création et de contrôleur

Lorsque la file d’attente de demandes est créée, l’application peut l’ouvrir en tant que processus de contrôleur ou processus de création. Les processus du contrôleur et du créateur agissent en tant qu’administrateurs pour la file d’attente des demandes, mais le contrôleur n’effectue pas d’opérations d’e/s sur celui-ci. L’application indique qu’il s’agit d’un processus de contrôleur lorsque la file d’attente des demandes est créée en spécifiant le [](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue)contrôleur de balises de la **\_ \_ \_ file d’attente \_ \_ des demandes http Create** dans le paramètre *Flags* de HttpCreateRequestQueue. Si l’indicateur de contrôleur de l’indicateur de la **\_ \_ \_ file d’attente \_ \_ des demandes http Create** n’est pas défini, l’application est un processus de création.

La liste suivante contient les tâches effectuées par le processus du contrôleur et le processus de création :

-   Créez la file d’attente des demandes et spécifiez le nom.
-   Configurez la file d’attente des demandes à l’aide de la fonction [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) .
-   Interrogez les paramètres de configuration de la file d’attente des demandes à l’aide de la fonction [**HttpQueryRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpqueryrequestqueueproperty) .
-   Créez des groupes d’URL et associez-les à une file d’attente de demandes.
-   Définir la liste de contrôle d’accès qui spécifie les processus de travail qui sont autorisés à recevoir des e/s dans la file d’attente des demandes.
-   Appelez [**HttpWaitForDemandStart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) pour retarder l’instanciation des processus de travail jusqu’à ce que la première requête arrive dans la file d’attente des demandes.

En plus de ces tâches, le processus de création peut également effectuer des opérations d’e/s sur la file d’attente des demandes.

## <a name="worker-processes"></a>Processus de travail

Un processus de travail peut ouvrir une file d’attente de demandes existante uniquement si elle a reçu l’autorisation d’y accéder dans la liste de contrôle d’accès. Les processus de travail qui fonctionnent avec le moins de privilèges peuvent ouvrir une file d’attente de demandes et y effectuer des e/s. Les applications ouvrent une file d’attente de demandes existante en appelant [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) avec l' **\_ indicateur http Create \_ Request \_ Queue \_ \_ Open \_ existant** dans le paramètre *Flags* et le nom de la file d’attente des demandes dans le paramètre *pname* .

Le processus de travail exécute les fonctions suivantes :

-   Recevoir des demandes et envoyer des réponses sur la file d’attente de demandes.
-   Ouvrez une file d’attente de demandes existante par son nom. Le descripteur de la file d’attente de demandes retourné au processus de travail ne peut pas être utilisé pour configurer la file d’attente des demandes.
-   Interrogez les paramètres de configuration de la file d’attente des requêtes.

Le diagramme suivant montre le modèle de processus de travail pour les files d’attente de demandes. La file d’attente des demandes peut avoir plusieurs processus de travail qui traitent les e/s et un processus de création qui configure la file d’attente des demandes.

![modèle de processus de travail pour les files d’attente de demandes](images/namedrequestqueue.png)

 

 




