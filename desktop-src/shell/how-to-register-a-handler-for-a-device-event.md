---
description: Décrit les processus d’implémentation de gestionnaires d’événements d’appareil dans le registre.
ms.assetid: 84B12B5C-C179-4124-A1FC-B90D120336BF
title: Comment inscrire un gestionnaire pour un événement d’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a13abe8917d93ac6a4801e0c11cb7223da25e362923df229180b8c8e6211ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859598"
---
# <a name="how-to-register-a-handler-for-a-device-event"></a>Comment inscrire un gestionnaire pour un événement d’appareil

Les gestionnaires définissent la partie logicielle de l’exécution automatique. Ils définissent l’icône et le nom convivial du logiciel, ainsi que le composant COM (Component Object Model) à instancier et comment initialiser le composant en réponse à un événement. Chaque gestionnaire d’un événement spécifique s’inscrit sous la forme d’une valeur sous la clé **EventHandler** appropriée. Lorsque cet événement est détecté, l’utilisateur est invité à choisir un gestionnaire dans la liste de tous les gestionnaires inscrits pour cet événement.

## <a name="instructions"></a>Instructions


Les gestionnaires et leurs valeurs associées sont définis sous la  \\ clé des **gestionnaires** AutoplayHandlers. Les sous-clés diffèrent selon que le système peut lire le contenu de l’appareil directement ou si l’appareil fournit du contenu au système par le biais d’une interface propriétaire.

L’exemple suivant montre les sous-clés et les valeurs utilisées pour un périphérique, telles qu’une caméra vidéo numérique ou un lecteur .mp3, qui fournit son contenu au système par le biais d’une interface propriétaire. L’exemple de gestionnaire est appelé **MyHandler**.

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     Handlers
                        MyHandler
                           Action [REG_SZ] = Play music
                           CLSID [REG_SZ] = {a51f2ed3-634e-4a97-9d55-efcf08e7b32f}
                           DefaultIcon [REG_EXPAND_SZ] = %ProgramFiles%\Windows Media Player\wmplayer.exe,0
                           InitCmdLine [REG_SZ] = /Play
                           ProgID [REG_SZ] = WMP.PlayMusicFiles
                           Provider [REG_SZ] = Windows Media Player
```

> [!Note]  
> Tandis que l’exemple montre à la fois un ProgID et une valeur d’identificateur de classe (CLSID), dans la pratique, ces valeurs sont mutuellement exclusives afin qu’une seule ou l’autre soit présente. La valeur ProgID est préférée. Le cas échéant, il doit pointer vers un composant COM qui implémente l’interface [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) .

 

Vous pouvez entrer la valeur de l’action en tant que valeur littérale, par exemple « lire la musique » comme illustré dans cet exemple, ou en tant que nom de fichier avec une chaîne de ressource. Vous pouvez également entrer la valeur du fournisseur sous la forme d’une valeur littérale ou d’un nom de fichier avec une chaîne de ressource. L’exécution automatique combine la valeur d’action et la valeur de fournisseur avec le mot « using » pour créer une légende conviviale qui s’affiche dans l’interface utilisateur. dans l’exemple, la légende obtenue est « lire la musique à l’aide de Lecteur Windows Media ».

La valeur DefaultIcon pointe vers un fichier. ico ou une ressource dans un fichier binaire. Si la valeur numérique qui suit le nom de fichier binaire est égale ou supérieure à zéro, alors il s’agit de la valeur d’index de l’icône dans ce fichier binaire. S’il s’agit d’une valeur négative, il s’agit de l’ID de ressource icône. Les valeurs d’index négatives sont recommandées. Aucune valeur n’est nécessaire dans le cas d’un fichier. ico. Il est recommandé d’utiliser des variables d’environnement dans le chemin d’accès.

La valeur InitCmdLine passe l’état non modifié à l’aide de la méthode [**IHWEventHandler :: Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize) avant que toutes les autres méthodes ne soient appelées.

L’exemple suivant montre les sous-clés et les valeurs utilisées pour un appareil qui peut être lu directement, par exemple un lecteur de CD-ROM ou un autre disque amovible. Là encore, l’exemple de gestionnaire est appelé **MyHandler**.

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     Handlers
                        MyHandler
                           Action [REG_SZ] = @%systemroot%\System32\wiaacmgr.exe,-276
                           DefaultIcon [REG_EXPAND_SZ] = %systemroot%\System32\wiaacmgr.exe,-2
                           InvokeProgID [REG_SZ] = WIA.AutoPlayDropHandler
                           InvokeVerb [REG_SZ] = open
                           Provider [REG_SZ] = @%systemroot%\System32\wiaacmgr.exe,-101
```

Dans cet exemple, les valeurs action et Provider sont affichées sous la forme d’un nom de fichier avec une chaîne de ressource plutôt que des valeurs littérales, mais les chaînes qu’elles référencent sont utilisées de la même manière. Elles sont combinées avec le mot « using » pour former une légende conviviale, comme expliqué précédemment.

Les valeurs InvokeProgID et InvokeVerb remplacent CLSID, InitCmdLine et ProgID. Les valeurs InvokeProgID et InvokeVerb correspondent aux noms de clés qui se trouvent sous la **\_ \_ racine** de la clé HKEY, comme indiqué dans l’entrée de Registre suivante. Cet ensemble d’exemples de clés correspond à l’exemple de gestionnaire spécifique décrit précédemment.

```
HKEY_CLASSES_ROOT
   WIA.AutoplayDropHandler
      shell
         open
            DropTarget
               Clsid = {F1ABE2B5-C073-4dba-B6EB-FD7A5111DD8F}
```

La fonction [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) utilise le CLSID pour implémenter l’application appropriée.

Une fois que vous avez défini le gestionnaire de l’une des deux manières suivantes, vous devez l’inscrire pour un événement spécifique. Pour ce faire, vous devez fournir le nom du gestionnaire en tant que valeur pour la clé de cet événement sous **EventHandlers**. L’exemple suivant montre comment inscrire **MyHandler** en tant que gestionnaire pour l’événement GenericVolumeArrival. Aucune valeur de données n’est assignée.

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     EventHandlers
                        GenericVolumeArrival
                           MyHandler [REG_SZ]
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler)
</dt> <dt>

[**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

 
