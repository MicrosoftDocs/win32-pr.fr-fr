---
description: Cette rubrique explique comment inscrire un gestionnaire d’aperçus associé à un type de données donné.
ms.assetid: 5f194d29-d09f-4426-a63e-911db65ce700
title: Comment inscrire un gestionnaire d’aperçus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5af9610de1822678521557fc20aa53f4e556e0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973131"
---
# <a name="how-to-register-a-preview-handler"></a>Comment inscrire un gestionnaire d’aperçus

Cette rubrique explique comment inscrire un gestionnaire d’aperçus associé à un type de données donné. À des fins d’illustration, les exemples de cette rubrique utilisent un type de fichier. xyz. L’inscription d’un gestionnaire d’aperçus est un enregistrement standard basé sur une association de fichiers.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Étape 1 :

Tout d’abord, une extension de nom de fichier est associée à un ProgID. L’entrée suivante associe la sous-clé **xyzfile** ProgID à l’extension de nom de fichier. xyz.

```
HKEY_CLASSES_ROOT
   .xyz
      (Default) = [REG_SZ] xyzfile
```

La sous-clé **xyzfile** ProgID est stockée avec les autres ProgID comme indiqué ci-dessous :

```
HKEY_CLASSES_ROOT
   xyzfile
```

Chaque sous-clé ProgID du gestionnaire d’aperçus contient une sous-clé nommée **shellex** qui contient une sous-clé *toujours* nommée **{8895b1c6-B41F-4c1c-A562-0d564250836f}**. La présence de cette sous-clé indique au système que le gestionnaire est un gestionnaire d’aperçus.

La valeur par défaut de la sous-clé **{8895b1c6-B41F-4c1c-A562-0d564250836f}** est l’identificateur de classe (CLSID) de votre gestionnaire. Un exemple de la sous-clé **xyzfile** ProgID est illustré ici, associant un gestionnaire de CLSID {ec3a629a-a47c-4245-BC78-b4b63d0e3154}.

```
HKEY_CLASSES_ROOT
   xyzfile
      shellex
         {8895b1c6-b41f-4c1c-a562-0d564250836f}
            (Default) = [REG_SZ] {ec3a629a-a47c-4245-bc78-b4b63d0e3154}
```

### <a name="step-2"></a>Étape 2 :

Ensuite, ajoutez la sous-clé sous **CLSID** pour votre gestionnaire d’aperçus. Un exemple est illustré ici. Une explication des entrées individuelles suit.

```
HKEY_CLASSES_ROOT
   CLSID
      {ec3a629a-a47c-4245-bc78-b4b63d0e3154}
         (Default) = [REG_SZ] Fabricam XYZ Preview Handler
         DisplayName = [REG_SZ] @myhandler.dll,-101
         Icon = [REG_SZ] myhandler.dll,201
         AppID = [REG_SZ] {6d2b5079-2f0b-48dd-ab7f-97cec514d30b}
         InprocServer32
            (Default) = [REG_EXPAND_SZ] %ProgramFiles%\Fabricam\myhandler.dll
            ThreadingModel = [REG_SZ] Apartment
            ProgID = [REG_SZ] xyzfile
            VersionIndependentProgID = [REG_SZ] Version IndependentProgID
```

La valeur par défaut de votre sous-clé ( **{ec3a629a-A47C-4245-BC78-b4b63d0e3154}**) n’est pas obligatoire ou utilisée. Toutefois, la définition d’une chaîne non localisée peut vous aider à déboguer les problèmes d’inscription.

Le signe moins (-101) dans la ressource. dll de l’entrée DisplayName existe pour des raisons d’héritage. En revanche, l’entrée d’icône ne nécessite pas de signe moins.

La valeur AppID donne une référence à l’AppID de l’application associée à l’extension de nom de fichier (stockée sous l’AppID **\_ \_ racine de classes HKEY** \\ . La valeur utilisée ici ({6d2b5079-2f0b-48dd-AB7F-97cec514d30b}) est l’ID de l’hôte de substitution Prevhost.exe. les gestionnaires d’aperçus 32 bits doivent utiliser **AppID** {534A1E02-D58F-44f0-B58B-36CBED287C7C} lorsqu’ils sont installés sur des systèmes d’exploitation 64 bits.

Les entrées sous la sous-clé **InprocServer32** incluent une référence à la sous-clé ProgID de l’extension de nom de fichier, ainsi qu’une entrée pour un [VersionIndependentProgID](../com/versionindependentprogid.md).

### <a name="step-3"></a>Étape 3 :

Enfin, le gestionnaire d’aperçus doit être ajouté à la liste de tous les gestionnaires d’aperçus. Cette liste est utilisée comme une optimisation par le système pour énumérer tous les gestionnaires d’aperçus inscrits à des fins d’affichage. Là encore, la valeur par défaut n’est pas obligatoire, elle facilite simplement le processus de débogage.

> [!Note]  
> Dans Windows 7, si l’application est installée pour tous les utilisateurs de l’ordinateur, utilisez HKEY \_ local \_ machine ; si pour un seul utilisateur, utilisez HKEY \_ Current \_ User.

 

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PreviewHandlers
                  {ec3a629a-a47c-4245-bc78-b4b63d0e3154}
                     (Default) = [REG_SZ] Fabricam XYZ Preview Handler
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestionnaires d’aperçus et hôte de l’interpréteur de commandes](preview-handlers.md)
</dt> <dt>

[Génération de gestionnaires d’aperçus](building-preview-handlers.md)
</dt> <dt>

[Instructions du gestionnaire d’aperçus](preview-handler-guidelines.md)
</dt> </dl>

 

 
