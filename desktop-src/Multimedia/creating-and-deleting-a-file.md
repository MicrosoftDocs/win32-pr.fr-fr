---
title: Création et suppression d’un fichier
description: Création et suppression d’un fichier
ms.assetid: a4b4a310-7230-4f1d-b084-c47db39adaac
keywords:
- e/s de fichier multimédia, création de fichiers
- e/s de fichier, création de fichiers
- entrée et sortie (e/s), création de fichiers
- E/s (entrée et sortie), création de fichiers
- création de fichiers d’e/s
- e/s de fichier multimédia, suppression de fichiers
- e/s de fichier, suppression de fichiers
- entrée et sortie (e/s), suppression de fichiers
- E/s (entrée et sortie), suppression de fichiers
- suppression des fichiers d’e/s
- mmioOpen fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c22cd6330874d0b5da74d69193359c025c709c79
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725372"
---
# <a name="creating-and-deleting-a-file"></a>Création et suppression d’un fichier

Pour créer un fichier, définissez le paramètre *dwOpenFlags* de la fonction [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) sur MMIO \_ Create. L’exemple suivant crée un fichier et l’ouvre pour la lecture et l’écriture.


```C++
HMMIO hFile; 

hFile = mmioOpen("NEWFILE.TXT", NULL, MMIO_CREATE | MMIO_READWRITE); 
if (hFile != NULL) 
    // File created successfully. 
else 
    // File cannot be created. 
```



Si le fichier que vous créez existe déjà, il sera tronqué à une longueur égale à zéro.

Pour supprimer un fichier, définissez le paramètre *dwOpenFlags* de la fonction **mmioOpen** sur la valeur MMIO \_ Delete. Une fois que vous avez supprimé un fichier, il ne peut pas être récupéré par un moyen standard. Si votre application supprime un fichier à la demande d’un utilisateur, interrogez l’utilisateur avant de supprimer le fichier pour vous assurer que l’utilisateur souhaite le supprimer.

 

 