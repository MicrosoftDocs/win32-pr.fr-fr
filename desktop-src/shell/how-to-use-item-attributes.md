---
description: Les valeurs d’indicateur SFGAO des attributs d’environnement d’un élément peuvent être testées pour déterminer si le verbe doit être activé ou désactivé.
ms.assetid: 3A539A9D-DB6B-4E3D-AD26-D5309BECEBB1
title: Utilisation des attributs d’élément
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a438c81258677822ca9b940eb9f74366d6226ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864913"
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

## <a name="remarks"></a>Notes

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

 

 



