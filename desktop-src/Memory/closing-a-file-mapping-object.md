---
description: Lorsqu’un processus est terminé avec l’objet de mappage de fichier, il doit détruire toutes les vues de fichier dans son espace d’adressage à l’aide de la fonction UnmapViewOfFile pour chaque affichage de fichier.
ms.assetid: d62d068c-9b1d-4dbf-8b21-31a636a41456
title: Fermeture d’un objet de mappage de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ab35152bd90d401ca7f30a7497d1f0b06263539
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094210"
---
# <a name="closing-a-file-mapping-object"></a>Fermeture d’un objet de mappage de fichier

Lorsqu’un processus est terminé avec l’objet de mappage de fichier, il doit détruire toutes les vues de fichier dans son espace d’adressage à l’aide de la fonction [**UnmapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile) pour chaque affichage de fichier.

L’annulation du mappage d’une vue mappée d’un fichier invalide la plage occupée par la vue dans l’espace d’adressage du processus et rend la plage disponible pour d’autres allocations. Elle supprime l’entrée de la plage de travail pour chaque page virtuelle non mappée faisant partie de la plage de travail du processus et réduit la taille du jeu de travail du processus. Elle décrémente également le nombre de partages de la page physique correspondante.

Les pages modifiées de la vue non mappée ne sont pas écrites sur le disque tant que leur nombre de partages n’atteint pas zéro, ou en d’autres termes, jusqu’à ce qu’ils soient démappés ou supprimés des jeux de travail de tous les processus qui partagent les pages. Même si les pages modifiées sont écrites « tardivement » sur le disque ; autrement dit, les modifications peuvent être mises en cache en mémoire et écrites sur le disque ultérieurement. Pour réduire le risque de perte de données en cas de panne de courant ou de panne du système, les applications doivent vider explicitement les pages modifiées à l’aide de la fonction [**FlushViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) .

Quand chaque processus se termine à l’aide de l’objet de mappage de fichier et que toutes les vues n’ont pas été mappées, il doit fermer le handle de l’objet de mappage de fichier et le fichier sur le disque en appelant [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle). Ces appels à **CloseHandle** échouent même si des vues de fichiers sont toujours ouvertes. Toutefois, le fait de laisser les vues de fichiers mappées entraîne des fuites de mémoire.

 

 
