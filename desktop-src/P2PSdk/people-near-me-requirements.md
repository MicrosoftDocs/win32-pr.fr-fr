---
description: Conditions requises pour les personnes près de moi
ms.assetid: c7ab73fc-56a6-4b6c-820a-3f8e4a97cfaf
title: Conditions requises pour les personnes près de moi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ebbb904175184b6e9d06c807aa4b4ed645c93633114d6b9b64085e34dfa3683
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518349"
---
# <a name="people-near-me-requirements"></a>Conditions requises pour les personnes près de moi

pour que les [personnes près de moi](about-people-near-me.md) puissent fournir une connectivité transparente et une collaboration simple aux utilisateurs pour Windows les applications réseau homologues, les conditions suivantes sont remplies :

### <a name="people-discovery"></a>Découverte de personnes

La découverte de personnes permet à un utilisateur de découvrir et d’afficher l’ensemble des pairs qui se trouvent sur le sous-réseau local. Tous les ordinateurs sur le sous-réseau local doivent publier les noms des homologues connectés. les homologues répertoriés après une requête de découverte sont l’ensemble des utilisateurs qui exécutent Windows Vista et qui sont configurés pour publier un surnom pour d’autres utilisateurs à l’aide du voisinage [immédiat](about-people-near-me.md). Cette fonctionnalité est désactivée par défaut et doit être activée par l’utilisateur connecté.

> [!Note]  
> Les homologues distants découverts pendant le processus de découverte « People Near me » ne sont pas nécessairement les utilisateurs anticipés associés aux homologues découverts.

 

### <a name="extended-data-discovery"></a>Découverte étendue des données

La découverte étendue des données permet de rechercher des utilisateurs qui ont des intérêts spécifiques. Il est également possible pour les utilisateurs de spécifier qu’ils veulent publier des données supplémentaires sur eux-mêmes. Par exemple, les données peuvent présenter un intérêt professionnel spécifique au sein d’une conférence industrielle, en plus du surnom de l’utilisateur connecté.

### <a name="application-discovery"></a>Découverte des applications

La nature exacte de la collaboration ad hoc activée par voisinage immédiat est spécifique aux applications. Par exemple, la collaboration peut consister à discuter ou à partager des photos, toutes deux nécessitant des applications spécifiques. Pour que les personnes près de moi activent les activités de collaboration, l’ensemble des applications qui sont disponibles pour les scénarios voisinage immédiat doit également être publiée et détectable.

### <a name="subscription"></a>Abonnement

À l’aide d’un abonnement, les applications peuvent s’abonner pour suivre la présence, les applications et les modifications des objets d’une personne.

### <a name="invitation"></a>Invitation

Une fois que les personnes, les centres d’intérêt et les applications ont été découverts, la collaboration pair à pair, à l’aide d’une application voisinage immédiat, peut commencer une invitation et l’acceptation d’Exchange. L’homologue initiateur envoie un message d’invitation à un autre pair ou homologue. Les utilisateurs qui reçoivent l’invitation peuvent accepter ou refuser l’invitation. Lorsque l’invitation est acceptée, l’application homologue appropriée pour l’activité demandée est lancée.

### <a name="add-as-a-contact"></a>Ajouter en tant que contact

Si les utilisateurs établissent une activité de collaboration par le biais de voisinage immédiat et veulent conserver le contact au fil du temps, ils peuvent s’ajouter l’un à l’autre en tant que contact. Une fois cette opération effectuée, ils peuvent observer l’état de présence d’un utilisateur (par exemple, en ligne, hors connexion ou absent) et l’inviter à une activité de collaboration à tout moment sur Internet. Toute activité qui était possible avec la personne lorsqu’elle se trouvait à proximité est également possible avec un contact sur Internet.

### <a name="security"></a>Sécurité

Pour protéger les utilisateurs et les données échangées dans une activité de collaboration pair à pair, les utilisateurs disposent d’un contrôle de configuration sur ce qui est publié. Les utilisateurs doivent également accepter une invitation avant que la collaboration pair à pair puisse commencer. L’activité de collaboration est chiffrée avec un canal chiffré SSL (Secure Sockets Layer) (SSL) (également connu sous le nom de Schannel). SSL est un protocole de chiffrement pour protéger les communications basées sur TCP. Pour plus d’informations, consultez [Schannel](windows-vista-components-for-people-near-me.md). ces exigences sont prises en charge par un nouvel ensemble de composants dans l’architecture de [mise en réseau Windows homologue](what-is-peer-networking-.md)dans Windows Vista.

 

 



