---
title: Élément FlowMenuLayout
description: Représente une disposition horizontale avec des sauts de ligne pour les éléments d’une galerie.
ms.assetid: 40c3a2e1-e58a-4d34-a237-b1bea116c82e
keywords:
- Ruban des fenêtres d’élément FlowMenuLayout
topic_type:
- apiref
api_name:
- FlowMenuLayout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ec9690dd9839755a90abee4c8649c32eae4db6b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106544150"
---
# <a name="flowmenulayout-element"></a>Élément FlowMenuLayout

Représente une disposition horizontale avec des sauts de ligne pour les éléments d’une galerie.

## <a name="usage"></a>Utilisation

``` syntax
<FlowMenuLayout
  Rows = "xs:integer"
  Columns = "xs:integer"
  Gripper = "xs:string"/>
```

## <a name="attributes"></a>Attributs



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
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
<td><strong>Colonnes</strong><br/></td>
<td>xs:integer<br/></td>
<td>Non<br/></td>
<td>Spécifie le nombre d’éléments à afficher sur une seule ligne.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS : Integer)<br/> </dt> <dd> Entier positif ou négatif. <br/> La valeur par défaut est <strong>2</strong>. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Manipulation</strong><br/></td>
<td>xs:string<br/></td>
<td>Non<br/></td>
<td>Une poignée de redimensionnement attachée à la liste déroulante de la Galerie. <br/> <img src="images/controls/gripper.png" alt="Screen shot of a vertical gripper." /><br/> Limité à l’une des valeurs suivantes :<br/> <br/>
<dt><span></span><span></span><strong></strong> None<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Barr<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Virage<br/> </dt> <dd> Par défaut. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Lignes</strong><br/></td>
<td>xs:integer<br/></td>
<td>Non<br/></td>
<td>Spécifie le nombre de lignes d’élément à afficher sans défilement. <br/> <br/>
<dt><span></span><span></span><strong></strong> (XS : Integer)<br/> </dt> <dd> Entier positif ou négatif. <br/> La valeur par défaut est <strong>-1</strong> qui spécifie d’afficher autant de lignes d’éléments que possible.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Éléments enfants

Il n’y a pas d’éléments enfants.

## <a name="parent-elements"></a>Éléments parents



| Élément                                                                                                 |
|---------------------------------------------------------------------------------------------------------|
| [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md)<br/>       |
| [**InRibbonGallery.MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md)<br/>       |
| [**SplitButtonGallery.MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md)<br/> |



## <a name="remarks"></a>Notes

Obligatoire.

L’élément [**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) ou **FlowMenuLayout** doit se produire une seule fois pour chaque élément [**DropDownGallery. MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md), [**InRibbonGallery. MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md)ou [**SplitButtonGallery. MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md) .

Les éléments sont organisés en fonction des propriétés de saut de ligne inhérentes aux attributs de *ligne* et de *colonne* . Lorsque le contenu dépasse la longueur d’une seule ligne, le menu coupe les lignes, encapsule les lignes et aligne le contenu de manière appropriée.

## <a name="examples"></a>Exemples

L’exemple suivant illustre le balisage de base pour [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).

Cette section de code illustre la déclaration de contrôle [**DropDownGallery. MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md) avec une spécification **FlowMenuLayout** .


```XML
<!-- DropDownGallery -->
<Group CommandName="cmdDropDownGalleryGroup">
  <DropDownGallery CommandName="cmdDropDownGallery"
                   TextPosition="Hide"
                   Type="Commands"
                   ItemHeight="32"
                   ItemWidth="32">
    <DropDownGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </DropDownGallery.MenuLayout>
    <DropDownGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
       </MenuGroup>
       <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </DropDownGallery.MenuGroups>
  </DropDownGallery>
</Group>
```



## <a name="element-information"></a>Informations sur les éléments



|                                     |           |
|-------------------------------------|-----------|
| Système minimal pris en charge<br/> | Windows 7 |
| Peut être vide                        | Oui       |



 

 





