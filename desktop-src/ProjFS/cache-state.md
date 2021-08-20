---
title: État du cache dans la racine de virtualisation
description: Décrit les différents États de cache qu’un fichier ou un répertoire géré par le fournisseur peut avoir.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 378973075017cc1ac06bf46840ea9d2d1058150a46587eb537374d501396ce30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792866"
---
# <a name="cache-state-in-the-virtualization-root"></a>État du cache dans la racine de virtualisation

Le fournisseur utilise le système de fichiers local sous la racine de virtualisation comme un cache des éléments qu’il gère.  Un élément (fichier ou répertoire) peut être dans l’un des six États du système de fichiers local :

* Les machines

  L’élément n’existe pas localement sur le disque.  Elle est projetée, c’est-à-dire synthétisée, pendant les énumérations de son répertoire parent.  Les éléments virtuels sont fusionnés avec tous les éléments qui peuvent exister sur le disque pour présenter le contenu complet du répertoire parent.

* Espace réservé

  Pour les fichiers : le contenu du fichier (flux de données principal) n’est pas présent sur le disque.  Les métadonnées du fichier (nom, taille, horodatages, attributs, etc.) sont mises en cache sur le disque.
  
  Pour les répertoires : tout ou partie des descendants immédiats de l’annuaire (fichiers et répertoires du répertoire) ne sont pas présents sur le disque, c’est-à-dire qu’ils sont toujours virtuels.  Les métadonnées du répertoire (nom, horodatages, attributs, etc.) sont mises en cache sur le disque.

* Espace réservé hydraté

  Pour les fichiers : le contenu et les métadonnées du fichier ont été mis en cache sur le disque.  Également appelé « fichier partiel ».
  
  Pour les répertoires : un répertoire qui a été créé sur le disque en tant qu’espace réservé ne devient jamais un répertoire d’espace réservé hydraté.  Cela permet au fournisseur d’ajouter ou de supprimer des éléments de l’annuaire dans son magasin de stockage et de faire en sorte que ces modifications soient reflétées dans le cache local.

* Espace réservé de modification (hydraté ou non)

  Les métadonnées de l’élément ont été modifiées localement et ne sont plus un cache de son état dans le magasin du fournisseur. Notez que la création ou la suppression d’un fichier ou d’un répertoire dans un répertoire d’espaces réservés entraîne l’indisponibilité de ce répertoire.

* Fichier/répertoire complet

  Pour les fichiers : le contenu du fichier (flux de données principal) a été modifié.  Le fichier n’est plus un cache de son état dans le magasin du fournisseur.  Les fichiers qui ont été créés sur le système de fichiers local (par exemple, qui n’existent pas dans le magasin du fournisseur) sont également considérés comme des fichiers complets.
  
  Pour les répertoires : les répertoires qui ont été créés sur le système de fichiers local (par exemple, qui n’existent pas dans le magasin du fournisseur) sont considérés comme des répertoires complets.  Un répertoire créé sur le disque en tant qu’espace réservé ne devient jamais un répertoire complet.
  
* Objet tombstone

  Espace réservé masqué spécial qui représente un élément qui a été supprimé du système de fichiers local.  Lorsqu’un répertoire est énuméré, ProjFS fusionne l’ensemble d’éléments locaux (espaces réservés, fichiers complets, etc.) avec le jeu d’éléments projetés virtuels.  Si un élément apparaît dans les jeux locaux et prévus, l’élément local est prioritaire.  Si un fichier n’existe pas dans le système de fichiers local, il n’y a pas d’état local. par conséquent, il apparaît dans l’énumération.  Toutefois, si cet élément a été supprimé, son affichage dans l’énumération est inattendu.  Le remplacement d’un élément supprimé par un objet tombstone entraîne les effets suivants :

  * Énumérations pour ne pas révéler l’élément.
  * Le fichier s’ouvre et s’attend à ce que l’élément existe, par exemple, « fichier introuvable ».
  * Les créations de fichier qui s’attendent à une opération réussie uniquement si l’élément n’existe pas, ProjFS supprime l’objet tombstone dans le cadre de l’opération.

Pour illustrer les États ci-dessus, considérez la séquence suivante, en fonction d’un fournisseur ProjFS qui a un fichier unique « foo.txt » situé dans la racine de virtualisation C:\Root.

1. Une application énumère C:\Root.  Il voit le fichier virtuel « foo.txt ».  Étant donné que le fichier n’a pas encore été accédé, le fichier n’existe pas sur le disque.
1. L’application ouvre un handle pour C:\root\foo.txt.  ProjFS indique au fournisseur de créer un espace réservé pour celui-ci.
1. L’application lit le contenu du fichier.  Le fournisseur fournit le contenu du fichier à ProjFS et il est mis en cache dans C:\root\foo.txt.  Le fichier est maintenant un espace réservé hydraté.
1. L’application met à jour l’horodateur de la dernière modification.  Le fichier est maintenant un espace réservé hydraté modifié.
1. L’application ouvre un handle pour l’accès en écriture au fichier.  C:\root\foo.txt est désormais un fichier complet.
1. L’application supprime C:\root\foo.txt.  ProjFS remplace le fichier par un objet tombstone.  Désormais, lorsque l’application énumère C:\Root, elle ne voit pas foo.txt.  S’il tente d’ouvrir le fichier, l’ouverture échoue avec ERROR_FILE_NOT_FOUND.
