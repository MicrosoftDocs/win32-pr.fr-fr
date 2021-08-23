---
description: Un espace de noms fait référence à une fonctionnalité permettant d’associer (au minimum) les attributs de protocole et d’adressage d’un service réseau avec un ou plusieurs noms conviviaux.
ms.assetid: 4139a8c2-d940-41e0-a3e8-fce3b70a1ff3
title: Modèle de résolution de noms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f23395cc6db5a93ec572f59e0d5ac6aaa7890c5c42a7966b86601eb190a54796
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118822779"
---
# <a name="name-resolution-model"></a>Modèle de résolution de noms

Un *espace de noms* fait référence à une fonctionnalité permettant d’associer (au minimum) les attributs de protocole et d’adressage d’un service réseau avec un ou plusieurs noms conviviaux. De nombreux espaces de noms sont actuellement utilisés en grande partie, y compris le système DNS ( [Domain Name System](../dns/dns-start-page.md) ), le [Active Directory Domain Services](../ad/active-directory-domain-services.md), le Bindery, le services d’annuaire NetWare (NDS) (NDS) de Novell et X. 500. Ces espaces de noms varient considérablement dans la façon dont ils sont organisés et implémentés. Certaines de leurs propriétés sont particulièrement importantes pour comprendre le point de vue de la résolution de noms Winsock.

## <a name="types-of-namespaces"></a>Types d’espaces de noms

Il existe trois types d’espaces de noms différents dans lesquels un service peut être inscrit :

-   Dynamique
-   statique
-   Persistante

Les espaces de noms dynamiques permettent aux services de s’inscrire avec l’espace de noms à la volée, et pour que les clients découvrent les services disponibles au moment de l’exécution. Les espaces de noms dynamiques s’appuient souvent sur des diffusions pour indiquer la disponibilité continue d’un service réseau. Les anciens exemples d’espaces de noms dynamiques incluent l’espace de noms SAP (Service Advertising Protocol) utilisé dans un environnement NetWare et l’espace de noms du protocole de liaison de noms (NBP) utilisé par AppleTalk. l’espace de noms PNRP (Peer Name resolution Protocol) utilisé sur Windows est un exemple plus récent d’espace de noms dynamique.

Les espaces de noms statiques requièrent que tous les services soient inscrits à l’avance, c’est-à-dire lorsque l’espace de noms est créé. Les fichiers d' *hôtes*, de *protocole* et de *services* utilisés par la plupart des implémentations TCP/IP sont un exemple d’espace de noms statique. sur Windows, ces fichiers se trouvent généralement dans le dossier *C : \\ Windows \\ system32 \\ drivers \\ etc* .

Les espaces de noms persistants permettent aux services de s’inscrire à l’espace de noms à la volée. Contrairement aux espaces de noms dynamiques, toutefois, les espaces de noms persistants conservent les informations d’inscription dans un stockage non volatile où il reste jusqu’à ce que le service demande sa suppression. Les espaces de noms persistants sont typified par des services d’annuaire tels que X. 500 et NDS (NetWare Directory Service). Ces environnements permettent l’ajout, la suppression et la modification des propriétés du service. En outre, l’objet de service représentant le service dans le service d’annuaire peut avoir plusieurs attributs associés au service. L’attribut le plus important pour les applications clientes est les informations d’adressage du service. DNS est un autre exemple d’espace de noms persistant. bien qu’il existe un moyen par programmation de résoudre les noms dns à l’aide de Windows sockets, le fournisseur d’espaces de noms dns dans Windows ne prend pas en charge l’enregistrement de nouveaux noms dns à l’aide de Winsock. Vous devez utiliser les fonctions DNS directement pour inscrire des noms DNS. Pour plus d’informations, consultez la [référence DNS](../dns/dns-reference.md).

## <a name="namespace-organization"></a>Organisation de l’espace de noms

De nombreux espaces de noms sont organisés hiérarchiquement. Certains, tels que X. 500 et NDS, permettent une imbrication illimitée. D’autres autorisent la combinaison de services dans un seul niveau de hiérarchie ou de groupe. Il s’agit généralement d’un *groupe de travail*. Lors de la construction d’une requête, il est souvent nécessaire d’établir un point de contexte dans une hiérarchie d’espaces de noms à partir de laquelle la recherche commence.

## <a name="namespace-provider-architecture"></a>Architecture du fournisseur d’espace de noms

Naturellement, les interfaces de programmation utilisées pour interroger les différents types d’espaces de noms et pour enregistrer des informations dans un espace de noms (si elles sont prises en charge) sont très différentes. Un *fournisseur d’espaces de noms* est un logiciel résident localement qui sait comment mapper l’index de l’espace de noms Winsock et un espace de noms existant (qui peut être implémenté localement ou accessible via le réseau). L’architecture du fournisseur d’espace de noms est illustrée comme suit :

![architecture du fournisseur d’espace de noms](images/ovrvw3-1.png)

Notez qu’il est possible pour un espace de noms donné, par exemple DNS, d’avoir plusieurs fournisseurs d’espaces de noms installés sur un ordinateur donné.

