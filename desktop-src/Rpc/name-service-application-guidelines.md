---
title: Instructions pour les applications de service de noms
description: Lorsque vous développez votre application distribuée, vous devez fournir aux utilisateurs de l’application une méthode pour spécifier le nom sous lequel ils peuvent inscrire l’application dans la base de données de service de noms.
ms.assetid: cda997b3-6031-4c0f-affc-c766ba4b7fd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7e0e79f8ddb9e2076da8d7b8d2c275cb1b1941f6867bfea68dd46bc6c352d49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927828"
---
# <a name="name-service-application-guidelines"></a>Instructions pour les applications de service de noms

Lorsque vous développez votre application distribuée, vous devez fournir aux utilisateurs de l’application une méthode pour spécifier le nom sous lequel ils peuvent inscrire l’application dans la base de données de service de noms. Cette méthode peut se composer d’un fichier de données, d’une entrée de ligne de commande ou d’une boîte de dialogue.

Bien que l’architecture du service de noms RPC prenne en charge différentes méthodes d’organisation des entrées de serveur d’une application, elle est optimisée pour les recherches. Par conséquent, des mises à jour fréquentes peuvent nuire aux performances du service de noms et de l’application. Pour éviter d’exporter les informations inutilement, choisissez une conception qui permet au serveur de déterminer si ses informations se trouvent dans la base de données du service de noms. En outre, chaque instance de serveur doit exporter vers son propre nom d’entrée. Dans le cas contraire, il sera difficile pour une instance de modifier ses UUID d’objets ou séquences de protocole pris en charge sans perturber les informations d’une autre instance.

La méthode suivante évite ces pièges et fournit de bonnes performances, quel que soit le service de noms utilisé par votre réseau.

Pour commencer, concevez votre application de sorte que la première fois qu’une instance de serveur donnée démarre, qu’elle sélectionne un nom d’entrée de serveur unique et enregistre ce nom dans le Registre avec les autres informations de configuration de l’application. Ensuite, il exporte ses descripteurs de liaison et les UUID d’objet, le cas échéant, vers son entrée de service de nom.

Les appels suivants de l’instance de serveur doivent vérifier que l’entrée de service de nom est présente et contient l’ensemble correct d’UUID d’objets et de handles de liaison. Une entrée manquante peut signifier qu’un administrateur l’a supprimée ou qu’une panne de courant a entraîné la perte des informations de service de nom. Il est important de vérifier que les handles de liaison dans l’entrée sont corrects ; Si un administrateur ajoute la prise en charge TCP/IP à un ordinateur, par exemple, les serveurs RPC écoutent cette séquence de protocole lorsqu’ils appellent [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs). Toutefois, si le serveur ne met pas à jour l’entrée de service de nom, les clients ne seront pas informés que TCP est pris en charge.

Lorsque le client importe, il doit spécifier **null** comme nom d’entrée. Si vous spécifiez la **valeur null** , les fonctions de la bibliothèque Microsoft RPC recherchent l’interface dans toutes les entrées de service de nom du domaine ou du groupe de travail de l’ordinateur client, ce qui recherche les informations pour chaque instance.

Si vous utilisez des UUID d’objet pour représenter des objets connus tels que des imprimantes, vous pouvez utiliser une variante de cette méthode. Au lieu d’exporter des liaisons vers une entrée, concevez votre application afin que chaque instance crée une entrée pour chaque objet pris en charge, par exemple «/.:/ Printers/Laser1 "et"/.:/ Printers/Laser2.» Ensuite, le serveur doit exporter ses handles de liaison vers chaque entrée de serveur, ainsi que l’UUID d’objet correspondant à cette entrée.

Dans ce cas, un client peut rechercher une ressource par son nom en l’important à partir de l’entrée de serveur appropriée. elle ne requiert pas l’UUID de l’objet de la ressource. S’il a l’UUID de ressource, mais pas le nom, il peut importer à partir de l’entrée **null** .

 

 




