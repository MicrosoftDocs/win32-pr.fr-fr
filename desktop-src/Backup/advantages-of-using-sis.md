---
title: Avantages de l’utilisation de SIS
description: Les avantages de l’utilisation de SIS et de l’architecture de sauvegarde SIS sont les suivants.
ms.assetid: c72a14a1-92ae-4875-ae73-e277ed2b0c0d
keywords:
- Sauvegarde SIS (Single-Instance Store), avantages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcd1856ce54e817c25830f15f133c7d76c6a80fc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028665"
---
# <a name="advantages-of-using-sis"></a>Avantages de l’utilisation de SIS

L’utilisation de SIS et l’architecture de sauvegarde SIS présentent les avantages suivants :

-   Les connexions entre les liaisons SIS et les fichiers de sauvegarde sont gérées automatiquement par l’architecture SIS lorsque vos applications de sauvegarde appellent les fonctions de l’API de sauvegarde SIS.
-   Le contenu des points d’analyse SIS est opaque pour vos applications de sauvegarde et de restauration, ce qui garantit que les mises à niveau vers les éléments internes SIS ne nécessitent pas de modification de l’API SIS ou de vos applications de sauvegarde et de restauration qui appellent les fonctions API SIS. Vous devez uniquement recompiler votre application avec une nouvelle version de la DLL SIS, nommée Sisbkup.dll.
-   Étant donné que SIS est implémenté en tant que pilote de filtre de système de fichiers, il suit en permanence les connexions entre les liens SIS et les fichiers de sauvegarde. Une fois les fichiers sauvegardés et restaurés, la sauvegarde SIS garantit qu’une seule instance du fichier de sauvegarde sera sauvegardée et restaurée, quel que soit le nombre de liens SIS qui pointent vers celle-ci.

 

 