Comme indiqué ci-dessus, le terme « *service* générique » fait référence à la moitié du serveur d’une application client/serveur. Dans Winsock, un service est associé à une *classe de service*, et chaque instance d’un service particulier a un *nom de service* qui doit être unique dans la classe de service. le serveur FTP, SQL Server, XYZ Corp. employee Info server, etc., sont des exemples de classes de service. Comme l’exemple tente d’illustrer, certaines classes de service sont bien connues, tandis que d’autres sont uniques et spécifiques à une application verticale particulière. Dans les deux cas, chaque classe de service est représentée par un nom de classe et un identificateur de classe. Le nom de classe ne doit pas nécessairement être unique, mais l’identificateur de classe doit être. Les identificateurs globaux uniques (GUID) sont utilisés pour représenter des identificateurs de classe de service. Pour les services connus, les noms de classe et les identificateurs de classe (GUID) ont été préalloués, et les macros sont disponibles pour la conversion entre, par exemple, les numéros de port TCP (dans l’ordre des octets de l’hôte) et les GUID d’identificateur de classe correspondants. Pour les autres services, le développeur choisit le nom de la classe et utilise l’utilitaire Uuidgen.exe pour générer un GUID pour l’identificateur de classe.

La notion d’une classe de service existe pour permettre l’établissement d’un ensemble d’attributs qui sont communs à toutes les instances d’un service particulier. Cet ensemble d’attributs est fourni au moment où la classe de service est définie sur Winsock et est appelé « informations de schéma de la classe de service ». Lorsqu’un service est installé et mis à disposition sur un ordinateur hôte, ce service est considéré comme *instancié*, et son nom de service est utilisé pour distinguer une instance particulière du service des autres instances qui peuvent être connues de l’espace de noms.

Notez que l’installation d’une classe de service ne doit se produire que sur les ordinateurs sur lesquels le service s’exécute, et non sur tous les clients qui peuvent utiliser le service. Dans la mesure du possible, la \_32.dll Ws2 fournit les informations de schéma de la classe de service à un fournisseur d’espace de noms au moment où une instanciation d’un service doit être inscrite ou qu’une requête de service est lancée. Le \_32.dll Ws2 ne stocke pas ces informations elles-mêmes, mais tente de les récupérer à partir d’un fournisseur d’espace de noms qui a indiqué sa capacité à fournir ces données. Étant donné qu’il n’y a aucune garantie que le \_32.dll Ws2 peut fournir le schéma de la classe de service, les fournisseurs d’espaces de noms qui ont besoin de ces informations doivent disposer d’un mécanisme de secours pour l’obtenir via des moyens spécifiques à l’espace de noms.

Comme indiqué ci-dessus, Internet a adopté ce qui peut être appelé modèle de service centré sur l’hôte. Les applications qui ont besoin de localiser l’adresse de transport d’un service doivent généralement résoudre l’adresse d’un hôte spécifique connu pour héberger le service. À cette adresse, ils ajoutent le numéro de port connu et créent donc une adresse de transport complète. Pour faciliter la résolution des noms d’hôtes, un identificateur de classe de service spécial a été préalloué (**SVCID \_ hostname**). Une requête qui spécifie le nom d’hôte **SVCID \_** comme classe de service et spécifie un nom d’hôte pour le nom de l’instance de service retourne des informations sur l’adresse de l’hôte si la requête est réussie.

dans Windows sockets 2, les applications indépendantes du protocole doivent éviter d’avoir à comprendre les détails internes d’une adresse de transport. Par conséquent, la nécessité d’obtenir d’abord une adresse d’hôte, puis d’ajouter le port est problématique. Pour éviter cela, les requêtes peuvent également inclure le nom connu d’un service particulier et le protocole sur lequel le service fonctionne, par exemple FTP sur TCP. Dans ce cas, une requête réussie retourne une adresse de transport complète pour le service spécifié sur l’hôte indiqué, et l’application n’est pas requise pour inspecter les éléments internes d’une structure [**sockaddr**](sockaddr-2.md) .

Le système de noms de domaine d’Internet ne dispose pas d’un moyen bien défini pour stocker les informations de schéma de la classe de service. Par conséquent, les fournisseurs d’espaces de noms DNS pour Winsock peuvent uniquement prendre en charge les services TCP/IP connus pour lesquels un GUID de classe de service a été préalloué.

Dans la pratique, il ne s’agit pas d’une limitation sérieuse dans la mesure où les GUID de classe de service ont été préalloués pour l’ensemble des ports TCP et UDP, et les macros sont disponibles pour récupérer le GUID associé à un port TCP ou UDP avec le port exprimé dans l’ordre d’octet de l’hôte. Ainsi, tous les services familiers, tels que HTTP, FTP, Telnet, Whois, etc., sont bien pris en charge.

En poursuivant notre exemple de classe de service, les noms d’instance du service FTP peuvent être « alder.intel.com » ou « ftp.microsoft.com », tandis qu’une instance du serveur d’informations d’employé XYZ peut être nommée « XYZ Corp. Employee info Server version 3,5 ».

Dans les deux premiers cas, la combinaison du GUID de la classe de service pour FTP et du nom de l’ordinateur (fourni comme nom de l’instance de service) identifie de manière unique le service souhaité. Dans le troisième cas, le nom d’hôte où se trouve le service peut être découvert au moment de la requête de service, de sorte que le nom de l’instance de service n’a pas besoin d’inclure un nom d’hôte.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence DNS](../dns/dns-reference.md)
</dt> <dt>

[Structures de données de résolution de noms](name-resolution-data-structures-2.md)
</dt> <dt>

[Résolution de noms indépendante du protocole](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Inscription et résolution de noms](registration-and-name-resolution-2.md)
</dt> <dt>

[**SOCKADDR**](sockaddr-2.md)
</dt> <dt>

[Résumé des fonctions de résolution de noms](summary-of-name-resolution-functions-2.md)
</dt> </dl>

 

 
