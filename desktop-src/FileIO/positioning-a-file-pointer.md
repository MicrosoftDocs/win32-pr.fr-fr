---
description: Windows utilise un pointeur de fichier pour effectuer le suivi des octets lus ou écrits.
ms.assetid: 21c75d96-0357-422d-b12b-74c56f64ecf1
title: Positionnement d’un pointeur de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6588a3d65e71c2180c4e9753e65cd94ed070d36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518693"
---
# <a name="positioning-a-file-pointer"></a><span data-ttu-id="f4a6a-103">Positionnement d’un pointeur de fichier</span><span class="sxs-lookup"><span data-stu-id="f4a6a-103">Positioning a File Pointer</span></span>

<span data-ttu-id="f4a6a-104">Quand une application appelle [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) pour ouvrir un fichier pour la première fois, Windows place le [pointeur de fichier](file-pointers.md) au début du fichier.</span><span class="sxs-lookup"><span data-stu-id="f4a6a-104">When an application calls [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) to open a file for the first time, Windows places the [file pointer](file-pointers.md) at the beginning of the file.</span></span> <span data-ttu-id="f4a6a-105">Au fur et à mesure que les octets sont lus ou écrits dans le fichier, Windows avance le pointeur de fichier le nombre d’octets lus ou écrits.</span><span class="sxs-lookup"><span data-stu-id="f4a6a-105">As bytes are read from or written to the file, Windows advances the file pointer the number of bytes read or written.</span></span>

<span data-ttu-id="f4a6a-106">Une application peut positionner le pointeur de fichier sur un offset spécifié en appelant [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer).</span><span class="sxs-lookup"><span data-stu-id="f4a6a-106">An application can position the file pointer to a specified offset by calling [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer).</span></span>

<span data-ttu-id="f4a6a-107">La fonction [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) peut également être utilisée pour interroger la position actuelle du pointeur de fichier en spécifiant une méthode Move du **fichier \_ Current** et une distance de zéro.</span><span class="sxs-lookup"><span data-stu-id="f4a6a-107">The [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) function can also be used to query the current file pointer position by specifying a move method of **FILE\_CURRENT** and a distance of zero.</span></span>

 

 



