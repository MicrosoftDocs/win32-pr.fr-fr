---
description: Les éléments du panneau de configuration qui sont implémentés dans une DLL qui exporte la fonction CPlApplet ont des exigences d’inscription différentes de .exe fichiers.
title: Comment inscrire les éléments du panneau de configuration de la DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b25fffb3b06f93640c5ca8623fb24ffb53c6fd3ecae0b9e23cabafacdceba8f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593189"
---
# <a name="how-to-register-dll-control-panel-items"></a>Comment inscrire les éléments du panneau de configuration de la DLL

> [!Note]  
> Les instructions d’implémentation actuelles stipulent que les nouveaux éléments du panneau de configuration doivent être implémentés en tant que fichiers .exe plutôt qu’en tant que fichiers .cpl. Les informations suivantes sont incluses principalement pour des raisons d’héritage.

 

Les éléments du panneau de configuration qui sont implémentés dans une DLL qui exporte la fonction [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) ont des exigences d’inscription différentes de .exe fichiers. à partir de Windows XP, les dll des éléments du panneau de configuration doivent être installées dans le dossier de l’application associée sous le dossier Program Files. Les éléments stockés dans le répertoire system32 avec une extension de .cpl n’ont pas besoin d’être inscrits ; ils s’affichent automatiquement dans le panneau de configuration. Tous les autres éléments du panneau de configuration qui utilisent **CPlApplet** doivent être inscrits de l’une des deux manières suivantes :

-   si l’élément du panneau de configuration doit être mis à la disposition de tous les utilisateurs, enregistrez le chemin d’accès en fonction de l’ordinateur en ajoutant une valeur de **REG \_ EXPAND \_ SZ** à la clé **HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Control Panel** de la \\ sous-clé **Cpls** , définie sur le chemin d’accès de la DLL.
-   Si l’élément du panneau de configuration doit être disponible pour chaque utilisateur, utilisez **HKEY \_ Current \_ User** comme clé racine au lieu de **HKEY \_ local \_ machine**.

Les deux exemples suivants inscrivent l’élément du panneau de configuration *MyCplApp* . La DLL est nommée MyCpl.cpl et se trouve dans le répertoire de l’application *champ MyCorp \\ MonApp* . Ce premier exemple illustre l’inscription par ordinateur.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Étape 1 :

Ajoutez ces informations au registre pour enregistrer l’existence du fichier .cpl.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Cpls
                     MyCpl = [REG_EXPAND_SZ] %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl
```

### <a name="step-2"></a>Étape 2 :

**Windows Vista et versions ultérieures :** Ajoutez ces informations supplémentaires au registre pour fournir un GUID pour l’élément du panneau de configuration.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.Software.AppId
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = {A newly generated GUID}
```

En générant un GUID pour identifier de manière unique l’élément du panneau de configuration, vous pouvez ajouter des liens de tâches au panneau de configuration. Sans ce GUID, les liens de tâche ne sont pas associés à l’élément du panneau de configuration. Consultez [création de liens de tâches pouvant faire l’objet d’une recherche pour un élément du panneau de configuration](creating-searchable-task-links.md).

### <a name="step-3"></a>Étape 3 :

**Windows Vista et versions ultérieures :** Ajoutez les informations suivantes au registre pour créer un nom canonique pour l’élément.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.ApplicationName
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_SZ] MyCorporation.MyCpl
```

En ajoutant un nom canonique, les utilisateurs peuvent lancer l’élément du panneau de configuration à partir d’une ligne de commande en entrant `control.exe /name MyCorporation.MyCpl` . Cela permet également de modifier ultérieurement une implémentation d’un fichier .cpl dans un fichier .exe, sans exiger que les programmes d’appel apportent des modifications, car ils peuvent continuer à ouvrir l’élément via son nom canonique. Pour plus d’informations sur les noms canoniques, consultez [exécution des éléments du panneau de configuration](executing-control-panel-items.md).

### <a name="step-4"></a>Étape 4 :

**Windows Vista et versions ultérieures :** Ajoutez les informations suivantes au registre pour assigner un élément du panneau de configuration à une ou plusieurs catégories.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.ControlPanel.Category
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_DWORD] 3
```

**Windows XP :** Ajoutez les informations suivantes au registre pour assigner un élément du panneau de configuration à une ou plusieurs catégories.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     {305CA226-D286-468e-B848-2B2E8E697B74} 2
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_DWORD] 3
```

Cet exemple affecte l’élément à la catégorie 3, qui correspond à réseau et Internet. Pour ajouter un élément à plusieurs catégories, fournissez la liste sous la forme d’une valeur de REG \_ SZ séparée par des virgules, par exemple « 3, 8 ». Les valeurs peuvent être fournies sous la forme d’une valeur décimale ou hexadécimale. notez que la possibilité d’ajouter un élément à plusieurs catégories n’est possible que dans Windows XP Service Pack 2 (SP2) et versions ultérieures. Consultez [assignation de catégories du panneau de configuration](assigning-control-panel-categories.md) pour toutes les valeurs possibles.

### <a name="step-5"></a>Étape 5 :

**Windows Vista et versions ultérieures :** Ajoutez les informations suivantes au registre pour créer et pointer vers un fichier XML pour contenir des liens de tâches pour l’élément. La valeur doit être un \_ chemin d’accès reg SZ comme indiqué ici ou un module et un ID de ressource (par exemple, « C : \\ Program Files \\ champ MyCorp \\ MyApp \\MyApp.exe,-31 ») s’il s’agit d’une ressource incorporée. L’emplacement du fichier XML doit être entièrement spécifié. Elle ne peut pas utiliser une variable d’environnement telle que% ProgramFiles%.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.Software.TasksFileUrl
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_SZ] C:\ProgramFiles\MyCorp\MyApp\MyTasks.xml
```

Pour plus d’informations sur les liens de tâches et sur la façon de créer le fichier XML pour les stocker, consultez [création de liens de tâches pouvant faire l’objet d’une recherche pour un élément du panneau de configuration](creating-searchable-task-links.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Inscription des éléments du panneau de configuration](registering-control-panel-items.md)
</dt> <dt>

[Comment inscrire des éléments du panneau de configuration exécutables](how-to-register-an-executable-control-panel-item-registration-.md)
</dt> </dl>

 

 
