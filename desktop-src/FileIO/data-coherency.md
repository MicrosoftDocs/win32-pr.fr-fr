---
description: Si les données sont cohérentes, les données sur le serveur et tous les clients sont synchronisées. Un système logiciel qui assure la cohérence des données est un système de contrôle de révision (RCS).
ms.assetid: cd33d20e-bf25-4a50-9b20-344495554434
title: Cohérence des données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f300296ff0fdc807beb95e2c03662814957bedb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867698"
---
# <a name="data-coherency"></a>Cohérence des données

Les données *cohérentes* sont des données qui sont identiques sur le réseau. En d’autres termes, si les données sont cohérentes, les données sur le serveur et tous les clients sont synchronisées. Un système logiciel qui assure la cohérence des données est un système de contrôle de révision (RCS). Un tel système est généralement relativement simple, avec un seul utilisateur autorisé à modifier un fichier spécifié à la fois. D’autres personnes peuvent lire le fichier, mais ne peut pas le modifier.

L’utilisateur qui peut modifier un fichier est dit qu’il l’a extrait. L’utilisateur archive ensuite le fichier modifié afin que d’autres utilisateurs puissent voir les modifications. Une fois que l’utilisateur a archivé un fichier dans, un autre utilisateur peut l’extraire.

Un RCS requiert l’intervention active des utilisateurs pour fonctionner de façon utile. Un système de fichiers qui fonctionne sur un réseau doit gérer le problème automatiquement.

Il est assez simple de fournir une mise en cache locale des données cohérentes lorsque vous disposez d’un seul thread sur un client qui accède à un fichier sur le réseau à la fois. Toutefois, dans la plupart des cas, de nombreux threads différents sur un ou plusieurs ordinateurs peuvent lire le même fichier. Cette situation est toujours relativement simple. Étant donné que les données du fichier sont statiques, chaque ordinateur client peut avoir sa propre copie locale sans aucune incidence sur la cohérence des données.

Une situation plus courante est l’un des threads qui modifient le fichier, et beaucoup d’autres threads le lisent. Au moment où une opération d’écriture se produit, tous les caches locaux de ce fichier sont obsolètes. Le serveur doit avertir chaque client pour abandonner son cache. Toutes les opérations de lecture ultérieures pour le fichier doivent être effectuées sur le réseau.

Dans une autre situation courante, plusieurs threads sur un ou plusieurs clients réseau peuvent essayer d’écrire dans le même fichier. Cette situation est semblable à celle dans laquelle plusieurs utilisateurs RCS veulent tous apporter des modifications au même fichier. Chaque utilisateur de la séquence doit extraire le fichier, apporter des modifications, puis archiver le fichier. De même, dans un schéma de mise en cache local, le serveur doit transmettre le privilège d’écriture dans un fichier à un thread client à la fois.

 

 



