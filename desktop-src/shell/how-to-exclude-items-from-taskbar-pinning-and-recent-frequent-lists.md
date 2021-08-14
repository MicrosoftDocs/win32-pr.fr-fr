---
description: les Applications, les processus et les fenêtres peuvent choisir de ne pas être disponibles pour s’épingler à la barre des tâches ou d’être incluses dans la liste la plus fréquemment utilisée (MFU) du menu Démarrer.
title: Comment exclure des éléments de l’épinglage de la barre des tâches et des listes récentes/fréquentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3adb60353836e436f4327837c30448c7628a435048cc2a41b0464d56341f410
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118223563"
---
# <a name="how-to-exclude-items-from-taskbar-pinning-and-recentfrequent-lists"></a>Comment exclure des éléments de l’épinglage de la barre des tâches et des listes récentes/fréquentes

Les applications, les processus et les fenêtres peuvent choisir de ne pas être disponibles pour épingler à la barre des tâches ou d’être incluses dans la liste la plus fréquemment utilisée (MFU) du menu **Démarrer** .

## <a name="instructions"></a>Instructions


Il existe trois mécanismes pour accomplir l’exclusion des éléments de l’épinglage de la barre des tâches et des listes récentes/fréquentes :

-   Ajoutez l’entrée NoStartPage à l’inscription de l’application, comme illustré dans cet exemple :

    ```
    HKEY_CLASSES_ROOT
       Applications
          Example.exe
             NoStartPage
    ```

    Les données associées à l’entrée NoStartPage sont ignorées. Seule la présence de l’entrée est requise. Par conséquent, le type idéal pour NoStartPage est **reg \_ None**.

    Notez que toute utilisation d’un ID de modèle utilisateur d’application explicite (AppUserModelID) remplace l’entrée NoStartPage. Si un AppUserModelID explicite est appliqué à un raccourci, à un processus ou à une fenêtre, il devient regroupement et éligible pour la liste MFU du menu **Démarrer** .

-   Définissez la propriété [System. AppUserModel. PreventPinning](../properties/props-system-appusermodel-preventpinning.md) sur les fenêtres et les raccourcis. Cette propriété doit être définie sur une fenêtre avant que la propriété AppUserModel de la valeur de la propriété de l’ID du groupe de [ \_ \_ sécurité](../properties/props-system-appusermodel-id.md) .
-   Ajoutez une valeur AppUserModelID explicite sous la forme d’une valeur sous la sous-clé de Registre suivante, comme indiqué dans cet exemple :

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      FileAssociation
                         NoStartPageAppUserModelIDs
                            AppUserModelID1
                            AppUserModelID2
                            AppUserModelID3
    ```

    Chaque entrée est une valeur **reg \_ null** avec le nom de AppUserModelID. Toute AppUserModelID trouvée dans cette liste n’est pas regroupement et n’est pas éligible pour l’inclusion dans la liste des listes les plus fréquemment dans le menu **Démarrer** .

## <a name="remarks"></a>Remarques

N’oubliez pas que certains fichiers exécutables, ainsi que les raccourcis contenant certaines chaînes dans leurs noms, sont automatiquement exclus de l’épinglage et de l’inclusion dans la liste des MFU.

> [!Note]  
> Cette exclusion automatique peut être remplacée en appliquant une AppUserModelID explicite.

 

Si l’une des chaînes suivantes, quelle que soit la casse, est incluse dans le nom du raccourci, le programme n’est pas regroupement et n’est pas affiché dans la liste des plus fréquemment utilisés (non applicable à Windows 10) :

-   Documentation
-   Aide
-   Installer
-   En savoir plus
-   Lisez-moi
-   Lire en premier
-   Fichier Lisezmoi
-   Supprimer
-   Installation
-   Assistance
-   Nouveautés

La liste de programmes suivante n’est pas regroupement et est exclue de la liste des plus fréquemment utilisées :

-   Applaunch.exe
-   Control.exe
-   Dfsvc.exe
-   Dllhost.exe
-   Guestmodemsg.exe
-   Hh.exe
-   Install.exe
-   Isuninst.exe
-   Lnkstub.exe
-   Mmc.exe
-   Mshta.exe
-   Msiexec.exe
-   Msoobe.exe
-   Rundll32.exe
-   Setup.exe
-   St5unst.exe
-   Unwise.exe
-   Unwise32.exe
-   Werfault.exe
-   Winhlp32.exe
-   Wlrmdr.exe
-   Wuapp.exe

Les listes précédentes sont stockées dans les valeurs de Registre suivantes.

> [!Note]  
> Ces listes ne doivent pas être modifiées par les applications. Utilisez l’une des méthodes de liste d’exclusion décrites précédemment dans cette rubrique pour la même expérience.

 

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FileAssociation
                     AddRemoveApps
                     HostApps
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[La barre des tâches](taskbar.md)
</dt> <dt>

[Extensions de la barre des tâches](taskbar-extensions.md)
</dt> </dl>

 

 
