---
description: l’Windows Installer détermine s’il faut autoriser la suppression d’un assembly common language runtime basé sur une liste de clients qu’il conserve indépendamment de l’assembly.
ms.assetid: 3f83ad88-e6a4-484b-bcf5-8e2e65f1f41f
title: Suppression d’assemblys du global assembly cache
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47d50bc2856891c67952a27b27a27cf1cf2d1d65
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009656"
---
# <a name="removal-of-assemblies-from-the-global-assembly-cache"></a>Suppression d’assemblys du global assembly cache

l’Windows Installer détermine s’il faut autoriser la suppression d’un assembly common language runtime basé sur une liste de clients qu’il conserve indépendamment de l’assembly. le Windows Installer conserve un bit de code confidentiel pour représenter les clients Windows Installer de l’assembly. le programme d’installation épingle l’assembly pour le premier client Windows Installer et le désépingle lorsque le dernier client Windows Installer est supprimé. L’assembly gère un bit de code confidentiel pour chaque client d’un assembly.

la Windows Installer n’est pas directement responsable de la suppression physique des assemblys de common language runtime de l’ordinateur. le programme d’installation désépingle l’assembly lorsque la dernière Windows Installer client est supprimée. si le Windows Installer est le dernier client de l’assembly, le common language runtime permet de forcer un nettoyage synchrone de l’assembly. Le processus de nettoyage est atomique et il n’y a aucune provision pour une « restauration » à ce stade. Tout désépinglage de common language runtime assemblys doit se produire après que l’utilisateur a eu la possibilité d’annuler l’installation ou la suppression.

 

 



