---
title: Journalisation W3C
description: La journalisation étendue W3C est le type de journalisation côté serveur qui peut être activé sur la session serveur ou le groupe d’URL.
ms.assetid: a08b8f9e-2247-43c6-b253-81f72001d8d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb53ccf3b6bf5383a0a4da62538b6fa516c500f8
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119944"
---
# <a name="w3c-logging"></a>Journalisation W3C

La journalisation étendue W3C est le type de journalisation côté serveur qui peut être activé sur la session serveur ou le groupe d’URL. Lorsque la journalisation W3C est activée sur un groupe d’URL, la journalisation est exécutée uniquement sur les demandes routées vers le groupe d’URL. Un fichier journal distinct est créé pour chaque groupe d’URL configuré pour activer la journalisation W3C.

Lorsque la journalisation W3C est activée sur la session serveur, elle fonctionne comme une forme centralisée de journalisation pour tous les groupes d’URL sous la session serveur. Un seul fichier journal est conservé pour tous les groupes d’URL dans la session serveur.

Le tableau suivant répertorie les champs qui peuvent être enregistrés par l’API du serveur HTTP. La table contient un sous-ensemble des constantes de [**\_ \_ champ de journal http**](http-log-field--constants.md) . Certains des champs répertoriés ci-dessous sont générés automatiquement par l’API du serveur HTTP en interne et ne figurent donc pas dans la structure de [**\_ données des \_ champs \_ du journal http**](/windows/desktop/api/Http/ns-http-http_log_fields_data) . La colonne « apparaît en tant que » contient le texte qui apparaît dans le fichier journal. Les données de la table sont dans l’ordre d’occurrence dans l’enregistrement du fichier journal.

Les champs qui ne sont pas marqués « API du serveur HTTP générés » doivent être transmis au sein de la structure des [**\_ données des \_ champs \_ du journal http**](/windows/desktop/api/Http/ns-http-http_log_fields_data) par application. L’application peut générer ces champs à partir de la structure de la [**\_ requête http**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)) qui lui est transmise.



| Champ                            | Apparaît comme      | Description                                                                                                                                | \_Membre de \_ données de champs du journal http \_ | \_Constantes de champs du journal http \_      |
|----------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|----------------------------------|
| Date                             | date            | Date à laquelle l’activité s’est produite.                                                                                                   | API du serveur HTTP générée.     | \_date du \_ champ du journal http \_           |
| Temps                             | time            | Heure, au format UTC (temps universel coordonné), à laquelle l’activité s’est produite.                                                             | API du serveur HTTP générée.     | \_heure du \_ champ du journal http \_           |
| Nom du service et numéro d’instance | s-SiteName      | Le nom et le numéro d’instance du service Internet qui s’exécutait sur le client.                                                              | NomService                    | \_nom du \_ site du champ du journal http \_ \_     |
| Nom du serveur                      | s-ComputerName  | Nom du serveur sur lequel l’entrée de fichier journal a été générée.                                                                          | ServerName                     | \_nom d' \_ ordinateur du champ de journal http \_ \_ |
| Adresse IP du serveur                | s-IP            | Adresse IP du serveur sur lequel l’entrée de fichier journal a été générée.                                                                    | ServerIp                       | \_ \_ \_ adresse IP du serveur de champs du journal http \_     |
| Méthode                           | CS-méthode       | Le verbe demandé, par exemple, une méthode d’extraction.                                                                                             | Méthode                         | \_méthode de \_ champ de journal http \_         |
| Ressource URI                         | CS-URI-souche     | Cible du verbe, par exemple, Default.htm.                                                                                          | UriStem                        | \_ \_ ressource URI du champ du journal http \_ \_      |
| Requête URI                        | CS-URI-Query    | Requête, le cas échéant, que le client essayait d’exécuter. Une requête URI est nécessaire uniquement pour les pages dynamiques. | UriQuery                       | \_ \_ requête URI de champ de journal http \_ \_     |
| Port du serveur                      | port s-          | Numéro de port du serveur configuré pour le service.                                                                                 | ServerPort                     | \_port du \_ serveur de champs du journal http \_ \_   |
| User Name                        | cs-username     | Nom de l’utilisateur authentifié ayant accédé au serveur. Les utilisateurs anonymes sont indiqués par un trait d'union.                                    | Nom d’utilisateur                       | \_nom d' \_ utilisateur du champ de journal http \_ \_     |
| Adresse IP du client                | c-ip            | Adresse IP du client à l’origine de la demande.                                                                                        | ClientIp                       | \_IP du \_ client du champ du journal http \_ \_     |
| Version du protocole                 | cs-version      | Version du protocole HTTP utilisée par le client.                                                                                            | API du serveur HTTP générée.     | \_version du \_ champ du journal http \_        |
| User Agent                       | CS (agent utilisateur)  | Type de navigateur utilisé par le client.                                                                                                     | UserAgent                      | \_ \_ agent utilisateur du champ du journal http \_ \_    |
| Cookie                           | CS (cookie)      | Contenu du cookie envoyé ou reçu, le cas échéant.                                                                                        | Cookie                         | \_cookie de \_ champ de journal http \_         |
| Referrer                         | CS (référent)    | Site que l’utilisateur a visité pour la dernière fois. Ce site a fourni un lien vers le site actuel.                                                        | Referrer                       | \_référent du \_ champ du journal http \_       |
| Host                             | CS-hôte         | Nom de l’en-tête de l’hôte, le cas échéant.                                                                                                              | Host                           | \_hôte de \_ champ de journal http \_           |
| État HTTP                      | SC-Status       | Code d’état HTTP.                                                                                                                      | ProtocolStatus                 | \_État du \_ champ du journal http \_         |
| Sous-état protocole               | SC-SubStatus    | Code d’erreur du sous-état.                                                                                                                  | SubStatus                      | \_sous- \_ État du champ du journal http \_ \_    |
| État Win32                     | sc-Win32-État | Code d’État Windows.                                                                                                                   | Win32Status                    | \_ \_ État Win32 du champ de journal http \_ \_  |
| Octets envoyés                       | SC-octets        | Nombre d’octets envoyés par le serveur.                                                                                                    | API du serveur HTTP générée.     | \_octets du champ du journal http \_ \_ \_ envoyés    |
| Octets reçus                   | CS-octets        | Nombre d’octets reçus et traités par le serveur.                                                                                  | API du serveur HTTP générée.     | \_octets du champ du journal http \_ \_ \_ reçus    |
| Durée                       | temps écoulé      | Durée nécessaire à l’exécution de l’action, en millisecondes.                                                                                  | API du serveur HTTP générée.     | \_temps de champ du journal http \_ \_ \_ pris    |
| ID de flux                      | streamid          | ID du flux.                                                                                  | API du serveur HTTP générée.     | \_ID de \_ flux de champ de journal http \_ \_       |



 

