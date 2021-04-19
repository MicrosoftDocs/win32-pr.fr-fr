---
title: Journalisation IIS
description: La journalisation IIS est un type de journalisation côté serveur qui peut être activé sur un groupe d’URL.
ms.assetid: 2adfee73-090a-4bc1-827e-4b0e8075e2b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79d438d0926be2579fa526cc126c7f635a6eecd5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511236"
---
# <a name="iis-logging"></a>Journalisation IIS

La journalisation IIS est un type de journalisation côté serveur qui peut être activé sur un groupe d’URL. Le format de fichier journal IIS est un format texte ASCII fixe qui ne peut pas être personnalisé. Le fichier journal IIS contient les présences dans le cache en mode noyau de l’API du serveur HTTP. Ce type de journalisation peut être activé uniquement sur un groupe d’URL ; elle ne peut pas être utilisée sur la session serveur.

Le format de fichier journal IIS enregistre les données suivantes. Les données de la table sont dans l’ordre dans lequel elles se trouvent dans le fichier journal.



| Champ                | Description                                                                                                                                                                       |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Adresse IP du client    | Adresse IP du client à l’origine de la demande.                                                                                                                               |
| Nom d’utilisateur            | Nom de l’utilisateur authentifié ayant accédé au serveur. Les utilisateurs anonymes sont indiqués par un trait d'union. La meilleure pratique consiste à ce que l’application fournisse toujours le nom d’utilisateur. |
| Date                 | Date à laquelle l’activité s’est produite.                                                                                                                                          |
| Temps                 | Heure locale à laquelle l’activité s’est produite.                                                                                                                                    |
| Service et instance | Le nom et le numéro d’instance du service Internet qui s’exécutait sur le client.                                                                                                     |
| Nom du serveur          | Nom du serveur sur lequel l’entrée de fichier journal a été générée.                                                                                                                 |
| Adresse IP du serveur    | Adresse IP du serveur sur lequel l’entrée de fichier journal a été générée.                                                                                                           |
| Temps nécessaire           | Durée nécessaire à l’exécution de l’action, en millisecondes.                                                                                                                         |
| Octets client envoyés    | Nombre d’octets envoyés par le client.                                                                                                                                           |
| Octets serveur envoyés    | Nombre d’octets envoyés par le serveur.                                                                                                                                           |
| Code d’État du service  | Une valeur de 200 indique que la demande a été correctement exécutée.                                                                                                             |
| Code d’État Windows  | La valeur 0 (zéro) indique que la demande a été correctement exécutée.                                                                                                        |
| Type de demande         | Verbe de requête.                                                                                                                                                                 |
| Cible de l’opération  | Cible du verbe, par exemple, Default.htm.                                                                                                                                 |
| Paramètres           | Paramètres passés à un script.                                                                                                                                        |



 

Tous les champs ne contiennent pas d’informations. Pour les champs pour lesquels il n’y a pas d’informations, un trait d’Union (-) apparaît en tant qu’espace réservé. Si un champ contient un caractère non imprimable, l’API du serveur HTTP le remplace par un signe plus (+) pour conserver le format du fichier journal. Cela se produit généralement avec les attaques de virus, quand, par exemple, un utilisateur malveillant envoie des retours chariot et des sauts de ligne qui, s’ils ne sont pas remplacés par le signe plus (+), peuvent altérer le format du fichier journal. Les champs sont séparés par des virgules, ce qui rend le format plus facile à lire que les autres formats ASCII, qui utilisent des espaces pour les séparateurs. L’heure est enregistrée en heure locale. Le temps nécessaire est enregistré en millisecondes. Pour plus d’informations sur le champ temps nécessaire, consultez la rubrique [journalisation W3C](w3c-logging.md) .

L’exemple suivant illustre une entrée de fichier journal commune NCSA.

``` syntax
192.168.114.201, -, 03/20/05, 7:55:20, W3SVC2, SERVER, 
172.21.13.45, 4502, 163, 3223, 200, 0, GET, /DeptLogo.gif, -,
```

 

 




