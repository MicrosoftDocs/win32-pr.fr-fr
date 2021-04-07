---
title: Élément VerticalMenuLayout
description: Représente une disposition verticale pour les éléments d’une galerie.
ms.assetid: 4124c639-c078-4eb0-9d36-37d1ffcebac0
keywords:
- Ruban des fenêtres d’élément VerticalMenuLayout
topic_type:
- apiref
api_name:
- VerticalMenuLayout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7fb848edcc8ab5ddff1405f35d5abd414ae40d15
ms.sourcegitcommit: 2387bc0339a1764564c1509e72ed5f2e8ae60b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/30/2020
ms.locfileid: "103724341"
---
# <a name="verticalmenulayout-element"></a>Élément VerticalMenuLayout

Représente une disposition verticale pour les éléments d’une galerie.

## <a name="usage"></a>Utilisation

``` syntax
<VerticalMenuLayout
  Rows = "xs:integer"
  IsMultipleHighlightingEnabled = "xs:boolean"
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
<td><strong>Manipulation</strong><br/></td>
<td>xs:string<br/></td>
<td>Non<br/></td>
<td>Une poignée de redimensionnement attachée à la liste déroulante de la Galerie. <br/> <img src="images/controls/gripper.png" alt="Screen shot of a vertical gripper." /><br/> Limité à l’une des valeurs suivantes :<br/> <br/>
<dt><span></span><span></span><strong></strong> None<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Barr<br/> </dt> <dd> Par défaut. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>IsMultipleHighlightingEnabled</strong><br/></td>
<td>xs:boolean<br/></td>
<td>Non<br/></td>
<td><strong>Windows 8 et versions ultérieures</strong><br/> Met en surbrillance tous les éléments de la liste jusqu’à l’élément MouseOver actuel (au lieu de l’élément MouseOver uniquement), et y compris celui-ci. Généralement utilisé pour plusieurs fonctionnalités d' <strong>annulation</strong> et de <strong>rétablissement</strong> .<br/> <br/>
<dt><span></span><span></span><strong></strong> :<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> fausses<br/> </dt> <dd> Par défaut. <br/> </dd> </dl></td>
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

L’élément **VerticalMenuLayout** ou [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md) doit se produire une seule fois pour chaque élément [**DropDownGallery. MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md), [**InRibbonGallery. MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md)ou [**SplitButtonGallery. MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md) .

## <a name="examples"></a>Exemples

L’exemple suivant illustre le balisage de base pour un élément **VerticalMenuLayout** .

Cette section de code montre les déclarations de contrôle [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) .


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



## <a name="element-information"></a>Informations sur les éléments



|                                     |           |
|-------------------------------------|-----------|
| Système minimal pris en charge<br/> | Windows 7 |
| Peut être vide                        | Oui       |



 

 





