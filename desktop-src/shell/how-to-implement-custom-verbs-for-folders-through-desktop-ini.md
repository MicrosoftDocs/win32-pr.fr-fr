---
description: dans Windows 7 et versions ultérieures, vous pouvez ajouter des verbes à un dossier à l’aide de Desktop.ini. Pour plus d’informations sur les fichiers de Desktop.ini, consultez Comment personnaliser des dossiers avec des Desktop.ini.
ms.assetid: F03AB35D-FBFE-46C2-A37F-F70C18219B9A
title: Comment implémenter des verbes personnalisés pour les dossiers via Desktop.ini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f49b3f12d51848d08e6480d4180a3768b807703e5655e3fcfcddffcdaf16b734
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111779"
---
# <a name="how-to-implement-custom-verbs-for-folders-through-desktopini"></a>Comment implémenter des verbes personnalisés pour les dossiers via Desktop.ini

dans Windows 7 et versions ultérieures, vous pouvez ajouter des verbes à un dossier à l’aide de Desktop.ini. Pour plus d’informations sur les fichiers de Desktop.ini, consultez [Comment personnaliser des dossiers avec des Desktop.ini](how-to-customize-folders-with-desktop-ini.md).

> [!Note]  
> Desktop.ini fichiers doivent toujours être marqués comme étant  +  **masqués** par le système afin qu’ils ne soient pas affichés aux utilisateurs.

 

Pour ajouter des verbes personnalisés pour les dossiers à l’aide d’un fichier Desktop.ini, procédez comme suit.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Étape 1 :

Créez un dossier marqué **en lecture seule** ou **système**.

### <a name="step-2"></a>Étape 2 :

Créez un fichier de Desktop.ini qui comprend un \[ . ShellClassInfo \] DirectoryClass = ProgID du dossier.

### <a name="step-3"></a>Étape 3 :

Dans le registre, créez le dossier racine de l’identificateur de classe de la **\_ classe \_ HKEY** \\  avec la valeur CanUseForDirectory. La valeur CanUseForDirectory évite l’utilisation abusive des ProgID qui sont définis pour ne pas participer à l’implémentation de verbes personnalisés pour les dossiers par le biais de Desktop.ini.

### <a name="step-4"></a>Étape 4 :

Ajoutez des verbes dans la sous-clé du **dossier** ProgID, par exemple :

```
HKEY_CLASSES_ROOT
   CustomFolderType
      Shell
         MyVerb
            command
               (Default) = %SystemRoot%\system32\notepad.exe %1\desktop.ini
```

## <a name="remarks"></a>Remarques

> [!Note]  
> Ces verbes peuvent être les verbes par défaut. dans ce cas, le double-clic sur le dossier active le verbe.

 

 

 



