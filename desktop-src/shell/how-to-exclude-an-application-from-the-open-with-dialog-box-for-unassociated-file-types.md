---
description: Comment exclure une application de la boîte de dialogue Ouvrir avec pour le type de fichier non associé.
title: Comment exclure une application de la boîte de dialogue Ouvrir avec pour les types de fichiers non associés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d90ae5ab49128df1eedd9b760286ce54f6b6498cbe00d4a945145a80f956cde
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350911"
---
# <a name="how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types"></a>Comment exclure une application de la boîte de dialogue Ouvrir avec pour les types de fichiers non associés

Lorsqu’un utilisateur tente d’ouvrir un fichier qui n’est pas membre d’un type de fichier inscrit (autrement dit, un type de fichier inconnu), ou lorsqu’un utilisateur sélectionne **Ouvrir avec** ou **ouvrir avec-> choisir le programme par défaut** dans le menu contextuel d’un fichier, le shell présente un sous-menu ou une boîte de dialogue qui permet à l’utilisateur de spécifier le programme utilisé pour ouvrir

Par défaut, toute application inscrite en tant que sous-clé de la **\_ classe HKEY classes \_ racine** \\  est présentée dans la boîte de dialogue **Ouvrir avec** . Ces applications sont présentées dans **Open avec** , que l’application soit inscrite ou non pour gérer le type de fichier.

Pour empêcher qu’une application n’apparaisse dans la boîte de dialogue **Ouvrir avec** lorsque l’application ne doit pas ou ne peut pas être utilisée pour ouvrir certains types de fichiers, utilisez l’une des deux techniques décrites dans cette rubrique.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Étape 1 :

Ajoutez une entrée NoOpenWith à la sous-clé de l’application. quand une application utilise un type de fichier, Windows enregistre ces informations pour créer la liste des **programmes recommandés** . Cette liste est présentée dans le sous-menu **Ouvrir avec** , comme illustré dans la capture d’écran suivante.

![capture d’écran du menu contextuel avec le sous-menu Ouvrir avec affiché](images/file-assoc/openwithsubmenu.png)

Ces applications recommandées sont également affichées dans la partie **Programmes recommandés** de la boîte de dialogue **Ouvrir avec** , comme illustré dans la capture d’écran suivante.

![capture d’écran de la boîte de dialogue Ouvrir avec avec les programmes recommandés](images/file-assoc/openwithdialog.png)

> [!Note]  
> Si une application s’est inscrite dans [OpenWithList](fa-file-types.md) ou OpenWithProgIDs pour le type de fichier, elle apparaît dans la liste des **Programmes recommandés** , même si l’entrée NoOpenWith est définie. En outre, n’oubliez pas que, qu’une application soit proposée dans une liste de programmes recommandés, un utilisateur peut accéder manuellement à n’importe quel fichier exécutable.

 

Les applications peuvent désactiver ce suivi en spécifiant une valeur NoOpenWith sous la sous-clé de l’application.

L’entrée NoOpenWith est une valeur **reg \_ SZ** vide, comme illustré dans l’exemple suivant.

```
HKEY_CLASSES_ROOT
   Applications
      MyProgram.exe
         NoOpenWith
```

La définition de l’entrée NoOpenWith a également les effets suivants :

-   Empêche l’épinglage d’un fichier à la liste de liens de l’application par le biais du glisser-déplacer, sauf si l’application est inscrite spécifiquement pour gérer ce type de fichier.
-   Empêche la boîte de dialogue de fichier commune et tout appel à la fonction [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) d’ajouter n’importe quel fichier à la liste de raccourcis de l’application, sauf si l’application est inscrite spécifiquement pour gérer ce type de fichier.

### <a name="step-2"></a>Étape 2 :

La deuxième façon d’empêcher une application d’apparaître dans la boîte de dialogue **Ouvrir avec** consiste à utiliser la sous-clé **SupportedTypes** pour répertorier explicitement les extensions des types de fichiers que l’application peut ouvrir. Cela empêche l’application d’apparaître dans la boîte de dialogue **Ouvrir avec** pour les types de fichiers qu’elle ne peut pas ouvrir. Cela entraîne également l’affichage de l’application dans la liste des **Programmes recommandés** , comme indiqué précédemment.

Cette méthode est particulièrement utile si une application peut enregistrer un fichier sous un certain type de fichier, mais ne peut pas ouvrir ce type de fichier. Une application doit également définir l' \_ indicateur Fos DONTADDTORECENT par le biais de [**IFileDialog :: SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) lors de l’appel de la boîte de dialogue **Enregistrer** . Cela empêche l’ajout de l’élément aux portions **récentes** ou **fréquentes** d’une liste de raccourcis. Il empêche également le suivi de l’application sous [OpenWithList](fa-file-types.md).

Chaque extension prise en charge est ajoutée sous la forme d’une entrée sous la sous-clé **SupportedTypes** , comme indiqué dans l’exemple suivant. Les entrées sont de type **reg \_ SZ** ou **reg \_ null**, sans valeurs associées.

```
HKEY_CLASSES_ROOT
   Applications
      ApplicationName
         SupportedTypes
            .ext1
            .ext2
            .ext3
```

Si une sous-clé **SupportedTypes** est fournie, seuls les fichiers avec ces extensions sont éligibles à l’épinglage à la liste de raccourcis de l’application ou au suivi dans la liste des destinations **récentes** ou **fréquentes** d’une application.

L’entrée NoOpenWith remplace la sous-clé **SupportedTypes** et masque l’application dans la boîte de dialogue **Ouvrir avec** .

 

 
