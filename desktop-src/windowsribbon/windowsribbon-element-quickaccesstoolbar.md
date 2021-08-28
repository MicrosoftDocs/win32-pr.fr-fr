---
title: Élément QuickAccessToolbar
description: Représente la barre d’outils accès rapide (QAT), une petite barre d’outils qui affiche des raccourcis vers les commandes du ruban.
ms.assetid: 59aa35c3-a844-46b3-b066-c9a321fb0891
keywords:
- élément QuickAccessToolbar Windows ruban
topic_type:
- apiref
api_name:
- QuickAccessToolbar
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fa9d097823d049d145c25d1027bdb5a67d688692
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624165"
---
# <a name="quickaccesstoolbar-element"></a>Élément QuickAccessToolbar

Représente la [barre d’outils accès rapide (qat)](windowsribbon-controls-quickaccesstoolbar.md), une petite barre d’outils qui affiche des raccourcis vers les commandes du ruban.

## <a name="usage"></a>Utilisation

``` syntax
<QuickAccessToolbar
  CommandName = "xs:positiveInteger or xs:string"
  CustomizeCommandName = "xs:positiveInteger or xs:string">
  child elements
</QuickAccessToolbar>
```

## <a name="attributes"></a>Attributs



<table>
<colgroup>
<col  />
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>Type</th>
<th>Obligatoire</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>CommandName</strong><br/></td>
<td>XS : positiveInteger ou XS : String<br/></td>
<td>No<br/></td>
<td>Associe l’élément à une <a href="windowsribbon-element-command.md"><strong>commande</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS : positiveInteger ou XS : String)<br/> </dt> <dd> Chaîne, valeur entière comprise entre 2 et 59999, inclusive, ou valeur hexadécimale comprise entre 0X2 et 0xea5f inclus. <br/> La valeur doit être unique dans le document XML du ruban. <br/> Longueur maximale : 100 caractères. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CustomizeCommandName</strong><br/></td>
<td>XS : positiveInteger ou XS : String<br/></td>
<td>No<br/></td>
<td>Insère un élément de commande supplémentaire dans le menu QAT.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS : positiveInteger ou XS : String)<br/> </dt> <dd> <img src="images/markup/qat-customizecommandname.png" alt="Screen shot of a QAT menu with the More commands... Command item." /><br/> Chaîne, valeur entière comprise entre 2 et 59999, inclusive, ou valeur hexadécimale comprise entre 0X2 et 0xea5f inclus. <br/> La valeur doit être unique dans le document XML du ruban. <br/> Longueur maximale : 100 caractères. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Éléments enfants



| Élément                                                                                                                   | Description                                   |
|---------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [**QuickAccessToolbar.ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> | Peut se produire au plus une fois<br/> <br/> |



## <a name="parent-elements"></a>Éléments parents



| Élément                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [**Ruban. QuickAccessToolbar**](windowsribbon-element-ribbon-quickaccesstoolbar.md)<br/> |



## <a name="remarks"></a>Remarques

Obligatoire.

Doit se produire une seule fois pour chaque [**ruban. QuickAccessToolbar**](windowsribbon-element-ribbon-quickaccesstoolbar.md).

Les éléments du QAT peuvent être ajoutés ou supprimés au moment de l’exécution.

Pour garantir la cohérence entre les applications du ruban, il est recommandé que le gestionnaire de commandes *CustomizeCommandName* lance une boîte de dialogue de personnalisation qat.

## <a name="examples"></a>Exemples

L’exemple suivant illustre le balisage de base pour **QuickAccessToolbar**.

Cette section de code affiche la déclaration de commande **QuickAccessToolbar** .


```XML
<Command Name="cmdQAT"
         Symbol="ID_QAT"
         Id="40000"/>
<Command Name="cmdCustomizeQAT"
         Symbol="ID_CUSTOM_QAT"
         Id="40001"/>
```



Cette section de code illustre la déclaration de contrôle **QuickAccessToolbar** .


```XML
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar CommandName="cmdQAT"
                            CustomizeCommandName="cmdCustomizeQAT">
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdButton1"/>
            <ToggleButton CommandName="cmdMinimize"
                          ApplicationDefaults.IsChecked="false"/>
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
```



## <a name="element-information"></a>Informations sur les éléments

* **système minimal pris en charge**: Windows 7
* **Peut être vide**: non



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Contrôle de barre d’outils accès rapide](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 





