---
description: Pour lire à partir d’une vue de fichier, déréférencez le pointeur retourné par la fonction MapViewOfFile comme indiqué dans les exemples ci-dessous.
ms.assetid: c2a3da09-d116-4c2c-9e6c-ec9e80c88b99
title: Lecture et écriture à partir d’un affichage des fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4458f98e1ea4239c01b77983ac13a9cb2eec5d86
ms.sourcegitcommit: ccf7dea7222b925441486fa564a1a61b69395562
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2021
ms.locfileid: "123463068"
---
# <a name="reading-and-writing-from-a-file-view"></a>Lecture et écriture à partir d’un affichage des fichiers

Pour lire à partir d’une vue de fichier, déréférencez le pointeur retourné par la fonction [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) comme indiqué dans les exemples ci-dessous.

La lecture ou l’écriture dans une vue de fichier d’un fichier autre que le fichier d’échange peut provoquer une exception dans l’exception **\_ d' \_ \_ erreur de page** . Par exemple, l’accès à un fichier mappé qui réside sur un serveur distant peut générer une exception si la connexion au serveur est perdue. Des exceptions peuvent également se produire en raison d’un disque saturé, d’une défaillance d’appareil sous-jacent ou d’un échec d’allocation de mémoire. Pour vous protéger contre les exceptions en raison d’erreurs d’entrée et de sortie (e/s), toutes les tentatives d’accès aux fichiers mappés en mémoire doivent être encapsulées dans des gestionnaires d’exceptions structurés. Lorsque vous recevez une **exception en cas d' \_ \_ \_ erreur de page** dans le filtre **\_ \_ except** , assurez-vous que l’adresse est dans le mappage auquel vous accédez actuellement. Si c’est le cas, récupérez ou basculez correctement. Sinon, ne gérez pas l’exception.

L’exemple suivant utilise le pointeur retourné par **MapViewOfFile** pour lire à partir de la vue de fichier :


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



L’exemple suivant utilise le pointeur retourné par **MapViewOfFile** pour écrire dans la vue de fichier :


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



La fonction [**FlushViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) copie le nombre spécifié d’octets de la vue de fichier dans le fichier physique, sans attendre que l’opération d’écriture en cache se produise :


```C++
  if (!FlushViewOfFile(lpMapAddress, dwBytesToFlush)) 
  {
    printf("Could not flush memory to disk (%d).\n", GetLastError()); 
  }
```



Si vous mappez un fichier compressé ou partiellement alloué sur une partition NTFS, vous risquez d’obtenir une erreur d’e/s supplémentaire lors de la pagination dans une partie du fichier. Dans ce cas, l’espace d’adressage mappé par [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) peut ne pas être sauvegardé par l’espace disque alloué. Cela est dû au fait qu’un fichier partiellement alloué peut comporter des zones de zéros pour lesquelles NTFS n’alloue pas d’espace disque, et un fichier compressé peut occuper moins d’espace disque que les données réelles qu’il représente. Si vous lisez ou écrivez dans une partie d’un fichier fragmenté ou compressé qui n’est pas sauvegardé par l’espace disque, le système d’exploitation peut tenter d’allouer de l’espace disque. Si le disque est plein, cela peut entraîner une exception indiquant une erreur d’e/s.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion structurée des exceptions](../debug/structured-exception-handling.md)
</dt> </dl>

 

 
