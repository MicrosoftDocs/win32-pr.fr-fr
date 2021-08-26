---
title: Journalisation NCSA
description: La journalisation étendue du NCSA est un type de journalisation côté serveur qui peut être activé sur un groupe d’URL.
ms.assetid: 14a2492a-3bcf-46f3-a3a5-1ea578516865
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9a5b9ef608da18264f4534c7e50e9672794a21bc61c91741feeb9e814c7afc8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078309"
---
# <a name="ncsa-logging"></a>Journalisation NCSA

La journalisation étendue du NCSA est un type de journalisation côté serveur qui peut être activé sur un groupe d’URL. Le format de fichier journal commun NCSA est un format texte ASCII fixe qui ne peut pas être personnalisé. Le fichier journal NCSA contient les présences dans le cache en mode noyau de l’API du serveur HTTP. Ce type de journalisation peut être activé uniquement sur un groupe d’URL ; elle ne peut pas être utilisée sur la session serveur.

Le format de fichier journal commun NCSA enregistre les données suivantes. Les données de la table sont dans l’ordre dans lequel elles se trouvent dans le fichier journal.



| Champ                                            | Description                                                                                                                                                                       |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Adresse de l’hôte distant                              | Adresse IP du client à l’origine de la demande.                                                                                                                               |
| Nom du journal distant                                  | Non utilisé. Cette valeur est toujours un trait d’Union.                                                                                                                                          |
| Nom d’utilisateur                                        | Nom de l’utilisateur authentifié ayant accédé au serveur. Les utilisateurs anonymes sont indiqués par un trait d'union. La meilleure pratique consiste à ce que l’application fournisse toujours le nom d’utilisateur. |
| Décalage de date, d’heure et GMT (Greenwich Mean Time) | Date et heure locales auxquelles l’activité s’est produite. Le décalage par rapport à l’heure de Greenwich est également indiqué.                                                                    |
| Version de la demande et du protocole                     | Version du protocole HTTP utilisée par le client.                                                                                                                                   |
| Code d’État du service                              | Code d’état HTTP. (Une valeur de 200 indique que la demande s’est terminée correctement.)                                                                                         |
| Octets envoyés                                       | Nombre d’octets envoyés par le serveur.                                                                                                                                           |



 

Tous les champs ne contiennent pas d’informations. Pour les champs pour lesquels il n’y a pas d’informations, un trait d’Union (-) apparaît en tant qu’espace réservé. Si un champ contient un caractère non imprimable, l’API du serveur HTTP le remplace par un signe plus (+) pour conserver le format du fichier journal. Cela se produit généralement avec les attaques de virus, quand, par exemple, un utilisateur malveillant envoie des retours chariot et des sauts de ligne qui, s’ils ne sont pas remplacés par le signe plus (+), peuvent altérer le format du fichier journal. Les champs sont séparés par des espaces et l’heure est enregistrée en tant qu’heure locale avec le décalage GMT.

L’exemple suivant illustre une entrée de fichier journal commune NCSA, telle qu’elle est affichée dans un éditeur de texte.

``` syntax
172.21.13.45 - Microsoft\JohnDoe [07/Apr/2004:17:39:04 -0800] 
"GET /scripts/iisadmin/ism.dll?http/serv HTTP/1.0" 200 3401
```

L’adresse IP du client est 172.21.13.45, et le nom d’utilisateur est Microsoft \\ johndoe. Le journal a été enregistré le 7 avril 2005 à 17:39:04 heure locale, avec un décalage de Greenwich de 8 heures. Le verbe de requête et la version de protocole étaient « obtenir/scripts/IISADMIN/ism.dll ? http/serv HTTP/1.0 ». Les codes d’État étaient 200 OK et le nombre d’octets envoyés par le client était 3401.

 

 




