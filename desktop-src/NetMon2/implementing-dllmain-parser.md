---
description: Moniteur réseau utilise la fonction d’exportation DllMain pour identifier l’existence de l’analyseur et libère les ressources que Moniteur réseau utilise pour stocker des informations sur l’analyseur.
ms.assetid: 1741a12c-3645-4e83-b97f-37e67218c5eb
title: Implémentation de l’analyseur DllMain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55dd1ab7432920ac7496643c7c6f9aa0692daf56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750052"
---
# <a name="implementing-dllmain-parser"></a>Implémentation de l’analyseur DllMain

Moniteur réseau utilise la fonction d’exportation **DllMain** pour identifier l’existence de l’analyseur et libère les ressources que Moniteur réseau utilise pour stocker des informations sur l’analyseur.

Lorsque Moniteur réseau appelle **DllMain** pour la première fois, la dll de l’analyseur appelle [**CreateProtocol**](createprotocol.md) pour effectuer les opérations suivantes :

-   Spécifiez le protocole détecté par l’analyseur.
-   Fournissez des points d’entrée pour les autres fonctions d’exportation de l’analyseur qui Moniteur réseaunt les appels.

Lorsque Moniteur réseau appelle **DllMain** pour la dernière fois, **DllMain** appelle [**DestroyProtocol**](destroyprotocol.md) pour libérer toutes les ressources que Moniteur réseau utilise pour stocker des informations sur l’analyseur.

La procédure suivante identifie les étapes nécessaires à l’implémentation de **DllMain**.

**Pour implémenter DllMain**

1.  Spécifiez la structure [**ENTRYPOINTS**](entrypoints.md) pour la fonction [**CreateProtocol**](createprotocol.md) et la variable d’attachement globale. La variable d’attachement est utilisée pour effectuer le suivi du nombre d’instances de protocole en cours d’exécution.
2.  Examinez la valeur du paramètre de *commande* défini par le système d’exploitation.

    Si le paramètre de *commande* est défini sur dll \_ process \_ Attach et Attach a la valeur 0, appelez [**CreateProtocol**](createprotocol.md) pour fournir le nom de protocole et les points d’entrée pour les fonctions d’exportation suivantes.

    -   **S’inscrire**
    -   **Désinscrire**
    -   **RecognizeFrame**
    -   **AttachProperties**
    -   **FormatProperties** (requis uniquement si Moniteur réseau affichera les propriétés de protocole).

    Si le paramètre de *commande* est défini sur \_ détacher le processus de la dll \_ et que Attach a la valeur 0, appelez [**DestroyProtocol**](destroyprotocol.md) à l’aide du handle d’instance retourné par [**CreateProtocol**](createprotocol.md) .

3.  Retourne la **valeur true** , car la fonction de l’analyseur **DllMain** doit toujours retourner la **valeur true**.

Voici une implémentation de base de **DllMain**. L’exemple de code utilise une instruction case pour intercepter les valeurs du paramètre *Command* afin de déterminer si [**CreateProtocol**](createprotocol.md) ou [**DestroyProtocol**](destroyprotocol.md) doit être appelé.

``` syntax
#include <windows.h>

// Entry point structure for parser export functions and global
// Attach variable.
ENTRYPOINTS EntryPoints =
{
  Register,
  Deregister,
  RecognizeFrame,
  AttachProperties,
  FormatProperties
};

DWORD Attached = 0; 

BOOL WINAPI DllMain(HANDLE hInstance, ULONG Command, LPVOID Reserved)
{
  switch(Command)
  {
  // Call CreateProtocol.
  case DLL_PROCESS_ATTACH:
       // Loading parser DLL.
       if(Attached == 0)
       {
         hProtocol = CreateProtocol( "ProtocolName",
                                     &EntryPoints,
                                     ENTRYPOINTS_SIZE);
       }
       Attached++;
       break;
  // Call DestroyProtocol.
  case DLL_PROCESS_DETACH:
       // Unloading parser DLL.
       Attached--;
       if(Attached == 0)
       {
         DestroyProtocol( hProtocol);
       }
       break;
  }
  return TRUE;
}
```

 

 



