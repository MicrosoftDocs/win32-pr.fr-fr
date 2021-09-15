---
description: Illustre l’appel d’une commande DDE à l’aide d’un verbe de Shell.
ms.assetid: 65DDD992-5E96-447E-9151-2CCA740822A1
title: Comment associer des verbes à des commandes DDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7174a22c993d93c347c8a0368fa7d1798362070f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127294751"
---
# <a name="how-to-associate-verbs-with-dde-commands"></a>Comment associer des verbes à des commandes DDE

L’appel d’un verbe lance normalement l’application spécifiée par la sous-clé de commande du verbe. toutefois, si votre application prend en charge les échange dynamique de données (DDE), vous pouvez à la place demander à l’interpréteur de commandes dde de lancer une conversation DDE.

Pour spécifier que l’appel d’un verbe doit initier une conversation DDE, procédez comme suit.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Étape 1 :

Ajoutez une sous-clé **ddeexec** à la clé du verbe.

### <a name="step-2"></a>Étape 2 :

Définissez la valeur par défaut de **ddeexec** sur la chaîne de commande DDE.

## <a name="remarks"></a>Notes

La clé **ddeexec** a trois sous-clés facultatives qui fournissent un certain contrôle sur le processus DDE :

-   **application**. Définissez la valeur par défaut de cette sous-clé sur le nom de l’application à utiliser pour établir la conversation DDE. S’il n’existe aucune sous-clé d' **application** , la valeur par défaut de la sous-clé de **commande** du verbe est utilisée comme nom d’application.
-   **rubrique**. Définissez la valeur par défaut de cette sous-clé sur le nom de la rubrique de la conversation DDE. S’il n’existe aucune sous-clé de **rubrique** , System est utilisé comme nom de rubrique.
-   **ifexec**. Définissez la valeur par défaut de cette sous-clé sur la commande DDE à utiliser si la conversation DDE ne peut pas être lancée. Lorsque l’initialisation échoue, l’application qui est spécifiée par la valeur par défaut de la sous-clé de **commande** du verbe est lancée. Si une clé **ifexec** existe, sa valeur par défaut est utilisée comme commande DDE. S’il n’existe aucune sous-clé **ifexec** , la valeur par défaut de la clé **ddeexec** est réutilisée comme commande DDE.

L’exemple suivant spécifie que l’appel du verbe Open pour MyProgram. 1 lance une conversation DDE avec la commande DDE Open (« %1 ») et le nom d’application MyProgram.

```
HKEY_CLASSES_ROOT
   MyProgram.1
      (Default) = MyProgram Application
      Shell
         (Default) = doit
         open
            command
               (Default) = C:\MyDir\MyProgram.exe "%1"
            ddeexec
               (Default) = Open("%1")
               application
                  (Default) = MyProgram
```

 

 



