---
description: Accès à une valeur de registre sans nom
ms.assetid: 1095da4c-8b9f-4674-9801-f2d25c4f372b
ms.tgt_platform: multiple
title: Accès à une valeur de registre sans nom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d62a82cfdb9d90ba11a177891ad7ee5e3310207825bd9a155c5eda3b10c4e68e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131922"
---
# <a name="accessing-an-unnamed-registry-value"></a>Accès à une valeur de registre sans nom

La valeur par défaut ou la valeur sans nom d’une clé de Registre est indiquée comme (par défaut) ou <No Name> dans l’éditeur du Registre regedit. Vous pouvez utiliser le fournisseur de Registre système pour accéder à une clé de registre sans nom. De même, vous pouvez également utiliser le fournisseur de Registre système pour accéder aux descriptions des bitmaps, qui sont définies en tant que valeurs sans nom.

La procédure suivante décrit comment récupérer une valeur de registre sans nom.

**Pour récupérer une valeur de registre sans nom**

1.  Définissez une propriété et définissez le qualificateur **PropertyContext** de cette propriété sur une chaîne vide.

    L’exemple de code suivant montre comment la classe définit des propriétés pour stocker des valeurs pour la clé spécifiée par le qualificateur **ClassContext** . La valeur par défaut est stockée dans la propriété **par défaut** .

    ``` syntax
    [dynamic, 
     provider("RegProv"), 
     ClassContext("local|hkey_local_machine\\software\\"
     "microsoft\\Active Setup\\Installed Components")]

    class RegTrans{
      [key] String Transports="";
      [PropertyContext("")] String Default;
      [PropertyContext("ComponentId")] String ComponentID;
      [PropertyContext("Locale")] String Locale;
    };
    ```

    La clé de transport n’utilise pas la valeur sans nom ; la compilation de ce fichier MOF ne produit donc aucune valeur pour la propriété **par défaut** , sauf si un outil de modification du Registre est utilisé pour modifier la valeur sans nom.

2.  Pour un fichier bitmap, définissez une propriété et définissez le **PropertyContext** de cette propriété.

    L’exemple de code suivant montre comment définir une propriété.

    ```mof
    Local|hkey_classes_root\\.bmp
    ```

    

 

 



