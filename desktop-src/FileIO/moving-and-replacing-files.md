---
description: Considérations relatives au déplacement et au remplacement de fichiers à l’aide des fonctions CopyFileEx, CreateFile, ReplaceFile et MoveFileEx.
ms.assetid: 4872af0d-42e8-4576-9aa9-4b8671375f2e
title: Déplacement et remplacement de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d7f08d2bd8d07645076620e839d7d12f5969502
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009903"
---
# <a name="moving-and-replacing-files"></a>Déplacement et remplacement de fichiers

Avant de pouvoir effectuer une opération de copie, le fichier source doit être fermé ou ouvert uniquement pour la lecture. Aucun thread ne peut ouvrir le fichier source pour l’écriture. Pour copier un fichier existant vers un nouveau fichier, utilisez la fonction [**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile) ou [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) . Les applications peuvent spécifier si **CopyFile** et **CopyFileEx** échouent si le fichier de destination existe déjà. Si le fichier de destination existe et qu’il est ouvert, il doit avoir été ouvert avec les autorisations de partage applicables. Pour plus d’informations, consultez [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea).

La fonction [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) permet également à une application de spécifier l’adresse d’une fonction de rappel (voir [**CopyProgressRoutine**](/windows/desktop/api/WinBase/nc-winbase-lpprogress_routine)) qui est appelée chaque fois qu’une autre partie du fichier a été copiée. L’application peut utiliser ces informations pour afficher un indicateur qui indique le nombre total d’octets copiés en pourcentage de la taille totale du fichier.

La fonction [**ReplaceFile**](/windows/desktop/api/WinBase/nf-winbase-replacefilea) remplace un fichier par un autre fichier, avec la possibilité de créer une copie de sauvegarde du fichier d’origine. La fonction conserve les attributs du fichier d’origine, tels que l’heure de création, les listes de contrôle d’accès et l’attribut de chiffrement.

Un fichier doit également être fermé avant qu’une application puisse le déplacer. Les fonctions [**MoveFile**](/windows/desktop/api/WinBase/nf-winbase-movefile) et [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa) copient un fichier existant vers un nouvel emplacement et supprime l’original.

La fonction [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa) permet également à une application de spécifier le mode de déplacement du fichier. La fonction peut remplacer un fichier existant, déplacer un fichier sur plusieurs volumes et retarder le déplacement du fichier jusqu’au redémarrage du système d’exploitation.

 

 