Le fichier journal est un format texte ASCII personnalisable. Les préfixes de champ du fichier sont définis comme suit :

| Préfixe    | Description                          |
|-----|---------------------------|
| s   | Actions du serveur.           |
| c   | Actions du client.           |
| SC  | Actions de serveur à client. |
| cs  | Actions client à serveur. |



 

L’application peut sélectionner un ou plusieurs champs du fichier journal étendu W3C, mais tous les champs ne contiennent pas d’informations. Pour les champs qui sont sélectionnés mais pour lesquels il n’y a pas d’informations, un trait d’Union (-) apparaît en tant qu’espace réservé. Si un champ contient un caractère non imprimable, l’API du serveur HTTP le remplace par un signe plus (+) pour conserver le format du fichier journal. Cela se produit généralement avec les attaques de virus, quand, par exemple, un utilisateur malveillant envoie des retours chariot et des sauts de ligne qui, s’ils ne sont pas remplacés par le signe plus (+), peuvent altérer le format du fichier journal. Les champs sont séparés par des espaces.

Si un champ est activé par le groupe d’URL ou la session de serveur, mais qu’il n’est pas sélectionné pour la demande, il apparaît dans le fichier journal avec un trait d’Union (-) en tant qu’espace réservé.

Les fichiers journaux sont créés lorsque la première requête arrive sur le groupe d’URL ou la session de serveur, ils ne sont pas créés lors de la configuration de la journalisation. L’exemple suivant montre la première entrée de fichier journal d’un fichier journal W3C avec les champs IP du client, nom d’utilisateur, adresse IP du serveur, port du serveur, méthode, ressource URI, requête URI, État et agent utilisateur activés :

``` syntax
#Software: Microsoft HTTP Server API 2.0  
#Version: 1.0   // the log file version as it's described by "https://www.w3.org/TR/WD-logfile".
#Date: 2002-05-02 17:42:15  // when the first log file entry was recorded, which is when the entire log file was created.
#Fields: date time c-ip cs-username s-ip s-port cs-method cs-uri-stem cs-uri-query sc-status cs(User-Agent)
2002-05-02 17:42:15 172.22.255.255 - 172.30.255.255 80 GET /images/picture.jpg - 200 Mozilla/4.0+(compatible;MSIE+5.5;+Windows+2000+Server)
```

Le champ date/heure est initialisé lorsque l’API du serveur HTTP reçoit le premier octet, avant que la demande ne soit analysée. L’horodateur de la durée d’exécution est arrêté lorsque la dernière opération d’envoi est effectuée. Le temps pris ne reflète pas le temps sur le réseau. La première demande au site montre un délai plus long que d’autres demandes similaires, car l’API du serveur HTTP ouvre le fichier journal avec la première requête.

 

 