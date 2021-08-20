---
description: Vous pouvez utiliser le registre pour définir un ou plusieurs verbes étendus. Les commandes associées s’affichent uniquement quand l’utilisateur clique avec le bouton droit sur un objet tout en appuyant sur la touche Maj.
ms.assetid: C6E51716-1D4F-454F-9AF4-8D0E486CB885
title: Comment définir des verbes étendus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef73244a03101de02653625912701b81aa9e8e11d975f96dd417eaa137bfba07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859716"
---
# <a name="how-to-define-extended-verbs"></a>Comment définir des verbes étendus

Vous pouvez utiliser le registre pour définir un ou plusieurs verbes étendus. Les commandes associées s’affichent uniquement quand l’utilisateur clique avec le bouton droit sur un objet tout en appuyant sur la touche Maj.

## <a name="instructions"></a>Instructions


Pour définir un verbe comme étendu, ajoutez simplement une valeur **\_ SZ** « étendue » à la sous-clé du verbe. Aucune donnée ne doit être associée à la valeur. L’exemple d’entrée de Registre suivant montre l’exemple de la section précédente, avec « doit » défini en tant que verbe étendu.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      (Default) = MyProgram Application
      Shell
         (Default) = doit
         open
            command
               (Default) = C:\MyDir\MyProgram.exe "%1"
         doit
            (Default) = &Do It
            extended
            command
               (Default) = C:\MyDir\MyProgram.exe /d "%1"
         print
            command
               (Default) = C:\MyDir\MyProgram.exe /p "%1"
         printto
            command
               (Default) = C:\MyDir\MyProgram.exe /p "%1" "%2" %3 %4
```

 

 



