---
description: La fonction AreFileApisANSI détermine si les fonctions d’e/s de fichier utilisent la page de codes du jeu de caractères ANSI ou OEM.
ms.assetid: 97ed3b08-ca5d-4ac2-bf1a-7eec40f9ffc2
title: Détermination de la page de codes du jeu de caractères en cours
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e180d908605ec423314ef2197829fd95ff51a18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865545"
---
# <a name="determining-the-current-character-set-code-page"></a><span data-ttu-id="2a288-103">Détermination de la page de codes du jeu de caractères en cours</span><span class="sxs-lookup"><span data-stu-id="2a288-103">Determining the Current Character Set Code Page</span></span>

<span data-ttu-id="2a288-104">La fonction [**AreFileApisANSI**](/windows/desktop/api/fileapi/nf-fileapi-arefileapisansi) détermine si les fonctions d’e/s de fichier utilisent la page de codes du jeu de caractères ANSI ou OEM.</span><span class="sxs-lookup"><span data-stu-id="2a288-104">The [**AreFileApisANSI**](/windows/desktop/api/fileapi/nf-fileapi-arefileapisansi) function determines whether the file I/O functions are using the ANSI or OEM character set code page.</span></span> <span data-ttu-id="2a288-105">La fonction [**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) fait en sorte que les fonctions utilisent la page de codes ANSI.</span><span class="sxs-lookup"><span data-stu-id="2a288-105">The [**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) function causes the functions to use the ANSI code page.</span></span> <span data-ttu-id="2a288-106">La fonction [**SetFileApisToOEM**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) fait en sorte que les fonctions utilisent la page de codes OEM.</span><span class="sxs-lookup"><span data-stu-id="2a288-106">The [**SetFileApisToOEM**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) function causes the functions to use the OEM code page.</span></span>

<span data-ttu-id="2a288-107">Par défaut, les fonctions d’e/s de fichier utilisent des noms de fichiers ANSI.</span><span class="sxs-lookup"><span data-stu-id="2a288-107">By default, file I/O functions use ANSI file names.</span></span> <span data-ttu-id="2a288-108">Les fonctions exportées par Kernel32.dll qui acceptent ou retournent des noms de fichiers sont affectées par le paramètre de page de codes du fichier.</span><span class="sxs-lookup"><span data-stu-id="2a288-108">Functions exported by Kernel32.dll that accept or return file names are affected by the file code page setting.</span></span>

<span data-ttu-id="2a288-109">[**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) et [**SetFileApisToOEM**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) définissent la page de codes par processus, plutôt que par thread ou par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="2a288-109">Both [**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) and [**SetFileApisToOEM**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) set the code page per process, rather than per thread or per computer.</span></span>

 

 



