---
title: UI_PKEY_Keytip
description: Identifie la propriété de KeyTip de l’interface utilisateur \_ \_ .
ms.assetid: 7af4abcb-abb0-466a-bc58-274fa18b79af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 940a855561dfd30dfbf063323f4b86b03561163c4fbf34f9db08be4eb3e1ece3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028607"
---
# <a name="ui_pkey_keytip"></a>KeyTip de l’interface utilisateur \_ \_

Identifie la propriété de KeyTip de l’interface utilisateur \_ \_ .

```
propertyDescription
   name = UI_PKEY_Keytip
   shellPKey = UI_PKEY_Keytip
   formatID = 00000003-7363-696e-8441798acf5aebb7
   propID = 3
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Remarques

L’interface utilisateur de \_ \_ la touche d’accès rapide est utilisée par une application pour interroger l’accélérateur clavier d’un contrôle de ruban.

Cette valeur de propriété est une chaîne, composée d’une séquence de caractères, y compris un espace blanc.

La valeur de l’interface utilisateur de la touche d’accès \_ \_ rapide agit comme touche d’accès rapide pour une commande, sauf si cette commande est exposée par le biais d’un élément de menu. Dans ce cas, le Framework ignore la valeur de KeyTip KeyTip de l’interface utilisateur \_ \_ et utilise à la place un caractère précédé d’un signe & comme spécifié par la [**commande. LabelTitle**](windowsribbon-element-command-labeltitle.md) ou [l’étiquette du \_ \_ nom de l’interface utilisateur](windowsribbon-reference-properties-uipkey-label.md). Si aucune esperluette n’est spécifiée par la **commande. LabelTitle** ou l' \_ \_ étiquette de nom de l’interface utilisateur, aucune touche d’accès ou touche d’accès rapide n’est exposée.

La longueur maximale de la touche d’entrée de l’interface utilisateur \_ \_ est illimitée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Propriétés de la ressource](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**Commande. KeyTip**](windowsribbon-element-command-keytip.md)
</dt> </dl>

 

 




