---
description: Toutes les fonctions, prototypes, structures et constantes sont définis dans le fichier d’en-tête Winwlx. h.
ms.assetid: 13b5bc92-583d-4031-94f9-f84dbfbf7ee7
title: Génération et test d’une DLL GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e6e4a00f15e6ced4827bbc3efeb3c459f5d6a8
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104321794"
---
# <a name="building-and-testing-a-gina-dll"></a>Génération et test d’une DLL GINA

Toutes les fonctions, prototypes, structures et constantes sont définis dans le fichier d’en-tête Winwlx. h.

> [!Note]  
> Les DLL GINA sont ignorées dans Windows Vista.

 

Pour tester une dll [*Gina*](/windows/desktop/SecGloss/g-gly) , utilisez le Winlogon.exe à partir d’une version vérifiée du système d’exploitation, qui est disponible avec le kit de développement de pilotes (DDK) Microsoft Windows. La version vérifiée de [*Winlogon*](/windows/desktop/SecGloss/w-gly) prend en charge le débogage de Ginas comme suit :

-   Vous pouvez utiliser la syntaxe suivante pour créer une section dans Win.ini pour spécifier les options de débogage Winlogon.

    ``` syntax
    [WinlogonDebug]
    LogFile=C:\Winlogon.log
    DebugFlags=Flag1 [, Flag2 ...]
    ```

    S’il est spécifié, **logfile** doit contenir le nom complet du fichier qui sera utilisé pour enregistrer les informations de débogage. Si le fichier n'existe pas, il est créé.

    Les options **DebugFlags** spécifient les genres d’informations de débogage à écrire dans le fichier journal ou le débogueur. **DebugFlags** peut contenir un ou plusieurs des indicateurs suivants.

    

    | Indicateur de débogage | Description                                                                                                                                                                |
    |----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | CoolSwitch     | La combinaison de touches CTRL + ALT + MAJ + TAB entraîne une interruption de débogage dans Winlogon.                                                                                               |
    | Error          | Erreurs d’impression.                                                                                                                                                              |
    | Init           | Affichez les messages d’initialisation et de progression.                                                                                                                                |
    | Notifier         | Imprimer les messages du package de notification.                                                                                                                                       |
    | SAS            | Imprimer des informations sur les notifications de [*séquence de touches de sécurité*](/windows/desktop/SecGloss/s-gly) (SAS). |
    | State          | Imprimer des messages lorsque Winlogon change d’État.                                                                                                                                |
    | Délai d'expiration        | Imprimer des messages quand une limite de temps est définie ou si une limite de temps est atteinte.                                                                                                        |
    | Trace          | Imprimer les informations de trace détaillées.                                                                                                                                           |
    | Avertir           | Afficher les avertissements.                                                                                                                                                            |

    

     

-   Pour démarrer la version vérifiée de Winlogon dans un débogueur, ajoutez l’entrée suivante au registre :

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows NT
                CurrentVersion
                   Image File Execution Options
                      winlogon.exe
                         Debugger = ntsd -d<dl>
    <dt>

                     Data type
</dt>
    <dd>                     REG_SZ</dd>
    </dl>
    ```

> [!NOTE]
> Vous devez utiliser le débogueur symbolique Windows (NTSD) pour déboguer Winlogon.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Chargement et exécution d’une DLL GINA](loading-and-running-a-gina-dll.md)
</dt> <dt>

[Fonctions d’exportation GINA](authentication-functions.md)
</dt> <dt>

[Structures GINA](authentication-structures.md)
</dt> <dt>

[Fonctions GINA des services Terminal Server](terminal-services-gina-functions.md)
</dt> </dl>

 

 
