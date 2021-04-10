---
title: Détermination de l’emplacement d’un partage
description: L’exemple suivant montre comment appeler la fonction WNetGetUniversalName pour déterminer l’emplacement d’un partage sur un lecteur Redirigé.
ms.assetid: ce57fecb-8b14-4514-a3fd-45d7ef6eee89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c50c0d46e9ac2e520f7be15812b2f541fd3e588f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941197"
---
# <a name="determining-the-location-of-a-share"></a><span data-ttu-id="090c6-103">Détermination de l’emplacement d’un partage</span><span class="sxs-lookup"><span data-stu-id="090c6-103">Determining the Location of a Share</span></span>

<span data-ttu-id="090c6-104">L’exemple suivant montre comment appeler la fonction [**WNetGetUniversalName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetuniversalnamea) pour déterminer l’emplacement d’un partage sur un lecteur Redirigé.</span><span class="sxs-lookup"><span data-stu-id="090c6-104">The following example demonstrates how to call the [**WNetGetUniversalName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetuniversalnamea) function to determine the location of a share on a redirected drive.</span></span>

<span data-ttu-id="090c6-105">Tout d’abord, l’exemple de code appelle la fonction **WNetGetUniversalName** , en spécifiant le niveau d’information [**Universal \_ name \_ info**](/windows/desktop/api/Winnetwk/ns-winnetwk-universal_name_infoa) pour récupérer un pointeur vers une chaîne de nom UNC (Universal Naming Convention) pour la ressource.</span><span class="sxs-lookup"><span data-stu-id="090c6-105">First the code sample calls the **WNetGetUniversalName** function, specifying the [**UNIVERSAL\_NAME\_INFO**](/windows/desktop/api/Winnetwk/ns-winnetwk-universal_name_infoa) information level to retrieve a pointer to a Universal Naming Convention (UNC) name string for the resource.</span></span> <span data-ttu-id="090c6-106">L’exemple appelle ensuite **WNetGetUniversalName** une deuxième fois, en spécifiant le niveau d’informations [**Remote \_ name \_ info**](/windows/desktop/api/Winnetwk/ns-winnetwk-remote_name_infoa) pour récupérer deux chaînes d’informations de connexion réseau supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="090c6-106">Then the sample calls **WNetGetUniversalName** a second time, specifying the [**REMOTE\_NAME\_INFO**](/windows/desktop/api/Winnetwk/ns-winnetwk-remote_name_infoa) information level to retrieve two additional network connection information strings.</span></span> <span data-ttu-id="090c6-107">Si les appels réussissent, l’exemple imprime l’emplacement du partage.</span><span class="sxs-lookup"><span data-stu-id="090c6-107">If the calls are successful, the sample prints the location of the share.</span></span>

<span data-ttu-id="090c6-108">Pour tester l’exemple de code suivant, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="090c6-108">To test the following code sample, perform the following steps:</span></span>

1.  <span data-ttu-id="090c6-109">Nommez l’exemple de code GetUni. cpp.</span><span class="sxs-lookup"><span data-stu-id="090c6-109">Name the code sample GetUni.cpp.</span></span>
2.  <span data-ttu-id="090c6-110">Ajoutez l’exemple à une application console appelée GetUni.</span><span class="sxs-lookup"><span data-stu-id="090c6-110">Add the sample to a console application called GetUni.</span></span>
3.  <span data-ttu-id="090c6-111">Liez les bibliothèques shell32. lib, MPR. lib et NetApi32. lib à la liste des bibliothèques du compilateur.</span><span class="sxs-lookup"><span data-stu-id="090c6-111">Link the libraries Shell32.lib, Mpr.lib, and NetApi32.lib to the compiler list of libraries.</span></span>
4.  <span data-ttu-id="090c6-112">À partir de l’invite de commandes, accédez au répertoire GetUni.</span><span class="sxs-lookup"><span data-stu-id="090c6-112">From the command prompt, change to the GetUni directory.</span></span>
5.  <span data-ttu-id="090c6-113">Compilez GetUni. cpp.</span><span class="sxs-lookup"><span data-stu-id="090c6-113">Compile GetUni.cpp.</span></span>
6.  <span data-ttu-id="090c6-114">Exécutez le fichier GetUni.exe suivi d’une lettre de lecteur et du signe deux-points, comme suit :</span><span class="sxs-lookup"><span data-stu-id="090c6-114">Run the file GetUni.exe followed by a drive letter and colon, like this:</span></span>

    <span data-ttu-id="090c6-115">**GetUni H :\\**</span><span class="sxs-lookup"><span data-stu-id="090c6-115">**GetUni H:\\**</span></span>


```C++
#define  STRICT
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

#pragma comment(lib, "mpr.lib")

#define BUFFSIZE = 1000

void main( int argc, char *argv[] )
{
  DWORD cbBuff = 1000;    // Size of Buffer
  TCHAR szBuff[1000];    // Buffer to receive information
  REMOTE_NAME_INFO  * prni = (REMOTE_NAME_INFO *)   &szBuff;
  UNIVERSAL_NAME_INFO * puni = (UNIVERSAL_NAME_INFO *) &szBuff;
  DWORD res;

  if((argc < 2) | (lstrcmp(argv[1], "/?") == 0))
  {
    printf("Syntax:  GetUni DrivePathAndFilename\n"
         "Example: GetUni U:\\WINNT\\SYSTEM32\\WSOCK32.DLL\n");
    return;
  }
  
  // Call WNetGetUniversalName with the UNIVERSAL_NAME_INFO_LEVEL option
  //
  printf("Call WNetGetUniversalName using UNIVERSAL_NAME_INFO_LEVEL.\n");
  if((res = WNetGetUniversalName((LPTSTR)argv[1],
         UNIVERSAL_NAME_INFO_LEVEL, // The structure is written to this block of memory. 
         (LPVOID) &szBuff, 
         &cbBuff)) != NO_ERROR) 
    //
    // If the call fails, print the error; otherwise, print the location of the share, 
    //  using the pointer to UNIVERSAL_NAME_INFO_LEVEL.
    //
    printf("Error: %ld\n\n", res); 
   
  else
    _tprintf(TEXT("Universal Name: \t%s\n\n"), puni->lpUniversalName); 
    
  //
  // Call WNetGetUniversalName with the REMOTE_NAME_INFO_LEVEL option
  //
  printf("Call WNetGetUniversalName using REMOTE_NAME_INFO_LEVEL.\n");
  if((res = WNetGetUniversalName((LPTSTR)argv[1], 
         REMOTE_NAME_INFO_LEVEL, 
         (LPVOID) &szBuff,    //Structure is written to this block of memory
         &cbBuff)) != NO_ERROR) 
    //
    // If the call fails, print the error; otherwise, print
    //  the location of the share, using 
    //  the pointer to REMOTE_NAME_INFO_LEVEL.
    //
    printf("Error: %ld\n", res); 
  else
    _tprintf(TEXT("Universal Name: \t%s\nConnection Name:\t%s\nRemaining Path: \t%s\n"),
          prni->lpUniversalName, 
          prni->lpConnectionName, 
          prni->lpRemainingPath);
  return;
}
```



 

 