---
description: Pour lire à partir d’une vue de fichier, déréférencez le pointeur retourné par la fonction MapViewOfFile comme indiqué dans les exemples ci-dessous.
ms.assetid: c2a3da09-d116-4c2c-9e6c-ec9e80c88b99
title: Lecture et écriture à partir d’un affichage des fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d98ec50dc6cd8b0224f2ba33a17ba80c7b0fc658
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106542042"
---
# <a name="reading-and-writing-from-a-file-view"></a><span data-ttu-id="e3038-103">Lecture et écriture à partir d’un affichage des fichiers</span><span class="sxs-lookup"><span data-stu-id="e3038-103">Reading and Writing From a File View</span></span>

<span data-ttu-id="e3038-104">Pour lire à partir d’une vue de fichier, déréférencez le pointeur retourné par la fonction [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) comme indiqué dans les exemples ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="e3038-104">To read from a file view, dereference the pointer returned by the [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) function as shown in the examples below.</span></span>

<span data-ttu-id="e3038-105">La lecture ou l’écriture dans une vue de fichier d’un fichier autre que le fichier d’échange peut provoquer une exception dans l’exception **\_ d' \_ \_ erreur de page** .</span><span class="sxs-lookup"><span data-stu-id="e3038-105">Reading from or writing to a file view of a file other than the page file can cause an **EXCEPTION\_IN\_PAGE\_ERROR** exception.</span></span> <span data-ttu-id="e3038-106">Par exemple, l’accès à un fichier mappé qui réside sur un serveur distant peut générer une exception si la connexion au serveur est perdue.</span><span class="sxs-lookup"><span data-stu-id="e3038-106">For example, accessing a mapped file that resides on a remote server can generate an exception if the connection to the server is lost.</span></span> <span data-ttu-id="e3038-107">Des exceptions peuvent également se produire en raison d’un disque saturé, d’une défaillance d’appareil sous-jacent ou d’un échec d’allocation de mémoire.</span><span class="sxs-lookup"><span data-stu-id="e3038-107">Exceptions can also occur because of a full disk, an underlying device failure, or a memory allocation failure.</span></span> <span data-ttu-id="e3038-108">Lors de l’écriture dans un affichage des fichiers, des exceptions peuvent également se produire parce que le fichier est partagé et qu’un autre processus a verrouillé une plage d’octets.</span><span class="sxs-lookup"><span data-stu-id="e3038-108">When writing to a file view, exceptions can also occur because the file is shared and a different process has locked a byte range.</span></span> <span data-ttu-id="e3038-109">Pour vous protéger contre les exceptions en raison d’erreurs d’entrée et de sortie (e/s), toutes les tentatives d’accès aux fichiers mappés en mémoire doivent être encapsulées dans des gestionnaires d’exceptions structurés.</span><span class="sxs-lookup"><span data-stu-id="e3038-109">To guard against exceptions due to input and output (I/O) errors, all attempts to access memory mapped files should be wrapped in structured exception handlers.</span></span> <span data-ttu-id="e3038-110">Lorsque vous recevez une **exception en cas d' \_ \_ \_ erreur de page** dans le filtre **\_ \_ except** , assurez-vous que l’adresse est dans le mappage auquel vous accédez actuellement.</span><span class="sxs-lookup"><span data-stu-id="e3038-110">When you receive **EXCEPTION\_IN\_PAGE\_ERROR** in your **\_\_except** filter, make sure that the address is within the mapping you are currently accessing.</span></span> <span data-ttu-id="e3038-111">Si c’est le cas, récupérez ou basculez correctement. Sinon, ne gérez pas l’exception.</span><span class="sxs-lookup"><span data-stu-id="e3038-111">If so, recover or fail gracefully; otherwise, do not handle the exception.</span></span>

<span data-ttu-id="e3038-112">L’exemple suivant utilise le pointeur retourné par **MapViewOfFile** pour lire à partir de la vue de fichier :</span><span class="sxs-lookup"><span data-stu-id="e3038-112">The following example uses the pointer returned by **MapViewOfFile** to read from the file view:</span></span>


