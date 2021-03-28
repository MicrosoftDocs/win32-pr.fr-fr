---
description: Une icône personnalisée doit être affectée à un type de fichier pour fournir une indication visuelle à l’utilisateur de ce type de fichier ou à l’application à laquelle ce type de fichier est associé.
ms.assetid: 84F293C2-BAB1-4BF8-9F89-122B6DAB29C3
title: Comment assigner une icône personnalisée à un type de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf625eb6177471702096f462846b8035772177ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973182"
---
# <a name="how-to-assign-a-custom-icon-to-a-file-type"></a>Comment assigner une icône personnalisée à un type de fichier

Quand aucune icône par défaut personnalisée n’est assignée à un type de fichier, le bureau et l’Explorateur Windows affichent tous les fichiers de ce type avec une icône générique par défaut. Par exemple, la capture d’écran suivante montre cette icône par défaut utilisée avec le fichier MyDocs4. MYP.

![capture d’écran de l’icône par défaut](images/icon.png)

Bien que tous les fichiers affichés dans cette capture d’écran soient des fichiers texte simples, seul MyDocs4. MYP affiche l’icône par défaut de Windows. Cela est dû au fait que l’extension. txt est un type de fichier inscrit qui a une icône par défaut personnalisée.

La capture d’écran suivante montre une icône personnalisée qui a été affectée au type de fichier. MYP.

![capture d’écran de l’icône personnalisée pour les fichiers. MYP](images/context4.png)

> [!Note]  
> Les icônes peuvent également être affectées sur la base d’une application spécifique.

 

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Étape 1 :

Créez une sous-clé nommée **DefaultIcon** dans l’un des deux emplacements suivants :

-   Pour une assignation de type de fichier, **HKEY \_ classes \_ root** \\ *. extension*
-   Pour une assignation d’application **, \_ classe \_** de l’identificateur racine de la racine de HKEY \\ 

### <a name="step-2"></a>Étape 2 :

Affectez à la sous-clé **DefaultIcon** une valeur par défaut de type **reg \_ SZ** qui spécifie le chemin d’accès complet au fichier qui contient l’icône.

### <a name="step-3"></a>Étape 3 :

Appelez la fonction [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) pour notifier à l’interpréteur de mise à jour son cache d’icône.

## <a name="remarks"></a>Notes

L’exemple suivant montre une vue détaillée des entrées de Registre requises pour l’affectation d’une icône de type de fichier. L’extension de nom de fichier est associée à une application, mais l’affectation d’icône correspond à l’extension de nom de fichier proprement dite afin que l’application associée ne dicte pas l’icône par défaut.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      DefaultIcon
         (Default) = C:\MyDir\MyProgram.exe,2
```

L’exemple suivant montre une vue détaillée des entrées de Registre requises pour l’affectation d’une icône d’application. L’extension de nom de fichier. MYP est d’abord associée à l’application MyProgram. 1. La sous-clé ProgID MyProgram. 1 est ensuite affectée à l’icône par défaut personnalisée.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      DefaultIcon
         (Default) = C:\MyDir\MyProgram.exe,2
```

Tout fichier qui contient une icône est acceptable, y compris les fichiers. ico,. exe et. dll. Si le fichier contient plusieurs icônes, le chemin d’accès doit être suivi d’une virgule, puis de l’index de l’icône.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de fichiers](fa-file-types.md)
</dt> </dl>

 

 



