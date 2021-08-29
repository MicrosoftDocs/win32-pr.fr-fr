---
title: Gestion des enregistrements de ressources DNS
description: En savoir plus sur la gestion des enregistrements de ressources. Un enregistrement de ressource est l’unité d’entrée d’informations dans les fichiers de zone DNS, qui permet de résoudre toutes les requêtes DNS.
ms.assetid: ddad5f14-5a2d-4966-87b7-b354666f9e24
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61aa9e5c6711d0db763691beafdf8b49a4c3c3e670964e5345b753f91592f826
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692979"
---
# <a name="managing-dns-resource-records"></a>Gestion des enregistrements de ressources DNS

Un enregistrement de ressource, communément appelé RR, est l’unité d’entrée d’informations dans les fichiers de zone DNS. Les RR sont les blocs de construction de base des informations IP et de nom d’hôte et sont utilisés pour résoudre toutes les requêtes DNS. Les enregistrements de ressources sont dans un grand nombre de types afin de fournir des services de résolution de noms étendus.

Les différents types de RR ont des formats différents, car ils contiennent des données différentes. De nombreux RR partagent un format commun. Chaque serveur DNS contient des RR pour la partie de l’espace de noms pour laquelle il fait autorité.

Le fournisseur WMI DNS prend actuellement en charge les types RR suivants. Cliquez sur le nom de l’enregistrement de ressource pour accéder à sa page de référence.



| Enregistrement de ressource (dans le fournisseur)                             | Description                                                  |
|-----------------------------------------------------------|--------------------------------------------------------------|
| [**MicrosoftDNS \_ aType**](microsoftdns-atype.md)         | Nom de l’enregistrement de mappage d’adresse                               |
| [**MicrosoftDNS \_ AAAAType**](microsoftdns-aaaatype.md)   | Enregistrement d’adresse d’hôte à IPv6                                  |
| [**MicrosoftDNS \_ AFSDBType**](microsoftdns-afsdbtype.md) | Enregistrement du serveur de base de données du système de fichiers Andrew                    |
| [**MicrosoftDNS \_ ATMAType**](microsoftdns-atmatype.md)   | Enregistrement d’adresse-à-nom ATM                                   |
| [**MicrosoftDNS \_ CNAMEType**](microsoftdns-cnametype.md) | Enregistrement de [*nom canonique*](c-gly.md) |
| [**MicrosoftDNS \_ HINFOType**](microsoftdns-hinfotype.md) | Enregistrement d’informations sur l’hôte                                      |
| [**MicrosoftDNS \_ ISDNType**](microsoftdns-isdntype.md)   | Enregistrement réseau numérique de services intégrés                   |
| [**MicrosoftDNS, \_ KeyType**](microsoftdns-keytype.md)     | Enregistrement de clé. Consultez la RFC 2535                                     |
| [**MicrosoftDNS \_ MBType**](microsoftdns-mbtype.md)       | Enregistrement de boîte aux lettres                                               |
| [**MicrosoftDNS \_ MDType**](microsoftdns-mdtype.md)       | Agent de messagerie pour l’enregistrement de domaine                             |
| [**MicrosoftDNS \_ MFType**](microsoftdns-mftype.md)       | Agent de transfert du courrier pour l’enregistrement de domaine                  |
| [**MicrosoftDNS \_ MGType**](microsoftdns-mgtype.md)       | Enregistrement du groupe de messagerie                                            |
| [**MicrosoftDNS \_ MINFOType**](microsoftdns-minfotype.md) | Enregistrement d’informations de messagerie                                      |
| [**MicrosoftDNS \_ MRType**](microsoftdns-mrtype.md)       | Enregistrement de renommage de boîte aux lettres                                        |
| [**MicrosoftDNS \_ MXType**](microsoftdns-mxtype.md)       | Enregistrement du serveur de messagerie                                        |
| [**MicrosoftDNS \_ NSType**](microsoftdns-nstype.md)       | Enregistrement de serveur de noms                                           |
| [**MicrosoftDNS \_ NXTType**](microsoftdns-nxttype.md)     | Enregistrement suivant                                                  |
| [**MicrosoftDNS \_ PTRType**](microsoftdns-ptrtype.md)     | Adresse de l’enregistrement de mappage de nom                               |
| [**MicrosoftDNS \_ RPType**](microsoftdns-rptype.md)       | Enregistrement de personne responsable                                    |
| [**MicrosoftDNS \_ RTType**](microsoftdns-rttype.md)       | Itinéraire par enregistrement                                         |
| [**MicrosoftDNS \_ SIGType**](microsoftdns-sigtype.md)     | Enregistrement de signature                                             |
| [**MicrosoftDNS \_ SOAType**](microsoftdns-soatype.md)     | Autorité de certification                                           |
| [**MicrosoftDNS \_ SRVType**](microsoftdns-srvtype.md)     | Enregistrement de service                                               |
| [**MicrosoftDNS \_ TXTType**](microsoftdns-txttype.md)     | Enregistrement texte                                                  |
| [**MicrosoftDNS \_ WINSType**](microsoftdns-winstype.md)   | Enregistrement du serveur WINS                                           |
| [**MicrosoftDNS \_ WINSRType**](microsoftdns-winsrtype.md) | Enregistrement de recherche inversée WINS                                   |
| [**MicrosoftDNS \_ WKSType**](microsoftdns-wkstype.md)     | Enregistrement des services bien connus                                   |
| [**MicrosoftDNS \_ X25Type**](microsoftdns-x25type.md)     | Enregistrement de mappage d’adresse-à-nom X. 121                         |



 

## <a name="administration-steps"></a>Étapes d’administration

Le fournisseur WMI DNS permet d’administrer des RR à partir du serveur lui-même ou à partir d’hôtes distants. Les étapes générales nécessaires à l’administration des RR à l’aide du fournisseur WMI DNS sont les suivantes :

-   Connexion au fournisseur WMI DNS
-   Obtention d’une instance d’enregistrement de ressource
-   Énumération ou modification d’une propriété d’enregistrement de ressource ou utilisation d’une méthode

Les tâches suivantes sont liées aux exemples de script associés.

-   [Liste des types de ressources](dns-wmi-provider-samples-managing-dns-resource-records.md)
-   [Ajout d’un enregistrement de ressource](dns-wmi-provider-samples-managing-dns-resource-records.md)
-   [Suppression d’un enregistrement de ressource](dns-wmi-provider-samples-managing-dns-resource-records.md)
-   [Modification d’un enregistrement de ressource](dns-wmi-provider-samples-managing-dns-resource-records.md)

 

 




