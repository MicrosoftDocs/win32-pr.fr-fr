---
description: dans Windows 7 et versions ultérieures, vous pouvez utiliser la sous-clé ExtendedSubCommandsKey pour créer des menus en cascade étendus.
ms.assetid: 6E8B4FB7-D4DB-4DBC-AF6F-59D02CB6AB13
title: Créer des menus en cascade avec l’entrée de Registre ExtendedSubCommandsKey
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 220a38825ae250a0d58d30bc7de93f290f819eb8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296119"
---
# <a name="how-to-create-cascading-menus-with-the-extendedsubcommandskey-registry-entry"></a>Comment créer des menus en cascade avec l’entrée de Registre ExtendedSubCommandsKey

dans Windows 7 et versions ultérieures, vous pouvez utiliser la sous-clé **ExtendedSubCommandsKey** pour créer des menus en cascade étendus.

La capture d’écran suivante est un exemple de menu en cascade étendu.

![capture d’écran montrant le menu en cascade étendu pour les appareils](images/file-assoc/extendedsubcommandskey.png)

Étant donné que **HKEY \_ classes \_ root** est une combinaison de **HKEY \_ Current \_ User** et de **HKEY \_ local \_ machine**, vous pouvez inscrire les sous-verbes sous la sous-clé de classes de logiciels de l' **\_ \_ utilisateur actuel HKEY** \\  \\  . L’avantage de cette approche est que les autorisations élevées ne sont pas requises. D’autres associations de fichiers peuvent réutiliser cet ensemble complet de verbes en spécifiant la même sous-clé **ExtendedSubCommandsKey** . Si vous n’avez pas besoin de réutiliser cet ensemble de verbes, vous pouvez répertorier les verbes sous le parent. Dans ce cas, assurez-vous que la valeur par défaut du parent est vide, comme illustré dans l’exemple d’entrée de Registre dans cette section.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Étape 1 :

Créez une sous-clé sous **HKEY \_ classes \_ racine** \\ *ProgID* \\ **Shell** \\ *CascadeMenuKey* et donnez à CascadeMenuKey un nom tel que *CascadeTest*, par exemple. Ajoutez ensuite une entrée MUIVerb de type de Registre **\_ SZ** et donnez-lui un nom tel que test cascade menu 2, comme illustré dans l’exemple de Registre suivant.

```
HKEY_CLASSES_ROOT
   txtfile
      shell
         CascadeTest
            MUIVerb = Test Cascade Menu 2
```

### <a name="step-2"></a>Étape 2 :

Sous la sous-clé *CascadeTest* que vous avez créée, ajoutez une sous-clé **ExtendedSubCommandsKey** , puis ajoutez les sous-commandes du document (de type **reg \_ SZ**), par exemple :

```
HKEY_CLASSES_ROOT
   txtfile
      Shell
         Test Cascade Menu 2
            (Default)
            ExtendedSubCommandsKey
               Layout
               Properties
               Select all
```

Assurez-vous que la valeur par défaut de la sous-clé *menu de test cascade 2* est vide et affichée comme **(valeur non définie)**.

### <a name="step-3"></a>Étape 3 :

Remplissez les sous-verbes à l’aide de l’une des implémentations de verbe statique suivantes. Notez que la sous-clé CommandFlags représente les valeurs EXPCMDFLAGS. Si vous souhaitez ajouter un séparateur avant ou après l’élément de menu cascade, utilisez ECF \_ SEPARATORBEFORE (0x20) ou ECF \_ SEPARATORAFTER (0x40). pour obtenir une description des indicateurs Windows 7 et versions ultérieures, consultez [**IExplorerCommand :: GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags). ECF \_ SEPARATORBEFORE fonctionne uniquement pour les éléments de menu de niveau supérieur. MUIVerb est de type **reg \_ SZ** et CommandFlags est de type **reg \_ DWORD**.

```
HKEY_CLASSES_ROOT
   txtile
      Shell
         Test Cascade Menu 2
            (Default)
            ExtendedSubCommandsKey
               Shell
                  cmd1
                     MUIVerb = Notepad
                     command
                        (Default) = %SystemRoot%\system32\notepad.exe %1
                  cmd2
                     MUIVerb = Wordpad
                     CommandFlags = 0x20
                     command
                        (Default) = C:\Program Files\Windows NT\Accessories\wordpad.exe %1
```

## <a name="remarks"></a>Notes

La capture d’écran suivante illustre les exemples d’entrée de clé de Registre précédents.

![capture d’écran montrant un exemple de menu en cascade montrant les choix du bloc-notes et de WordPad](images/file-assoc/testcascademenu2.png)

 

 



