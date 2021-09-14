---
title: Services de base
description: Services de base
ms.assetid: 7b77ed5d-0bd9-4926-b73f-afc7070fe314
keywords:
- e/s de fichier multimédia, services de base
- e/s de fichier, services de base
- entrée et sortie (e/s), services de base
- E/s (entrée et sortie), services de base
- e/s de base
- mmioOpen fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 688dc6b96c612d94524758acce5d8c742fc13a36
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007227"
---
# <a name="basic-services"></a>Services de base

L’utilisation des services d’e/s de base est semblable à l’utilisation des services d’e/s de fichier au moment de l’exécution de la bibliothèque Runtime C. Les fichiers doivent être ouverts pour pouvoir être lus ou écrits. Après la lecture ou l’écriture, le fichier doit être fermé. Vous pouvez également modifier l’emplacement actuel de lecture ou d’écriture dans un fichier ouvert.

Avant de commencer des opérations d’e/s dans un fichier, vous devez ouvrir le fichier à l’aide de la fonction [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) . Cette fonction retourne un handle de fichier de type **HMMIO**. Vous pouvez utiliser ce descripteur de fichier pour identifier le fichier ouvert lors de l’appel d’autres fonctions d’e/s de fichier.

> [!Note]  
> Un descripteur de fichier **HMMIO** n’est pas un descripteur de fichier standard. N’utilisez pas de descripteurs de fichiers **HMMIO** avec des fonctions d’e/s de fichier Win32 ou C.

 

Quand vous utilisez [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) pour ouvrir un fichier, vous utilisez un indicateur pour spécifier si vous l’ouvrez pour la lecture, l’écriture ou les deux. Vous pouvez également spécifier des indicateurs qui vous permettent de créer ou de supprimer un fichier. Utilisez la fonction [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) pour fermer un fichier une fois que vous avez terminé de le lire ou d’écrire dans celui-ci.

Vous pouvez lire et écrire des fichiers à l’aide des fonctions [**mmioRead**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread) et [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) , respectivement. L’opération de lecture ou d’écriture suivante se produit à la position de fichier actuelle ou au pointeur de fichier dans un fichier. La position actuelle du fichier est avancée chaque fois qu’un fichier est lu ou écrit.

Vous pouvez également modifier la position actuelle du fichier à l’aide de la fonction [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) . Vous devez vous assurer que vous spécifiez un emplacement valide dans un fichier. Si vous spécifiez un emplacement non valide, par exemple au-delà de la fin du fichier, **mmioSeek** peut ne pas renvoyer d’erreur, mais les opérations d’e/s ultérieures peuvent échouer.

Il existe des indicateurs que vous pouvez utiliser avec la fonction **mmioOpen** pour les opérations au-delà des e/s de fichier de base. En spécifiant une structure [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) , par exemple, vous pouvez ouvrir des fichiers de mémoire, spécifier une procédure d’e/s personnalisée ou fournir une mémoire tampon pour les e/s mises en mémoire tampon.

 

 