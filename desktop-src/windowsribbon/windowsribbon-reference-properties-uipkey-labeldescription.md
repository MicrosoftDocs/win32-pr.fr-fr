---
title: UI_PKEY_LabelDescription
description: Identifie la propriété LabelDescription de l’interface utilisateur \_ \_ .
ms.assetid: e7dfbe7e-c9c9-44fe-9e2d-39e20f5f7062
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cb81e723d5f55dcfd63f1bb89bff4741b4e088e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840298"
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

## <a name="remarks"></a>Notes

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

 

 




