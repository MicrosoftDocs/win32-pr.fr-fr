---
description: L’intégralité du test et du débogage de vos implémentations de gestionnaires de protocole consiste à comprendre comment les gestionnaires de protocole sont lancés.
ms.assetid: 33c99620-7381-4719-9fc6-4c8284481411
title: Débogage de gestionnaires de protocole
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 321d59c0c7915f9bbf84a80091408ba88a9a75ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112399"
---
# <a name="debugging-protocol-handlers"></a>Débogage de gestionnaires de protocole

L’intégralité du test et du débogage de vos implémentations de gestionnaires de protocole consiste à comprendre comment les gestionnaires de protocole sont lancés.

Cette rubrique est organisée comme suit :

-   [À propos du débogage des gestionnaires de protocole](#about-debugging-protocol-handlers)
-   [Configuration du débogage](#setting-up-debugging)
-   [Ressources supplémentaires](#additional-resources)
-   [Rubriques connexes](#related-topics)

## <a name="about-debugging-protocol-handlers"></a>À propos du débogage des gestionnaires de protocole

Le processus SearchIndexer (searchindexer.exe) lance une copie du processus SearchProtocolHost (SearchProtocolHost.exe) dans le contexte système et une autre copie dans le contexte de l’utilisateur. Ensuite, les gestionnaires de protocole sont chargés dans le processus SearchProtocolHost en fonction des besoins. Ils ne sont pas déchargés tant que le service de recherche n’est pas arrêté. La même instance d’un gestionnaire de protocole est réutilisée autant de fois que le service est en cours d’exécution.

Les processus SearchIndexer et SearchProtocolHost communiquent fréquemment pendant l’indexation. Si vous suspendez ou arrêtez le processus SearchProtocolHost à déboguer, le SearchIndexer lance un nouveau processus SearchProtocolHost, invalidant la session de débogage. En outre, si vous attachez directement votre débogueur au processus SearchProtocolHost, vous pouvez rompre l’héritage handle-héritage à partir de searchindexer.exe à searchprotocolhost.exe, et les deux processus ne pourront pas communiquer.

Pour éviter ces problèmes, vous devez notifier le service de recherche que vous déboguez, et vous devez attacher le débogueur au processus SearchIndexer avec des instructions pour déboguer les processus enfants, comme décrit ci-dessous.

## <a name="setting-up-debugging"></a>Configuration du débogage

Procédez comme suit pour configurer le débogage de votre gestionnaire de protocole.

1.  Informez le service de recherche que vous déboguez en affectant la valeur 1 à la valeur DebugFilters dans le registre :

    ```
    HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft
       Windows Search
          Gathering Manager
             DebugFilters = 1
    ```

2.  Attachez un débogueur à l’aide de la clé de registre des options d’exécution du fichier image :

    ```
    HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion
       Image File Execution Options
          SearchIndexer.exe
             Debugger = <path to debugger> <debugger options> 
    ```

    Les options d’un débogueur d’exemple sont décrites dans le tableau suivant.

    

    **Exemple utilisant le** débogueur ntsd Debugger *= C : \\ débogueurs \\ntsd.exe-odGx-C : "sXe LD mydll.dll ; g"*   <br/>

3.  Redémarrez searchindexer.exe sous le débogueur en utilisant compmgmt. msc, services. msc ou une fenêtre de commande avec des commandes semblables à ce qui suit :
    ```
    net stop wsearch
    <copy new DLLs for debugging>
    net start wsearch
            
    ```

    

Pour faire la distinction entre un processus SearchProtocolHost en cours d’exécution dans le contexte système et un processus en cours d’exécution dans le contexte de l’utilisateur, vous pouvez passer en revue les chaînes d’environnement. Par exemple, avec ntsd.exe, vous pouvez utiliser la commande d’extension **! PEB** pour afficher une vue mise en forme des informations contenues dans le bloc Process Environment (PEB).

## <a name="additional-resources"></a>Ressources supplémentaires

-   Pour plus d’informations sur la création de gestionnaires, consultez [inscription d’extensions de Shell](../shell/reg-shell-exts.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> Développement <dt>**conceptuel**</dt> de <dt><a href="-search-3x-wds-phaddins.md">gestionnaires de protocoles</a></dt> <dt><a href="-search-3x-wds-extidx-prot-implementing.md">Présentation des gestionnaires de protocole</a></dt> <dt><a href="-search-3x-wds-notifyingofchanges.md">notification de l’index des modifications</a></dt> <dt><a href="-search-3x-wds-ph-ui-extensions.md">Ajout d’icônes et de menus contextuels</a></dt> <dt><a href="-search-3x-wds-ph-ui-samplecode.md">exemple de code : extensions de Shell pour les gestionnaires de protocole</a></dt> <dt><a href="-search-3x-wds-ph-search-connector.md">création d’un connecteur de recherche pour un gestionnaire de protocole</a></dt> <dt><a href="-search-3x-wds-ph-install-registration.md">installation et inscription de gestionnaires de protocole</a></dt> </dl>

 

 
