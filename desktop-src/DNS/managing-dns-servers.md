---
title: Gestion des serveurs DNS
description: En savoir plus sur la gestion des serveurs DNS. Un serveur DNS est un ordinateur qui termine le processus de résolution de noms dans DNS.
ms.assetid: 9ac68e35-112a-44d3-918d-2caea47b6e52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d797e05bc326b35e48173082d9b36a2b334fd9
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010772"
---
# <a name="managing-dns-servers"></a>Gestion des serveurs DNS

Un serveur DNS est un ordinateur qui termine le processus de résolution de noms dans DNS. Les serveurs DNS contiennent des fichiers, appelés *fichiers de zone*, qui leur permettent de résoudre les noms en adresses IP (ou vice versa). Lorsqu’il est interrogé, un serveur DNS répond de l’une des trois façons suivantes :

-   Le serveur renvoie les informations de résolution de noms ou de résolution IP demandées.
-   Le serveur retourne un pointeur vers un autre serveur DNS qui peut traiter la demande.
-   Le serveur indique qu’il ne dispose pas des informations demandées.

Les serveurs DNS peuvent, au cours de la préparation, retourner les informations de résolution demandées, interroger d’autres serveurs DNS. Mais au-delà de cela, les serveurs DNS n’effectuent aucune opération autre que celles mentionnées dans la liste précédente.

Il existe trois types principaux de serveurs DNS : les serveurs principaux, les serveurs secondaires et les serveurs de mise en cache. Pour plus d’informations sur ces serveurs DNS, consultez [serveurs DNS](dns-servers.md) .

## <a name="administration-steps"></a>Étapes d’administration

Le fournisseur WMI DNS permet l’administration de serveurs DNS à partir du serveur lui-même ou à partir d’hôtes distants. Les étapes générales nécessaires à l’administration d’un serveur DNS à l’aide du fournisseur WMI DNS sont les suivantes :

-   Connexion au fournisseur WMI DNS
-   Obtention d’une instance de serveur
-   Énumération ou modification d’une propriété de serveur, ou utilisation d’une méthode

Pour illustrer comment implémenter ces étapes d’administration, des exemples sont fournis. Les tâches suivantes sont liées aux exemples de script associés.

-   [Arrêt d’un serveur DNS](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Démarrage d’un serveur DNS](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Redémarrage d’un serveur DNS](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Ajout d’une adresse IP](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Suppression d’une adresse IP](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Liste des propriétés du serveur DNS](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Affichage des types de propriété de serveur DNS](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Modification des propriétés d’un serveur DNS](dns-wmi-provider-samples-managing-a-dns-server.md)

 

 




