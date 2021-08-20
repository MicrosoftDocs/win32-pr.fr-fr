---
description: Windows la Protection des ressources (WRP) empêche le remplacement des fichiers système essentiels, des dossiers et des clés de registre installés dans le cadre de Windows Vista ou Windows Server 2008.
ms.assetid: 1cb67b4a-dc75-4bd7-b314-d695c10d5558
title: Détection du remplacement des ressources
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e452b9fba0a8002e13d7fc309ff3c8a12ec114a6a33b1bd7d8d253d710ffa77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053215"
---
# <a name="detecting-resource-replacement"></a>Détection du remplacement des ressources

Windows la Protection des ressources (WRP) empêche le remplacement des fichiers système essentiels, des dossiers et des clés de registre installés dans le cadre de Windows Vista ou Windows Server 2008.

WRP protège les fichiers, dossiers et clés de registre sur Windows Vista ou Windows Server 2008 en détectant et en empêchant les tentatives de remplacement des ressources protégées. cette protection est basée sur une Windows liste de contrôle d’accès discrétionnaire (DACL) et des listes de contrôle d’accès (ACL) définies pour les ressources protégées. L’autorisation d’accès complet pour modifier les ressources protégées par WRP est limitée à TrustedInstaller. les ressources protégées par WRP ne peuvent être modifiées qu’à l’aide des [mécanismes de remplacement des ressources pris en charge](supported-file-replacement-mechanisms.md) par le service d’installation des Modules Windows. Les applications tentant de modifier une ressource protégée par WRP ne changent jamais la ressource et peuvent recevoir un message d’erreur indiquant que l’accès à la ressource a été refusé.

Les applications et les programmes d’installation peuvent utiliser les fonctions [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) et [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) pour déterminer si un fichier ou une clé de Registre est protégé.

* * Windows Server 2003 et Windows XP : * *

Windows La protection des fichiers (WFP) protège les fichiers système en détectant les tentatives de remplacement des fichiers système protégés. Cette protection est déclenchée lorsque WFP reçoit une notification de modification de répertoire pour un fichier dans un répertoire protégé. Lorsque WFP reçoit cette notification, il détermine quel fichier a changé. Si le fichier est protégé, WFP recherche la signature de fichier dans un fichier catalogue pour déterminer si le nouveau fichier est la version correcte. Si la version du fichier n’est pas correcte, le système remplace le fichier par la version appropriée à partir du média de distribution ou du cache, selon que le fichier se trouve dans le cache ou non. La plateforme WFP recherche le fichier approprié dans l’ordre suivant :

1.  Recherchez dans le répertoire du cache.
2.  Recherchez le chemin d’installation réseau si le système a été installé à l’aide de l’installation réseau.
3.  recherchez sur un cd-rom Windows, si le système a été installé à partir d’un cd-rom.

Si la protection de code à distance ne peut pas trouver automatiquement le fichier aux deux premiers emplacements, le message suivant s’affiche :

![message WFP affiché lorsqu’un fichier est introuvable dans le répertoire du cache ou le chemin d’installation réseau](images/wfp-1.png)

Si le système a été installé à l’aide d’un CD-ROM, WFP affiche le message suivant :

![message WFP affiché pour inviter l’utilisateur à insérer un CD-ROM Windows](images/wfp-2.png)

Si un administrateur n’est pas connecté, WFP ne peut pas afficher l’une de ces boîtes de dialogue. WFP affiche la boîte de dialogue lorsqu’un administrateur ouvre une session.

La protection des fichiers journaux enregistre également la tentative de remplacement de fichier dans le journal des événements système. Si l’administrateur a annulé la restauration du fichier approprié, WFP journalise l’annulation.

## <a name="retrieving-the-list-of-protected-files"></a>Récupération de la liste des fichiers protégés

L’exemple suivant montre comment les applications et les programmes d’installation peuvent utiliser la fonction [**SfcGetNextProtectedFile**](/windows/desktop/api/Sfc/nf-sfc-sfcgetnextprotectedfile) pour obtenir la liste complète des fichiers protégés.


```C++
#include <windows.h>
#include <sfc.h>
#include <stdio.h>

#pragma comment(lib, "sfc")

void wmain (int argc, WCHAR ** argv)
{  UNREFERENCED_PARAMETER(argc);    
   PROTECTED_FILE_DATA pfd = {0};
   BOOL fResult;

   wprintf (L"List of protected files:\n\n", argv[1]);

   while (FALSE != (fResult = SfcGetNextProtectedFile (NULL, &pfd)))
   {
      wprintf (L"   %lu   %s\n", pfd.FileNumber, pfd.FileName);
   }

   if (GetLastError() == ERROR_NO_MORE_FILES)
   {
      wprintf (L"\nAll %lu protected files listed\n", pfd.FileNumber);
   }
   else
   {
      wprintf (L"\nerror %lu: SfcGetNextProtectedFile() failed unexpectedly\n", GetLastError());
   }

}
```



 

 



