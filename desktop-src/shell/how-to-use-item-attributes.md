---
description: Les valeurs d’indicateur SFGAO des attributs d’environnement d’un élément peuvent être testées pour déterminer si le verbe doit être activé ou désactivé.
ms.assetid: 3A539A9D-DB6B-4E3D-AD26-D5309BECEBB1
title: Utilisation des attributs d’élément
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2ddcc567a820ba1d9c1394ca38f78fc9ce9ec634596f8dbe41feca9def32e90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859568"
---
# <a name="how-to-use-item-attributes"></a>Utilisation des attributs d’élément

Les valeurs d’indicateur [**SFGAO**](sfgao.md) des attributs d’environnement d’un élément peuvent être testées pour déterminer si le verbe doit être activé ou désactivé.

Pour utiliser cette fonctionnalité d’attribut, ajoutez les valeurs **reg \_ DWORD** suivantes sous le verbe :

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Étape 1 :

La valeur AttributeMask spécifie la valeur [**SFGAO**](sfgao.md) des valeurs de bit du masque avec lequel effectuer le test.

### <a name="step-2"></a>Étape 2 :

La valeur AttributeValue spécifie la valeur [**SFGAO**](sfgao.md) des bits qui sont testés.

### <a name="step-3"></a>Étape 3 :

Le ImpliedSelectionModel spécifie zéro pour les verbes d’élément, ou une valeur différente de zéro pour les verbes dans le menu contextuel d’arrière-plan.

## <a name="remarks"></a>Remarques

Dans l’exemple d’entrée de Registre suivant, AttributeMask est défini sur [**SFGAO \_ ReadOnly**](sfgao.md) (0x40000).

```
HKEY_CLASSES_ROOT
   txtfile
      Shell
         test.verb2
            AttributeMask = 0x40000
            AttributeValue = 0x0
            ImpliedSelectionModel = 0x0
            command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

 

 



