---
description: L’interface IExtender fournit un ensemble de propriétés de base qui sont ajoutées à l’interface d’un contrôle. Les programmeurs peuvent utiliser ces propriétés comme s’ils faisaient partie du contrôle.
ms.assetid: 901873bd-af6a-415e-865f-21769367c99f
title: Interface IExtender
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IExtender
- IExtender.Align
- IExtender.get_Align
- IExtender.put_Align
- IExtender.Enabled
- IExtender.get_Enabled
- IExtender.put_Enabled
- IExtender.Height
- IExtender.get_Height
- IExtender.put_Height
- IExtender.Left
- IExtender.get_Left
- IExtender.put_Left
- IExtender.TabStop
- IExtender.get_TabStop
- IExtender.put_TabStop
- IExtender.Top
- IExtender.get_Top
- IExtender.put_Top
- IExtender.Visible
- IExtender.get_Visible
- IExtender.put_Visible
- IExtender.Width
- IExtender.get_Width
- IExtender.put_Width
- IExtender.Name
- IExtender.get_Name
- IExtender.Parent
- IExtender.get_Parent
- IExtender.Hwnd
- IExtender.get_Hwnd
- IExtender.Container
- IExtender.get_Container
api_type:
- COM
api_location:
- Ole2disp.dll
- Oleaut32.dll
ms.openlocfilehash: a341f5d8a0ec554f008232f44156486df83d0fd8
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625110"
---
# <a name="iextender-interface"></a>Interface IExtender

L’interface **IExtender** fournit un ensemble de propriétés de base qui sont ajoutées à l’interface d’un contrôle. Les programmeurs peuvent utiliser ces propriétés comme s’ils faisaient partie du contrôle.

## <a name="members"></a>Membres

L’interface **IExtender** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IExtender** a également les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **IExtender** possède ces méthodes.



| Méthode                         | Description                                    |
|:-------------------------------|:-----------------------------------------------|
| [**Déplacer**](iextender-move.md) | Déplace un MDIForm, un formulaire ou un contrôle.<br/> |



 

### <a name="properties"></a>Propriétés

L’interface **IExtender** possède les propriétés suivantes.



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th >Propriété</th>
<th >Type d’accès</th>
<th >Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td >Aligner<br/></td>
<td >Lecture/écriture<br/></td>
<td >Retourne ou définit une valeur qui détermine si un objet est affiché dans n’importe quelle taille sur un formulaire ou s’il est affiché en haut, en bas, à gauche ou à droite du formulaire et s’il est automatiquement dimensionné pour s’ajuster à la largeur du formulaire.<br/> 
<table>
<thead>
<tr class="header">
<th>Constante</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>vbAlignNone 0</td>
<td>(Par défaut dans un formulaire non-MDI) None : la taille et l’emplacement peuvent être définis au moment de la conception ou dans le code. Le paramètre est ignoré si l’objet se trouve sur un formulaire MDI.</td>
</tr>
<tr class="even">
<td>vbAlignTop 1</td>
<td>(Par défaut dans un formulaire MDI) Top : l’objet se trouve en haut du formulaire et sa largeur est égale au paramètre de propriété ScaleWidth du formulaire.</td>
</tr>
<tr class="odd">
<td>vbAlignBottom 2</td>
<td>Bas : l’objet se trouve au bas du formulaire et sa largeur est égale au paramètre de propriété ScaleWidth du formulaire.</td>
</tr>
<tr class="even">
<td>vbAlignLeft 3</td>
<td>Left : l’objet se trouve à gauche du formulaire et sa largeur est égale au paramètre de propriété ScaleWidth du formulaire.</td>
</tr>
<tr class="odd">
<td>vbAlignRight 4</td>
<td>Right : l’objet se trouve à droite du formulaire et sa largeur est égale au paramètre de propriété ScaleWidth du formulaire.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><p>Conteneur</p></td>
<td ><p>Lecture seule</p></td>
<td ><p>Retourne le conteneur d’un contrôle sur un formulaire.</p></td>
</tr>
<tr class="odd">
<td ><p>Activé</p></td>
<td ><p>Lecture/écriture</p></td>
<td ><p>Retourne ou définit une valeur qui détermine si un formulaire ou un contrôle peut répondre à des événements générés par l’utilisateur.</p></td>
</tr>
<tr class="even">
<td ><p>Hauteur</p></td>
<td ><p>Lecture/écriture</p></td>
<td ><p>Retourne ou définit la hauteur d’un objet.</p></td>
</tr>
<tr class="odd">
<td ><p>HWND</p></td>
<td ><p>Lecture seule</p></td>
<td ><p>Retourne un handle pour un formulaire ou un contrôle.</p></td>
</tr>
<tr class="even">
<td ><p>Gauche</p></td>
<td ><p>Lecture/écriture</p></td>
<td ><p>Retourne ou définit la distance entre le bord interne gauche d’un objet et le bord gauche de son conteneur.</p></td>
</tr>
<tr class="odd">
<td ><p>Name</p></td>
<td ><p>Lecture seule</p></td>
<td ><p>Retourne le nom utilisé dans le code pour identifier un objet de formulaire, de contrôle ou d’accès aux données.</p></td>
</tr>
<tr class="even">
<td ><p>Parent</p></td>
<td ><p>Lecture seule</p></td>
<td ><p>Retourne le formulaire, l’objet ou la collection qui contient un contrôle ou un autre objet ou une autre collection.</p></td>
</tr>
<tr class="odd">
<td ><p>Tabulation</p></td>
<td ><p>Lecture/écriture</p></td>
<td ><p>Retourne ou définit une valeur qui indique si un utilisateur peut utiliser la touche <strong>Tab</strong> pour attribuer le focus à un objet.</p></td>
</tr>
<tr class="even">
<td ><p>Haut</p></td>
<td ><p>Lecture/écriture</p></td>
<td ><p>Retourne ou définit la distance entre le bord interne supérieur d’un objet et le bord supérieur de son conteneur.</p></td>
</tr>
<tr class="odd">
<td ><p>Visible</p></td>
<td ><p>Lecture/écriture</p></td>
<td ><p>Retourne ou définit une valeur qui indique si un objet est visible ou masqué.</p></td>
</tr>
<tr class="even">
<td ><p>Largeur</p></td>
<td ><p>Lecture/écriture</p></td>
<td ><p>Retourne ou définit la largeur d’un objet.</p></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ole2disp.dll ; </dt> <dt>Oleaut32.dll</dt> </dl> |



 

 
