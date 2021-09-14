---
title: Détermination de l’emplacement d’un partage
description: L’exemple suivant montre comment appeler la fonction WNetGetUniversalName pour déterminer l’emplacement d’un partage sur un lecteur Redirigé.
ms.assetid: ce57fecb-8b14-4514-a3fd-45d7ef6eee89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c50c0d46e9ac2e520f7be15812b2f541fd3e588f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013167"
---
# <a name="determining-the-location-of-a-share"></a>Détermination de l’emplacement d’un partage

L’exemple suivant montre comment appeler la fonction [**WNetGetUniversalName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetuniversalnamea) pour déterminer l’emplacement d’un partage sur un lecteur Redirigé.

Tout d’abord, l’exemple de code appelle la fonction **WNetGetUniversalName** , en spécifiant le niveau d’information [**Universal \_ name \_ info**](/windows/desktop/api/Winnetwk/ns-winnetwk-universal_name_infoa) pour récupérer un pointeur vers une chaîne de nom UNC (Universal Naming Convention) pour la ressource. L’exemple appelle ensuite **WNetGetUniversalName** une deuxième fois, en spécifiant le niveau d’informations [**Remote \_ name \_ info**](/windows/desktop/api/Winnetwk/ns-winnetwk-remote_name_infoa) pour récupérer deux chaînes d’informations de connexion réseau supplémentaires. Si les appels réussissent, l’exemple imprime l’emplacement du partage.

Pour tester l’exemple de code suivant, procédez comme suit :

1.  Nommez l’exemple de code GetUni. cpp.
2.  Ajoutez l’exemple à une application console appelée GetUni.
3.  Liez les bibliothèques shell32. lib, MPR. lib et NetApi32. lib à la liste des bibliothèques du compilateur.
4.  À partir de l’invite de commandes, accédez au répertoire GetUni.
5.  Compilez GetUni. cpp.
6.  Exécutez le fichier GetUni.exe suivi d’une lettre de lecteur et du signe deux-points, comme suit :

    **GetUni H :\\**


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



 

 