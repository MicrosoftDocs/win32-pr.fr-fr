---
title: Command. KeyTip, propriété
description: Représente la touche d’interfaut pour un contrôle.
ms.assetid: 214f69ae-dd35-4abf-b294-d898d7802aa6
keywords:
- Propriété Command. KeyTip Windows, ruban
topic_type:
- apiref
api_name:
- Command.Keytip
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab16b9b8e52094d6cdc85890dfc1cf8af63942c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106518107"
---
# <a name="commandkeytip-property"></a>Command. KeyTip, propriété

Représente la touche d’interfaut pour un contrôle.

## <a name="usage"></a>Utilisation

``` syntax
<Command.Keytip>
  child elements
</Command.Keytip>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants



| Élément                                                   | Description                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [**String**](windowsribbon-element-string.md)<br/> | Peut se produire au plus une fois<br/> <br/> |



## <a name="parent-elements"></a>Éléments parents



| Élément                                                     |
|-------------------------------------------------------------|
| [**Commande**](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a>Notes

Optionnel.

Peut se produire au plus une fois pour chaque élément de [**commande**](windowsribbon-element-command.md) .

**Command. KeyTip** peut contenir une valeur de type *XS : String* limitée à toute séquence de caractères Unicode, y compris un espace blanc.

Une **commande. KeyTip** peut commencer par un nombre uniquement lorsqu’elle est associée à un contrôle dans un [onglet](windowsribbon-controls-tab.md) ou la [barre d’outils accès rapide](windowsribbon-controls-quickaccesstoolbar.md).

Pour afficher les touches d’affichage qui sont valides pour l’état actuel du ruban, maintenez la touche ALT enfoncée. La capture d’écran suivante montre les info-bulles initiales qui s’affichent dans Microsoft Paint pour Windows 7. Une fois qu’un KeyTip de premier niveau a été sélectionné, seules les touches de deuxième niveau sont affichées.

![touches accélératrices de premier niveau dans Microsoft Paint pour Windows 7](images/properties/ui-pkey-label-keytips.png)

**Command. KeyTip** agit comme touche de raccourci pour une commande, sauf si cette commande est exposée par le biais d’un élément de menu. Dans ce cas, le Framework ignore la valeur **Command. KeyTip** et utilise à la place un caractère précédé d’un signe & comme spécifié par [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) ou [l' \_ \_ étiquette de l’interface utilisateur](windowsribbon-reference-properties-uipkey-label.md). Si aucune esperluette n’est spécifiée par la **commande. LabelTitle** ou l' \_ \_ étiquette de nom de l’interface utilisateur, aucune touche d’accès ou touche d’accès rapide n’est exposée.

Si aucune valeur n’est fournie pour **Command. KeyTip**, l’élément enfant [**String**](windowsribbon-element-string.md) est requis.

> [!Note]  
> Si **Command. KeyTip** contient à la fois une valeur et un élément enfant de [**chaîne**](windowsribbon-element-string.md) , la **chaîne** est prioritaire.

 

Par défaut, le Framework utilise les lettres suivantes pour générer automatiquement des touches d’info-bulle :

-   **F** est assigné au menu de l' [application](windowsribbon-controls-applicationmenu.md).
-   **Y** est assigné à toute commande qui n’a pas de KeyTip spécifié par l’application.
-   **Z** est assigné à chaque contrôle de [groupe](windowsribbon-controls-group.md) et ne peut pas être personnalisé. Un KeyTip de groupe s’affiche uniquement lorsque le [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) du contrôle spécifie une option de taille de **menu contextuel** . Pour plus d’informations, consultez [Personnalisation d’un ruban à l’aide de définitions de taille et de stratégies de mise à l’échelle](windowsribbon-templates.md).

> [!Note]  
> Aucune de ces lettres n’est réservée par l’infrastructure. Chaque peut être assigné à une ou plusieurs commandes selon les besoins.

 

Le Framework résout les conflits KeyTip des manières suivantes :

-   Si un ou plusieurs contrôles [onglet](windowsribbon-controls-tab.md) sont associés au même KeyTip, un nombre est ajouté à chaque KeyTip, en commençant à 1, et en accroissant de façon séquentielle (2,3,...) pour chaque contrôle dans l’ordre de déclaration. Si des contrôles onglet se voient attribuer la lettre F comme touche d’activation, le menu de l' [application](windowsribbon-controls-applicationmenu.md) reçoit la touche F1 avec les touches accélératrices restantes ajustées comme décrit.
-   Lorsqu’il est associé à un contrôle unique dans un [onglet](windowsribbon-controls-tab.md), le KeyTip F est valide à la fois pour le menu de l' [application](windowsribbon-controls-applicationmenu.md)et le contrôle. Le menu d’application par défaut KeyTip n’est pas modifié, mais la priorité est donnée au contrôle sous l’onglet actif.
-   Si un ou plusieurs contrôles d’un [onglet](windowsribbon-controls-tab.md) sont associés au même KeyTip, le Framework refactorise automatiquement les touches d’info-bulle de ces contrôles, comme décrit précédemment.

> [!Note]  
> Une légère variation de la couleur du texte est utilisée pour mettre en surbrillance les touches réfactorisées dans une implémentation de ruban standard. Pour une implémentation de ruban non standard où la couleur du ruban a été personnalisée, ce comportement de l’infrastructure est substitué et toutes les touches sont affichées avec la même couleur de texte. Pour plus d’informations, consultez [Personnalisation des couleurs du ruban](ribbon-color.md).

 

La longueur maximale est illimitée.

## <a name="examples"></a>Exemples

L’exemple suivant illustre le balisage pour un élément [**Command**](windowsribbon-element-command.md) avec une déclaration **Command. KeyTip** .


```XML
<Command>
  <Command.Name>cmdSave</Command.Name>
  <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
  <Command.Comment>Save</Command.Comment>
  <Command.Id>25003</Command.Id>
  <Command.LabelTitle>
    <String>
      <String.Content>Label for Save</String.Content>
      <String.Id>59999</String.Id>
      <String.Symbol>strSave</String.Symbol>
    </String>
  </Command.LabelTitle>
  <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
  <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
  <Command.Keytip>s1</Command.Keytip>
</Command>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[KeyTip de l’interface utilisateur \_ \_](windowsribbon-reference-properties-uipkey-keytip.md)
</dt> </dl>

 

 





