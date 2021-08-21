---
title: UI_PKEY_LabelDescription
description: Identifie la propriété LabelDescription de l’interface utilisateur \_ \_ .
ms.assetid: e7dfbe7e-c9c9-44fe-9e2d-39e20f5f7062
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d80a2db487988f66fcc393b3ba449dfda789248dabc3cd9e1d3e48acf9ba3473
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437995"
---
# <a name="ui_pkey_labeldescription"></a>IU \_ \_ LabelDescription

Identifie la propriété LabelDescription de l’interface utilisateur \_ \_ .

```
propertyDescription
   name = UI_PKEY_LabelDescription
   shellPKey = UI_PKEY_LabelDescription
   formatID = 00000002-7363-696e-8441798acf5aebb7
   propID = 2
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Remarques

L’interface utilisateur \_ \_ LabelDescription est utilisée par une application pour interroger la description associée à une [étiquette de \_ \_ nom d’utilisateur](windowsribbon-reference-properties-uipkey-label.md).

La valeur de la propriété est une chaîne limitée à toute séquence de caractères, y compris les espaces blancs et les sauts de ligne.

> [!Note]  
> Utilisez la référence de caractère XML UCS (Universal Character Set) `&#xA;` pour spécifier un saut de ligne.

 

La longueur maximale est illimitée.

L’alignement à droite n’est pas pris en charge.

La capture d’écran suivante illustre l’utilisation d’une étiquette et d’une description d’étiquette associée dans un menu d’application.

![capture d’écran montrant une étiquette et une description d’étiquette associée dans un menu d’application.](images/properties/ui-pkey-labeldescription.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Propriétés de la ressource](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**Commande. LabelDescription**](windowsribbon-element-command-labeldescription.md)
</dt> <dt>

[\_Étiquette de nom de l’interface utilisateur \_](windowsribbon-reference-properties-uipkey-label.md)
</dt> </dl>

 

 




