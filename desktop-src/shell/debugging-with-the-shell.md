---
description: Cette rubrique explique comment déboguer des dll d’extension de Shell et d’espace de noms.
title: Débogage avec l’interpréteur de commandes
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2fcaf633-9a6d-4fda-a690-28445b10a6d6
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 276023e5628ab7390398fd7bd367be32e45c13825fcf96625104be1ded8735de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032827"
---
# <a name="debugging-with-the-shell"></a>Débogage avec l’interpréteur de commandes

Cette rubrique explique comment déboguer des dll d’extension de Shell et d’espace de noms.

-   [Exécution de l’interpréteur de commandes sous un débogueur](#running-the-shell-under-a-debugger)
-   [Exécution et test des extensions de Shell](#running-and-testing-shell-extensions)
-   [Déchargement de la DLL](#unloading-the-dll)

## <a name="running-the-shell-under-a-debugger"></a>Exécution de l’interpréteur de commandes sous un débogueur

Pour déboguer votre extension, vous devez exécuter le shell à partir du débogueur. Procédez comme suit :

1.  Chargez le projet de l’extension dans le débogueur, mais ne l’exécutez pas.
2.  Arrêtez l’interpréteur de commandes.

    -   pour Windows Vista et versions ultérieures :
        1.  Affichez le menu **Démarrer** .
        2.  Appuyez sur CTRL + MAJ et cliquez avec le bouton droit sur l’arrière-plan de la moitié droite du menu **Démarrer** .
        3.  Dans le menu qui s’affiche, choisissez **quitter l’Explorateur**.
    -   pour Windows XP :
        1.  Dans le menu **Démarrer** , choisissez **arrêter**.
        2.  appuyez sur CTRL + ALT + maj, puis cliquez sur **non** dans la boîte de dialogue **arrêter l’Windows** .

    L’interpréteur de commandes est maintenant arrêté, mais toutes les autres applications sont toujours en cours d’exécution, y compris le débogueur.

3.  définissez le débogueur pour exécuter la DLL d’extension avec Explorer.exe à partir du répertoire **Windows** .
4.  Exécutez le projet à partir du débogueur. L’interpréteur de commandes est lancé comme d’habitude, mais le débogueur est attaché au processus de l’interpréteur de commandes.

## <a name="running-and-testing-shell-extensions"></a>Exécution et test des extensions de Shell

vous pouvez exécuter et tester vos extensions dans un processus distinct de l’explorateur de Windows pour éviter d’arrêter et de redémarrer le bureau et la barre des tâches. Votre bureau et votre barre des tâches peuvent toujours être utilisés pendant l’exécution et le test des extensions.

Pour activer cette fonctionnalité, ajoutez l' \_ entrée de Registre DWORD suivante au registre.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  DesktopProcess = 1
```

Pour que cette entrée prenne effet, vous devez vous déconnecter et vous reconnecter. Ce paramètre entraîne la création des fenêtres de bureau et de la barre des tâches dans un processus de Explorer.exe et toutes les autres fenêtres Explorateur et dossier à ouvrir dans un processus de Explorer.exe différent.

En plus de rendre plus pratique l’exécution et le test de vos extensions, ce paramètre rend également le bureau plus robuste en ce qui concerne les extensions d’environnement. De nombreuses extensions de ce type (extensions de menu contextuel, par exemple) sont chargées dans le processus de Explorer.exe non Desktop. Si ce processus se termine, le bureau et la barre des tâches ne seront pas affectés, et la fenêtre de l’Explorateur ou du dossier suivant recréera le processus terminé.

## <a name="unloading-the-dll"></a>Déchargement de la DLL

L’interpréteur de commandes décharge automatiquement toute DLL lorsque son nombre d’utilisations est égal à zéro, mais uniquement après que la DLL n’a pas été utilisée pendant une période donnée. Cette période inactive peut être inutilement longue, en particulier lors du débogage d’une DLL d’extension de Shell. Vous pouvez raccourcir la période inactive en ajoutant les informations suivantes au registre.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AlwaysUnloadDll
```

 

 



