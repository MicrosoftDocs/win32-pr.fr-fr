---
title: Le magasin commun SIS et les fichiers Common-Store
description: Tous les fichiers de sauvegarde gérés par la sauvegarde SIS (Single-Instance Store) sont appelés des fichiers de stockage commun.
ms.assetid: c6231c30-9d5a-428d-a94d-9dc8db933432
keywords:
- Sauvegarde des magasins courants
- Sauvegarde SIS (Single-Instance Store), magasins courants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b2f86b778b0a8db916fe580b8f833214523eb2e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842537"
---
# <a name="the-sis-common-store-and-common-store-files"></a>Le magasin commun SIS et les fichiers Common-Store

Tous les fichiers de sauvegarde gérés par la sauvegarde SIS (Single-Instance Store) sont appelés des *fichiers de stockage commun*. Un *magasin commun* existe sur chaque volume géré par SIS et contient tous les fichiers du magasin commun qui existent sur ce volume. Ce répertoire se trouve dans le répertoire racine du volume et est nommé « \\ SIS Common Store ». Le magasin commun est implémenté en tant que répertoire protégé contre l’accès utilisateur normal, car les fichiers du magasin commun sont conçus pour être accessibles directement uniquement par les fonctions d’API de sauvegarde SIS, et non pour les applications de sauvegarde et de restauration.

Les propriétés d’un fichier de magasin commun sont les suivantes :

-   Un fichier de magasin commun peut avoir un ou plusieurs liens pointant vers celui-ci.
-   Une fois créé, le contenu d’un fichier de magasin commun ne change jamais.
-   Les noms des fichiers de stockage commun sont globalement uniques, c’est-à-dire qu’ils sont uniques sur tous les volumes de tous les systèmes du monde, et la liaison entre un nom de fichier de magasin commun et ses données est globalement statique.

Lorsque SIS est activé sur un volume, une copie des fichiers dupliqués est alors créée dans le magasin commun, et tous les fichiers dupliqués sont remplacés par [des liens SIS](sis-links-and-reparse-points.md) pointant vers le fichier de magasin commun. Pour plus d’informations, consultez [activation ou désactivation de SIS sur un volume](/previous-versions/windows/it-pro/windows-server-storage-solutions/dd573313(v=ws.10)) dans la documentation technet.

Lorsque vous accédez à l’un des liens SIS pour une opération d’écriture, le filtre SIS restaure d’abord le contenu d’origine du fichier de liaison SIS à partir du fichier de magasin commun, le point d’analyse reliant le fichier de liaison SIS au magasin commun est supprimé, puis l’opération d’écriture est effectuée sur le fichier de destination d’origine.

Le fichier du magasin commun est supprimé uniquement lorsque le dernier lien SIS qui pointe vers celui-ci est supprimé.

 

 