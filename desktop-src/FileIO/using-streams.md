---
description: Exemple de code qui montre comment utiliser les flux de base du système de fichiers NTFS.
ms.assetid: 9cd5f418-404c-40f5-aa51-ef4d2a5f238e
title: Utilisation de Flux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23ebb6e2297c82e8643eb79ce66991b32fdf27e46fc723113a2866c79b2f8377
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078389"
---
# <a name="using-streams"></a>Utilisation de Flux

L’exemple de cette rubrique montre comment utiliser les flux de base du système de fichiers NTFS.

Cet exemple crée un fichier, nommé « TestFile », avec une taille de 16 octets. Toutefois, le fichier a également un type de flux supplémentaire :: $DATA, nommé « Stream », qui ajoute 23 octets supplémentaires qui ne sont pas signalés par le système d’exploitation. Par conséquent, lorsque vous affichez la propriété de taille de fichier pour le fichier, vous voyez uniquement la taille du flux par défaut :: $DATA pour le fichier.


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



Si vous tapez **type TestFile** à l’invite de commandes, la sortie suivante s’affiche :

``` syntax
This is TestFile
```

Toutefois, si vous tapez les mots **type TestFile : Stream**, cela génère l’erreur suivante :

« La syntaxe du nom de fichier, du nom de répertoire ou de l’étiquette de volume est incorrecte. »

Pour afficher ce qui se trouve dans TestFile : Stream, utilisez l’une des commandes suivantes :

**En savoir plus < TestFile : Stream**

**En savoir plus < TestFile : Stream : $DATA**

Le texte affiché est le suivant :

``` syntax
This is TestFile:Stream
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Flux de fichiers](file-streams.md)
</dt> </dl>

 

 



