---
description: De nombreuses fonctions renvoient un nombre potentiellement important de données à une adresse fournie comme l’un des paramètres par l’application.
ms.assetid: ef99edef-39b2-4d78-9c01-13720215d47f
title: Récupération de données de longueur inconnue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd30620018f3c4871bd27299c3dd21ae42936c51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863862"
---
# <a name="retrieving-data-of-unknown-length"></a>Récupération de données de longueur inconnue

De nombreuses fonctions renvoient un nombre potentiellement important de données à une adresse fournie comme l’un des paramètres par l’application. Dans tous ces cas, l’opération est effectuée de façon similaire, si elle n’est pas identique. Le paramètre qui pointe vers l’emplacement des données retournées utilise la Convention de notation où PB ou PV sont les deux premiers caractères du nom de paramètre. PCB est un autre paramètre dont le nom du paramètre contient les trois premiers caractères. Ce paramètre représente la taille, en octets, des données qui seront retournées à l’emplacement PB ou PV. Par exemple, considérez la spécification de fonction suivante :

``` syntax
#include <windows.h>

BOOL WINAPI SomeFunction(
  PCCRL_CONTEXT pCrlContext,  // in
  DWORD dwPropId,             // in
  BYTE *pbData,               // out
  DWORD *pcbData              // in/out
);
```

Dans cet exemple, *pbData* est un pointeur vers l’emplacement où les données seront retournées, et *pcbData* est la taille, en octets, des données retournées.

> [!Note]  
> Le paramètre Companion du paramètre PCB peut parfois comporter un préfixe légèrement différent, tel que p ou PV. En outre, pour les paramètres auxiliaires utilisant la combinaison de préfixes PWSZ et PCCh, le paramètre PCCh est le nombre, en caractères ([*Unicode*](../secgloss/u-gly.md) ou [*ASCII*](../secgloss/a-gly.md), le cas échéant), des données retournées.

 

Si la mémoire tampon spécifiée par le paramètre *pbData* n’est pas assez grande pour contenir les données retournées, la fonction définit le code d’erreur \_ plus de \_ données (qui peut être vu en appelant la fonction [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) ) et stocke la taille de mémoire tampon requise, en octets, dans la variable vers laquelle pointe *pcbData*.

Si **null** est entrée pour *pbData* et *pcbData* n’est pas **null**, aucune erreur n’est retournée et la fonction retourne la taille, en octets, de la mémoire tampon nécessaire dans la variable vers laquelle pointe *pcbData*. Cela permet à une application de déterminer la taille de, et la meilleure façon d’allouer, une mémoire tampon pour les données retournées.

> [!Note]  
> Lorsque la **valeur null** est entrée pour *pbData* afin de déterminer la taille nécessaire pour s’assurer que les données retournées tiennent dans la mémoire tampon spécifiée, le deuxième appel à la fonction qui remplit la mémoire tampon avec les données souhaitées peut ne pas utiliser la mémoire tampon entière. Après le deuxième appel, la taille réelle des données retournées est contenue dans *pcbData*. Utilisez cette taille lors du traitement des données.

 

L’exemple suivant montre comment les paramètres d’entrée et de sortie peuvent être implémentés à cet effet.


```C++
//-------------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)

void MyHandleError(char *s);

void main()
{

// Set up SomeFunction variables.
PCCRL_CONTEXT pCrlContext; // Initialized elsewhere.
DWORD dwPropId;            // Initialized elsewhere.
DWORD cbData;
BYTE  *pbData;

// Call SomeFunction to set cbData, the size of 
// the buffer needed for pbData.
if(SomeFunction(
     pCrlContext, 
     dwPropId, 
     NULL, 
     &cbData))
{
       printf("The function succeeded.\n");
}
else
{

// The function call failed. Handle the error.
       MyHandleError("Function call failed.");
}

// The call succeeded; the size for the needed buffer, in bytes, 
// now resides in cbData.

// Malloc memory for the size of the message.
if(pbData = (BYTE*)malloc(cbData))
{
   printf("Memory has been allocated.\n");
}
else
{

   // The allocation failed. Write an error message and exit.
   MyHandleError("Malloc operation failed. ");
}

// The space for the buffer has been allocated.
// Call SomeFunction to fill the buffer with the data.
if(SomeFunction(
      pCrlContext, 
      dwPropId, 
      pbData, 
      &cbData))
{
       printf("The function succeeded.\n");
}
else
{

   // The second function call failed. Handle the error.
   MyHandleError("The second call to the function failed.");
}

// The function succeeded; the data is now in the buffer
// pointed to by pbData. Note that cbData is
// updated with the actual size of the data returned. Use this size 
// to process bytes of pbData.

// When you have finished using the allocated memory, free it.
free(pbData);

} // End of main

//  This example uses the function MyHandleError, a simple error
//  handling function, to print an error message to the 
//  standard error (stderr) file and exit the program. 
//  For most applications, replace this function with one 
//  that does more extensive error reporting.
void MyHandleError(char *s)
{
    fprintf(stderr,"An error occurred in running the program.\n");
    fprintf(stderr,"%s\n",s);
    fprintf(stderr,"Error number %x.\n",GetLastError());
    fprintf(stderr,"Program terminating.\n");
    exit(1);
}
```



 

 
