---
description: Exemple de code qui montre comment utiliser les flux de base du système de fichiers NTFS.
ms.assetid: 9cd5f418-404c-40f5-aa51-ef4d2a5f238e
title: Utilisation des flux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04edc73a3524d45eeead4cd6c0d508925e6caa5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204206"
---
# <a name="using-streams"></a><span data-ttu-id="2cdda-103">Utilisation des flux</span><span class="sxs-lookup"><span data-stu-id="2cdda-103">Using Streams</span></span>

<span data-ttu-id="2cdda-104">L’exemple de cette rubrique montre comment utiliser les flux de base du système de fichiers NTFS.</span><span class="sxs-lookup"><span data-stu-id="2cdda-104">The example in this topic demonstrates how to use basic NTFS file system streams.</span></span>

<span data-ttu-id="2cdda-105">Cet exemple crée un fichier, nommé « TestFile », avec une taille de 16 octets.</span><span class="sxs-lookup"><span data-stu-id="2cdda-105">This example creates a file, called "TestFile," with a size of 16 bytes.</span></span> <span data-ttu-id="2cdda-106">Toutefois, le fichier a également un type de flux supplémentaire :: $DATA, nommé « Stream », qui ajoute 23 octets supplémentaires qui ne sont pas signalés par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="2cdda-106">However, the file also has an additional ::$DATA stream type, named "Stream" which adds an additional 23 bytes that is not reported by the operating system.</span></span> <span data-ttu-id="2cdda-107">Par conséquent, lorsque vous affichez la propriété de taille de fichier pour le fichier, vous voyez uniquement la taille du flux par défaut :: $DATA pour le fichier.</span><span class="sxs-lookup"><span data-stu-id="2cdda-107">Therefore, when you view the file size property for the file, you see only the size of default ::$DATA stream for the file.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

void main( )
 {
  HANDLE hFile, hStream;
  DWORD dwRet;

  hFile = CreateFile( TEXT("TestFile"), // Filename
                      GENERIC_WRITE,    // Desired access
                      FILE_SHARE_WRITE, // Share flags
                      NULL,             // Security Attributes
                      OPEN_ALWAYS,      // Creation Disposition
                      0,                // Flags and Attributes
                      NULL );           // OVERLAPPED pointer
  if( hFile == INVALID_HANDLE_VALUE )
   {
    printf( "Cannot open TestFile\n" );
    return;
   }
  else
   {
    WriteFile( hFile,              // Handle
               "This is TestFile", // Data to be written
               16,                 // Size of data, in bytes
               &dwRet,             // Number of bytes written
               NULL );             // OVERLAPPED pointer
    CloseHandle( hFile );
    hFile = INVALID_HANDLE_VALUE;
   }

  hStream = CreateFile( TEXT("TestFile:Stream"), // Filename
                        GENERIC_WRITE,           // Desired access
                        FILE_SHARE_WRITE,        // Share flags
                        NULL,                    // Security Attributes
                        OPEN_ALWAYS,             // Creation Disposition
                        0,                       // Flags and Attributes
                        NULL );                  // OVERLAPPED pointer
  if( hStream == INVALID_HANDLE_VALUE )
    printf( "Cannot open TestFile:Stream\n" );
  else
   {
    WriteFile( hStream,                   // Handle
               "This is TestFile:Stream", // Data to be written
               23,                        // Size of data
               &dwRet,                    // Number of bytes written
               NULL);                     // OVERLAPPED pointer
    CloseHandle( hStream );
    hStream = INVALID_HANDLE_VALUE;
   }
}
```



<span data-ttu-id="2cdda-108">Si vous tapez **type TestFile** à l’invite de commandes, la sortie suivante s’affiche :</span><span class="sxs-lookup"><span data-stu-id="2cdda-108">If you type **Type TestFile** at a command prompt, it displays the following output:</span></span>

``` syntax
This is TestFile
```

<span data-ttu-id="2cdda-109">Toutefois, si vous tapez les mots **type TestFile : Stream**, cela génère l’erreur suivante :</span><span class="sxs-lookup"><span data-stu-id="2cdda-109">However, if you type the words **Type TestFile:Stream**, it generates the following error:</span></span>

<span data-ttu-id="2cdda-110">« La syntaxe du nom de fichier, du nom de répertoire ou de l’étiquette de volume est incorrecte. »</span><span class="sxs-lookup"><span data-stu-id="2cdda-110">"The filename, directory name, or volume label syntax is incorrect."</span></span>

<span data-ttu-id="2cdda-111">Pour afficher ce qui se trouve dans TestFile : Stream, utilisez l’une des commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="2cdda-111">To view what is in TestFile:stream, use one of the following commands:</span></span>

<span data-ttu-id="2cdda-112">**En savoir plus < TestFile : Stream**</span><span class="sxs-lookup"><span data-stu-id="2cdda-112">**More < TestFile:Stream**</span></span>

<span data-ttu-id="2cdda-113">**En savoir plus < TestFile : Stream : $DATA**</span><span class="sxs-lookup"><span data-stu-id="2cdda-113">**More < TestFile:Stream:$DATA**</span></span>

<span data-ttu-id="2cdda-114">Le texte affiché est le suivant :</span><span class="sxs-lookup"><span data-stu-id="2cdda-114">The text displayed is as follows:</span></span>

``` syntax
This is TestFile:Stream
```

## <a name="related-topics"></a><span data-ttu-id="2cdda-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2cdda-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2cdda-116">Flux de fichiers</span><span class="sxs-lookup"><span data-stu-id="2cdda-116">File Streams</span></span>](file-streams.md)
</dt> </dl>

 

 



