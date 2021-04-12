---
description: Un pointeur de fichier est une valeur de décalage de 64 bits qui spécifie l’octet suivant à lire ou l’emplacement de réception de l’octet suivant écrit.
ms.assetid: 1e8bc657-affa-4a17-8435-c93de5075a1d
title: Pointeurs de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4fc804711665c045361d40c69fb71a4959b4c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202218"
---
# <a name="file-pointers"></a><span data-ttu-id="e4811-103">Pointeurs de fichiers</span><span class="sxs-lookup"><span data-stu-id="e4811-103">File Pointers</span></span>

<span data-ttu-id="e4811-104">Lorsqu’un fichier est ouvert, Windows associe un *pointeur de fichier* avec le flux par défaut.</span><span class="sxs-lookup"><span data-stu-id="e4811-104">When a file is opened, Windows associates a *file pointer* with the default stream.</span></span> <span data-ttu-id="e4811-105">Ce pointeur de fichier est une valeur de décalage de 64 bits qui spécifie l’octet suivant à lire ou l’emplacement de réception de l’octet suivant écrit.</span><span class="sxs-lookup"><span data-stu-id="e4811-105">This file pointer is a 64-bit offset value that specifies the next byte to be read or the location to receive the next byte written.</span></span> <span data-ttu-id="e4811-106">Chaque fois qu’un fichier est ouvert, le système place le pointeur de fichier au début du fichier, qui est le décalage zéro.</span><span class="sxs-lookup"><span data-stu-id="e4811-106">Each time a file is opened, the system places the file pointer at the beginning of the file, which is offset zero.</span></span> <span data-ttu-id="e4811-107">Chaque opération de lecture et d’écriture avance le pointeur de fichier du nombre d’octets lus et écrits.</span><span class="sxs-lookup"><span data-stu-id="e4811-107">Each read and write operation advances the file pointer by the number of bytes being read and written.</span></span> <span data-ttu-id="e4811-108">Par exemple, si le pointeur de fichier se trouve au début du fichier et qu’une opération de lecture de 5 octets est demandée, le pointeur de fichier se trouvera au décalage 5 immédiatement après l’opération de lecture.</span><span class="sxs-lookup"><span data-stu-id="e4811-108">For example, if the file pointer is at the beginning of the file and a read operation of 5 bytes is requested, the file pointer will be located at offset 5 immediately after the read operation.</span></span> <span data-ttu-id="e4811-109">À mesure que chaque octet est lu ou écrit, le système avance le pointeur de fichier.</span><span class="sxs-lookup"><span data-stu-id="e4811-109">As each byte is read or written, the system advances the file pointer.</span></span> <span data-ttu-id="e4811-110">Le pointeur de fichier peut également être repositionné en appelant la fonction [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) .</span><span class="sxs-lookup"><span data-stu-id="e4811-110">The file pointer can also be repositioned by calling the [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) function.</span></span>

<span data-ttu-id="e4811-111">Quand le pointeur de fichier atteint la fin d’un fichier et que l’application tente de lire à partir du fichier, aucune erreur ne se produit, mais aucun octet n’est lu.</span><span class="sxs-lookup"><span data-stu-id="e4811-111">When the file pointer reaches the end of a file and the application attempts to read from the file, no error occurs, but no bytes are read.</span></span> <span data-ttu-id="e4811-112">Par conséquent, la lecture de zéro octet sans erreur signifie que l’application a atteint la fin du fichier.</span><span class="sxs-lookup"><span data-stu-id="e4811-112">Therefore, reading zero bytes without an error means the application has reached the end of the file.</span></span> <span data-ttu-id="e4811-113">L’écriture de zéro octet ne fait rien.</span><span class="sxs-lookup"><span data-stu-id="e4811-113">Writing zero bytes does nothing.</span></span>

<span data-ttu-id="e4811-114">Une application peut tronquer ou étendre un fichier à l’aide de la fonction [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile) .</span><span class="sxs-lookup"><span data-stu-id="e4811-114">An application can truncate or extend a file by using the [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile) function.</span></span> <span data-ttu-id="e4811-115">Cette fonction définit la fin du fichier à la position actuelle du pointeur de fichier.</span><span class="sxs-lookup"><span data-stu-id="e4811-115">This function sets the end of file to the current position of the file pointer.</span></span>

 

 



