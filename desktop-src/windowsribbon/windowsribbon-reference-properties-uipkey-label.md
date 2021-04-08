---
title: UI_PKEY_Label
description: Identifie la propriété de l’étiquette de l’interface utilisateur \_ \_ .
ms.assetid: 4d704133-bba7-4c32-a552-d748b66455eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 245ce8d239e1a0893c907a047aa9a48996cbf606
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840301"
---
# <a name="ui_pkey_label"></a>\_Étiquette de nom de l’interface utilisateur \_

Identifie la propriété de l’étiquette de l’interface utilisateur \_ \_ .

```
propertyDescription
   name = UI_PKEY_Label
   shellPKey = UI_PKEY_Label
   formatID = 00000004-7363-696e-8441798acf5aebb7
   propID = 4
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Notes

L' \_ \_ étiquette de groupe de caractères de l’interface utilisateur est utilisée par une application pour interroger le texte d’étiquette des onglets, des groupes, des boutons, des éléments de la Galerie et d’autres contrôles du ruban.

> [!Note]  
> Windows 8 et versions ultérieures : l’image du bouton de menu de l' [application](windowsribbon-controls-applicationmenu.md) a été changée en étiquette : **fichier**. Nous vous recommandons de ne pas utiliser de fichier comme étiquette pour vos propres onglets.

 

La valeur de la propriété est une chaîne limitée à toute séquence de caractères, y compris les espaces blancs et les sauts de ligne.

> [!Note]  
> Utilisez la référence de caractère XML UCS (Universal Character Set) `&#xA;` pour spécifier un saut de ligne.

 

L’alignement à droite n’est pas pris en charge.

La longueur maximale de l’étiquette de nom de la base de l’interface utilisateur \_ \_ est illimitée.

Si une commande est exposée à l’aide d’un élément de menu et que la valeur de [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) ou de l’étiquette de l’interface utilisateur \_ \_ contient une lettre précédée d’une esperluette, comme indiqué dans l’exemple suivant, cette lettre est traitée comme une touche d’accès et une touche d’accès rapide pour cette commande par l’infrastructure du ruban.


```XML
<Command Name="cmdNew"
         Symbol="ID_FILE_NEW"
         Comment="New"
         Id="25001"
         LabelTitle="&amp;New"/>
```



Pour afficher une esperluette dans une étiquette, échappez la désignation de caractères spéciaux par une double esperluette ( `&&` ), comme illustré dans l’exemple suivant.


```XML
<Command Name="cmdOpen"
         Symbol="ID_FILE_OPEN"
         Comment="Open"
         Id="25002"
         LabelTitle="&amp;&amp;Open"/>
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Propriétés de la ressource](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**Commande. LabelTitle**](windowsribbon-element-command-labeltitle.md)
</dt> <dt>

[IU \_ \_ LabelDescription](windowsribbon-reference-properties-uipkey-labeldescription.md)
</dt> </dl>

 

 




