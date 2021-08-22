---
title: UI_PKEY_FontProperties_Size
description: Identifie la \_ propriété de \_ taille FontProperties de l’interface utilisateur \_ .
ms.assetid: bd426910-9852-48e1-91c8-b94be5ef7199
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9c013c41290f6e062b03572a9e3cb848752efcb12f1c779348a0253f94d40e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028627"
---
# <a name="ui_pkey_fontproperties_size"></a>\_Taille de \_ FontProperties de l’interface utilisateur \_

Identifie la \_ propriété de \_ taille FontProperties de l’interface utilisateur \_ .

```
propertyDescription
   name = UI_PKEY_FontProperties_Size
   shellPKey = UI_PKEY_FontProperties_Size
   formatID = 00000302-7363-696e-8441798acf5aebb7
   propID = 302
   typeInfo
      type = VT_DECIMAL
```

## <a name="remarks"></a>Remarques

\_ \_ La taille FontProperties de l’interface utilisateur \_ est utilisée par une application pour interroger la valeur du contrôle de **taille de police** .

Les valeurs valides pour cette propriété sont comprises entre 1 et 9999 inclus. Si un utilisateur tente d’entrer une valeur non valide, l’entrée est rejetée et le contrôle de **taille de police** revient à la dernière valeur valide.

Si une application tente de définir la taille de police par programmation sur une valeur en dehors de la plage valide, l’infrastructure du ruban invalide toutes les propriétés de police et définit les contrôles de police (**taille de police** et **type de police**) à vide ou à leur état par défaut, le cas échéant.

La valeur par défaut est 0.

La valeur 0 indique qu’aucune taille de point unique n’est sélectionnée (aucun texte, ou une série de texte de taille hétérogène, est sélectionnée).

Un utilisateur ne peut pas définir la valeur 0 pour le contrôle de la taille de la **police** .

En dehors de 0, les valeurs valides pour la plage de taille FontProperties de l’interface utilisateur est \_ \_ \_ comprise entre *MinimumFontSize* et *MaximumFontSize* comme déclaré dans le balisage de [contrôle de police](windowsribbon-controls-fontcontrol.md) .

> [!Note]  
> Le contrôle de **taille de police** est défini sur vide lorsque la taille de police est définie par programme sur 0, par exemple lorsqu’une exécution de texte de taille hétérogène est mise en surbrillance.

 

Lorsqu’une exécution de texte de taille hétérogène est sélectionnée, l’application doit interroger l' [interface utilisateur \_ \_ FontProperties \_](windowsribbon-reference-properties-uipkey-fontproperties-deltasize.md) de l’IU pour capturer les commandes **agrandir la police** et **réduire la police** .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Propriétés du contrôle de police](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[Contrôle de police](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 




