---
description: Pour utiliser efficacement les ressources du système d’exploitation, une application doit fermer les fichiers lorsqu’ils ne sont plus nécessaires à l’aide de la fonction CloseHandle. Si un fichier est ouvert lorsqu’une application se termine, le système le ferme automatiquement.
ms.assetid: 6cf9694a-00c4-4750-8822-c25a1a102fd4
title: Fermeture et suppression de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03c74ad36f2f099b8d2430f52cc2c40b789862c691f56df1ccebcd20e82586ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696299"
---
# <a name="closing-and-deleting-files"></a>Fermeture et suppression de fichiers

Pour utiliser efficacement les ressources du système d’exploitation, une application doit fermer les fichiers lorsqu’ils ne sont plus nécessaires à l’aide de la fonction [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) . Si un fichier est ouvert lorsqu’une application se termine, le système le ferme automatiquement.

La fonction [**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) peut être utilisée pour supprimer un fichier à la fermeture. Un fichier ne peut pas être supprimé tant que tous les descripteurs ne sont pas fermés. Si un fichier ne peut pas être supprimé, son nom ne peut pas être réutilisé. Pour réutiliser un nom de fichier immédiatement, renommez le fichier existant.

Si vous supprimez un fichier ou un répertoire ouvert sur un ordinateur distant et qu’il a déjà été ouvert sur l’ordinateur distant sans le jeu d’autorisations lire le partage, n’appelez pas [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) ou [**OpenFile**](/windows/desktop/api/WinBase/nf-winbase-openfile) pour ouvrir d’abord le fichier ou le répertoire pour la suppression. Cela entraînera une violation de partage.

 

 
