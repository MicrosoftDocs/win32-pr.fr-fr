---
title: Liens SIS et points d’analyse
description: SIS est un pilote de filtre NTFS qui remplace les fichiers dupliqués par des liens de copie sur écriture (appelés « liens SIS ») qui pointent vers un fichier de stockage unique, ce qui réduit le disque et la surcharge de cache de ces fichiers.
ms.assetid: 1600a9ff-413c-4059-b04c-c862f6cf8f32
keywords:
- Sauvegarde des points d’analyse
- Sauvegarde SIS (Single-Instance Store), liens SIS
- Sauvegarde SIS (Single-Instance Store), points d’analyse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00f89901df6ce1fea1635d4250f2884ec9baf68fb1552766564909486c8ed00a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588859"
---
# <a name="sis-links-and-reparse-points"></a>Liens SIS et points d’analyse

SIS est un pilote de filtre NTFS qui remplace les fichiers dupliqués par des liens de copie sur écriture (appelés « liens SIS ») qui pointent vers un fichier de stockage unique, ce qui réduit le disque et la surcharge de cache de ces fichiers. Ce fichier de sauvegarde est contenu dans un [magasin commun](the-sis-common-store-and-common-store-files.md). L’implémentation de l’architecture SIS utilise des [points d’analyse](/windows/desktop/FileIO/reparse-points) qui contiennent des informations sur les liens SIS.

Les liens SIS sont implémentés en tant que fichiers épars, généralement avec la plupart des plages du fichier non alloué et un point d’analyse. La structure et le contenu d’un point d’analyse est opaque pour vos applications de sauvegarde et de restauration ; Toutefois, vos applications envoient et récupèrent les données de ces points d’analyse vers et à partir des fonctions de l’API SIS qui traitent les informations qu’elles contiennent. Les informations contenues dans un point d’analyse font référence à un seul fichier de stockage qui contient les données de fichier réelles. Ce fichier de sauvegarde est appelé un [fichier de magasin commun](the-sis-common-store-and-common-store-files.md)et il existe dans le magasin commun.

Lors de la restauration d’un lien SIS, votre application de restauration doit effectuer les étapes suivantes :

1.  Déterminez le ou les fichiers du magasin commun vers lesquels pointe le lien SIS.
2.  Si le ou les fichiers n’existent pas dans le magasin commun, restaurez le ou les fichiers avec le lien SIS.
3.  Si le lien SIS pointe vers un ou des fichiers du magasin commun qui existent sur le disque, restaurez uniquement le lien SIS. Rappelez-vous que les données des fichiers du magasin commun ne changent jamais ; par conséquent, si un fichier de magasin commun donné se trouve toujours sur le disque au moment de la restauration, il a le même contenu que lors de sa sauvegarde et il n’est pas nécessaire de le remplacer.

La seule surcharge supplémentaire requise pour les sauvegardes assistées par SIS est que votre application de sauvegarde doit sauvegarder le lien SIS et les données associées aux fichiers de sauvegarde. Toutes les opérations de sauvegarde et de restauration SIS sont locales sur un volume spécifique.

 

 