```C++
  DWORD dwLength;

  __try
  {
    dwLength = *((LPDWORD) lpMapAddress);
  }
  __except(GetExceptionCode()==EXCEPTION_IN_PAGE_ERROR ?
    EXCEPTION_EXECUTE_HANDLER : EXCEPTION_CONTINUE_SEARCH)
  {
    // Failed to read from the view.
  }
```



<span data-ttu-id="e3038-113">L’exemple suivant utilise le pointeur retourné par **MapViewOfFile** pour écrire dans la vue de fichier :</span><span class="sxs-lookup"><span data-stu-id="e3038-113">The following example uses the pointer returned by **MapViewOfFile** to write to the file view:</span></span>


```C++
  DWORD dwLength;

  __try
  {
    *((LPDWORD) lpMapAddress) = dwLength;
  }
  __except (GetExceptionCode() == EXCEPTION_IN_PAGE_ERROR ? 
    EXCEPTION_EXECUTE_HANDLER : EXCEPTION_CONTINUE_SEARCH)
  {
    // Failed to write to the view.
  }
```



<span data-ttu-id="e3038-114">La fonction [**FlushViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) copie le nombre spécifié d’octets de la vue de fichier dans le fichier physique, sans attendre que l’opération d’écriture en cache se produise :</span><span class="sxs-lookup"><span data-stu-id="e3038-114">The [**FlushViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) function copies the specified number of bytes of the file view to the physical file, without waiting for the cached write operation to occur:</span></span>


```C++
  if (!FlushViewOfFile(lpMapAddress, dwBytesToFlush)) 
  {
    printf("Could not flush memory to disk (%d).\n", GetLastError()); 
  }
```



<span data-ttu-id="e3038-115">Si vous mappez un fichier compressé ou partiellement alloué sur une partition NTFS, vous risquez d’obtenir une erreur d’e/s supplémentaire lors de la pagination dans une partie du fichier.</span><span class="sxs-lookup"><span data-stu-id="e3038-115">If you are mapping a compressed or sparse file on an NTFS partition, there is additional potential for an I/O error when paging in a portion of the file.</span></span> <span data-ttu-id="e3038-116">Dans ce cas, l’espace d’adressage mappé par [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) peut ne pas être sauvegardé par l’espace disque alloué.</span><span class="sxs-lookup"><span data-stu-id="e3038-116">In this case, the address space mapped by [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) may not be backed by allocated disk space.</span></span> <span data-ttu-id="e3038-117">Cela est dû au fait qu’un fichier partiellement alloué peut comporter des zones de zéros pour lesquelles NTFS n’alloue pas d’espace disque, et un fichier compressé peut occuper moins d’espace disque que les données réelles qu’il représente.</span><span class="sxs-lookup"><span data-stu-id="e3038-117">This is because a sparse file can have regions of zeros for which NTFS does not allocate disk space, and a compressed file can take up less disk space than the actual data that it represents.</span></span> <span data-ttu-id="e3038-118">Si vous lisez ou écrivez dans une partie d’un fichier fragmenté ou compressé qui n’est pas sauvegardé par l’espace disque, le système d’exploitation peut tenter d’allouer de l’espace disque.</span><span class="sxs-lookup"><span data-stu-id="e3038-118">If you read from or write to a portion of a sparse or compressed file that is not backed by disk space, the operating system may try to allocate disk space.</span></span> <span data-ttu-id="e3038-119">Si le disque est plein, cela peut entraîner une exception indiquant une erreur d’e/s.</span><span class="sxs-lookup"><span data-stu-id="e3038-119">If the disk is full, this can result in an exception indicating an I/O error.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e3038-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e3038-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3038-121">Gestion structurée des exceptions</span><span class="sxs-lookup"><span data-stu-id="e3038-121">Structured Exception Handling</span></span>](../debug/structured-exception-handling.md)
</dt> </dl>

 

 
