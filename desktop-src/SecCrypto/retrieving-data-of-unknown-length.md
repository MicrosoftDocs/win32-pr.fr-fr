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
# <a name="retrieving-data-of-unknown-length"></a><span data-ttu-id="e96da-103">Récupération de données de longueur inconnue</span><span class="sxs-lookup"><span data-stu-id="e96da-103">Retrieving Data of Unknown Length</span></span>

<span data-ttu-id="e96da-104">De nombreuses fonctions renvoient un nombre potentiellement important de données à une adresse fournie comme l’un des paramètres par l’application.</span><span class="sxs-lookup"><span data-stu-id="e96da-104">Many functions return a potentially large amount of data to an address provided as one of the parameters by the application.</span></span> <span data-ttu-id="e96da-105">Dans tous ces cas, l’opération est effectuée de façon similaire, si elle n’est pas identique.</span><span class="sxs-lookup"><span data-stu-id="e96da-105">In all these cases, the operation is performed in a similar, if not identical, fashion.</span></span> <span data-ttu-id="e96da-106">Le paramètre qui pointe vers l’emplacement des données retournées utilise la Convention de notation où PB ou PV sont les deux premiers caractères du nom de paramètre.</span><span class="sxs-lookup"><span data-stu-id="e96da-106">The parameter that points to the location of the returned data will use the notation convention where pb or pv are the first two characters of the parameter name.</span></span> <span data-ttu-id="e96da-107">PCB est un autre paramètre dont le nom du paramètre contient les trois premiers caractères.</span><span class="sxs-lookup"><span data-stu-id="e96da-107">Another parameter will have pcb as the first three characters of the parameter name.</span></span> <span data-ttu-id="e96da-108">Ce paramètre représente la taille, en octets, des données qui seront retournées à l’emplacement PB ou PV.</span><span class="sxs-lookup"><span data-stu-id="e96da-108">This parameter represents the size, in bytes, of the data that will be returned to the pb or pv location.</span></span> <span data-ttu-id="e96da-109">Par exemple, considérez la spécification de fonction suivante :</span><span class="sxs-lookup"><span data-stu-id="e96da-109">For example, consider the following function specification:</span></span>

``` syntax
#include <windows.h>

BOOL WINAPI SomeFunction(
  PCCRL_CONTEXT pCrlContext,  // in
  DWORD dwPropId,             // in
  BYTE *pbData,               // out
  DWORD *pcbData              // in/out
);
```

<span data-ttu-id="e96da-110">Dans cet exemple, *pbData* est un pointeur vers l’emplacement où les données seront retournées, et *pcbData* est la taille, en octets, des données retournées.</span><span class="sxs-lookup"><span data-stu-id="e96da-110">In this example, *pbData* is a pointer to the location where the data will be returned, and *pcbData* is the size, in bytes, of the returned data.</span></span>

> [!Note]  
> <span data-ttu-id="e96da-111">Le paramètre Companion du paramètre PCB peut parfois comporter un préfixe légèrement différent, tel que p ou PV.</span><span class="sxs-lookup"><span data-stu-id="e96da-111">The companion parameter to the pcb parameter may sometimes carry a slightly different prefix, such as p or pv.</span></span> <span data-ttu-id="e96da-112">En outre, pour les paramètres auxiliaires utilisant la combinaison de préfixes PWSZ et PCCh, le paramètre PCCh est le nombre, en caractères ([*Unicode*](../secgloss/u-gly.md) ou [*ASCII*](../secgloss/a-gly.md), le cas échéant), des données retournées.</span><span class="sxs-lookup"><span data-stu-id="e96da-112">Also, for companion parameters using the combination of prefixes pwsz and pcch, the pcch parameter is the count, in characters ([*Unicode*](../secgloss/u-gly.md) or [*ASCII*](../secgloss/a-gly.md), as applicable), of the returned data.</span></span>

 

<span data-ttu-id="e96da-113">Si la mémoire tampon spécifiée par le paramètre *pbData* n’est pas assez grande pour contenir les données retournées, la fonction définit le code d’erreur \_ plus de \_ données (qui peut être vu en appelant la fonction [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) ) et stocke la taille de mémoire tampon requise, en octets, dans la variable vers laquelle pointe *pcbData*.</span><span class="sxs-lookup"><span data-stu-id="e96da-113">If the buffer specified by the *pbData* parameter is not large enough to hold the returned data, the function sets the ERROR\_MORE\_DATA code (which can be seen by calling the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function) and stores the required buffer size, in bytes, in the variable pointed to by *pcbData*.</span></span>

<span data-ttu-id="e96da-114">Si **null** est entrée pour *pbData* et *pcbData* n’est pas **null**, aucune erreur n’est retournée et la fonction retourne la taille, en octets, de la mémoire tampon nécessaire dans la variable vers laquelle pointe *pcbData*.</span><span class="sxs-lookup"><span data-stu-id="e96da-114">If **NULL** is input for *pbData* and *pcbData* is not **NULL**, no error is returned, and the function returns the size, in bytes, of the needed memory buffer in the variable pointed to by *pcbData*.</span></span> <span data-ttu-id="e96da-115">Cela permet à une application de déterminer la taille de, et la meilleure façon d’allouer, une mémoire tampon pour les données retournées.</span><span class="sxs-lookup"><span data-stu-id="e96da-115">This lets an application determine the size of, and the best way to allocate, a buffer for the returned data.</span></span>

> [!Note]  
> <span data-ttu-id="e96da-116">Lorsque la **valeur null** est entrée pour *pbData* afin de déterminer la taille nécessaire pour s’assurer que les données retournées tiennent dans la mémoire tampon spécifiée, le deuxième appel à la fonction qui remplit la mémoire tampon avec les données souhaitées peut ne pas utiliser la mémoire tampon entière.</span><span class="sxs-lookup"><span data-stu-id="e96da-116">When **NULL** is input for *pbData* to determine the size needed to ensure that the returned data fits in the specified buffer, the second call to the function which populates the buffer with the desired data may not use the whole buffer.</span></span> <span data-ttu-id="e96da-117">Après le deuxième appel, la taille réelle des données retournées est contenue dans *pcbData*.</span><span class="sxs-lookup"><span data-stu-id="e96da-117">After the second call, the actual size of the data returned is contained in *pcbData*.</span></span> <span data-ttu-id="e96da-118">Utilisez cette taille lors du traitement des données.</span><span class="sxs-lookup"><span data-stu-id="e96da-118">Use this size when processing the data.</span></span>

 

<span data-ttu-id="e96da-119">L’exemple suivant montre comment les paramètres d’entrée et de sortie peuvent être implémentés à cet effet.</span><span class="sxs-lookup"><span data-stu-id="e96da-119">The following example shows how input and output parameters might be implemented for this purpose.</span></span>


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



 

 
