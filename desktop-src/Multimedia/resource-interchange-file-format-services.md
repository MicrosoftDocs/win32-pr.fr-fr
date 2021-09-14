---
title: Services de format de fichier de l’échange de ressources
description: Services de format de fichier de l’échange de ressources
ms.assetid: 8526794b-7b40-470f-94f7-935d7dbf9151
keywords:
- e/s de fichier multimédia, format RIFF (Resource Interchange File Format)
- e/s de fichier, format RIFF (Resource Interchange File Format)
- entrée et sortie (e/s), format RIFF (Resource Interchange File Format)
- E/s (entrée et sortie), format RIFF (Resource Interchange File Format)
- mmioOpen fonction)
- RIFF (Resource Interchange File Format)
- RIFF (Resource Interchange File Format)
- E/S RIFF
- Bloc RIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50cca3792ccded248951065c7b69f2e50d27e0ba
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121497"
---
# <a name="resource-interchange-file-format-services"></a>Services de format de fichier de l’échange de ressources

Le format par défaut pour les fichiers multimédias est RIFF (Resource Interchange File Format). Les fonctions d’e/s de fichier RIFF fonctionnent avec les services d’e/s de fichier de base mis en mémoire tampon et non mis en mémoire tampon. Vous pouvez ouvrir, lire et écrire des fichiers RIFF de la même façon que d’autres types de fichiers. Pour plus d’informations sur RIFF, consultez [fonctions et macros avifile](avifile-functions-and-macros.md).

Les fichiers RIFF utilisent des codes à quatre caractères pour identifier les éléments de fichier. Ces codes sont des quantités 32 bits représentant une séquence de un à quatre caractères alphanumériques ASCII, remplis sur la droite avec des espaces. Le type de données pour les codes à quatre caractères est **FourCC**. Utilisez la macro [**mmioFOURCC**](/windows/win32/api/vfw/nf-vfw-mmiofourcc) pour convertir quatre caractères en un code à quatre caractères. Pour convertir une chaîne se terminant par un caractère null en code à quatre caractères, utilisez la fonction [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) .

Le bloc de construction de base d’un fichier RIFF est un *segment*. Un segment est une unité logique de données multimédias, telle qu’une image unique dans un clip vidéo. Chaque segment contient les champs suivants :

-   Code à quatre caractères spécifiant l’identificateur de bloc
-   Valeur de mot double qui spécifie la taille du membre de données dans le bloc
-   Un champ de données

L’illustration suivante montre un bloc « RIFF » qui contient deux sous-segments.

![bloc riff contenant deux images de sous-bloc](images/mmio1.gif)

Un segment contenu dans un autre segment est un sous- *bloc*. Les seuls segments autorisés à contenir des sous-segments sont ceux dont l’identificateur de segment est « RIFF » ou « LIST ». Un segment qui contient un autre segment est appelé un *segment parent*. Le premier segment d’un fichier RIFF doit être un bloc « RIFF ». Tous les autres segments du fichier sont des sous-segments du bloc « RIFF ».

Les segments « RIFF » incluent un champ supplémentaire dans les quatre premiers octets du champ de données. Ce champ supplémentaire fournit le *type de formulaire* du champ. Le type de formulaire est un code à quatre caractères identifiant le format des données stockées dans le fichier. Par exemple, les fichiers audio Microsoft Waveform ont un type de formulaire « WAVE ».

Les segments « LIST » incluent également un champ supplémentaire dans les quatre premiers octets du champ de données. Ce champ supplémentaire contient le *type de liste* du champ. Le type de liste est un code à quatre caractères identifiant le contenu de la liste. Par exemple, un bloc « LIST » avec un type de liste « INFO » peut contenir des blocs « ICOP » et « ICRD » fournissant des informations sur la date de copyright et de création. L’illustration suivante montre un bloc « RIFF » qui contient un bloc « LIST » et un autre sous-bloc (le segment « LIST » contient deux sous-segments).

![bloc riff contenant une image de segment de liste](images/mmio2.gif)

Les services d’e/s de fichier multimédia incluent deux fonctions que vous pouvez utiliser pour naviguer parmi les segments d’un fichier RIFF : [**mmioAscend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend) et [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend). Vous pouvez utiliser ces fonctions comme fonctions de recherche de haut niveau. Quand vous descendez dans un segment, la position de fichier est définie sur le champ de données du segment (8 octets à partir du début du bloc). Pour les segments « RIFF » et « liste », la position de fichier est définie sur l’emplacement suivant le type de formulaire ou le type de liste (12 octets à partir du début du bloc). Lorsque vous vous retrouvez à l’extérieur d’un bloc, la position de fichier est définie à l’emplacement qui suit la fin du bloc.

Pour créer un nouveau bloc, utilisez la fonction [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) pour écrire un en-tête de bloc à la position actuelle dans un fichier ouvert. Les fonctions **mmioAscend**, **mmioDescend** et **mmioCreateChunk** utilisent la structure [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) pour spécifier et récupérer des informations sur les segments « riff ».

 

 