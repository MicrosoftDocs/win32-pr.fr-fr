---
description: L’interface IDxtCompositor définit les propriétés de la transition du compositeur. Cette interface est utilisée en interne par les services de modification DirectShow (DES) lors du rendu de la transition de compositeur.
ms.assetid: 519f1e00-4b67-4014-906b-043f2478baa7
title: Interface IDxtCompositor (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c2e19f555fe01cbec3763bc1dc76d11aeb5f5ecb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521688"
---
# <a name="idxtcompositor-interface"></a>Interface IDxtCompositor

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

L' `IDxtCompositor` interface définit les propriétés de la transition du [compositeur](compositor-transition.md) .

Cette interface est utilisée en interne par les services de modification DirectShow (DES) lors du rendu de la transition de compositeur. Les applications DES n’ont pas besoin d’utiliser cette interface. Pour définir les propriétés d’une transition dans DES, utilisez l’interface [**IPropertySetter**](ipropertysetter.md) .

La transition de compositeur composite une image de premier plan sur une image d’arrière-plan. Le *rectangle source* définit la section de l’image de premier plan qui est composite. Le *rectangle de destination* définit la section de l’image d’arrière-plan qui reçoit l’image de premier plan. Le diagramme suivant illustre ces rectangles.

![Propriétés de transition du compositeur](images/compmeasure.png)

## <a name="members"></a>Membres

L’interface **IDxtCompositor** hérite de **IDXEffect**. **IDxtCompositor** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IDxtCompositor** possède ces méthodes.



| Méthode                                                   | Description                                                         |
|:---------------------------------------------------------|:--------------------------------------------------------------------|
| [**afficher la \_ hauteur**](idxtcompositor-get-height.md)         | Récupère la hauteur du rectangle cible.<br/>            |
| [**Obtient les \_ offsets**](idxtcompositor-get-offsetx.md)       | Récupère le décalage horizontal du rectangle cible.<br/> |
| [**recevoir un \_ décalage**](idxtcompositor-get-offsety.md)       | Récupère le décalage vertical du rectangle cible.<br/>   |
| [**Obtient \_ SrcHeight**](idxtcompositor-get-srcheight.md)   | Récupère la hauteur du rectangle source.<br/>            |
| [**Obtient \_ SrcOffsetX**](idxtcompositor-get-srcoffsetx.md) | Récupère le décalage horizontal du rectangle source.<br/> |
| [**Obtient \_ SrcOffsetY**](idxtcompositor-get-srcoffsety.md) | Récupère le décalage vertical du rectangle source.<br/>   |
| [**Obtient \_ SrcWidth**](idxtcompositor-get-srcwidth.md)     | Récupère la largeur du rectangle source.<br/>             |
| [**afficher la \_ largeur**](idxtcompositor-get-width.md)           | Récupère la largeur du rectangle cible.<br/>             |
| [**Placer la \_ hauteur**](idxtcompositor-put-height.md)         | Spécifie la hauteur du rectangle cible.<br/>            |
| [**put \_ OffsetX**](idxtcompositor-put-offsetx.md)       | Spécifie le décalage horizontal du rectangle cible.<br/> |
| [**placer un \_ décalage**](idxtcompositor-put-offsety.md)       | Spécifie le décalage vertical du rectangle cible.<br/>   |
| [**put \_ SrcHeight**](idxtcompositor-put-srcheight.md)   | Spécifie la hauteur du rectangle source.<br/>            |
| [**put \_ SrcOffsetX**](idxtcompositor-put-srcoffsetx.md) | Spécifie le décalage horizontal du rectangle source.<br/> |
| [**put \_ SrcOffsetY**](idxtcompositor-put-srcoffsety.md) | Spécifie le décalage vertical du rectangle source.<br/>   |
| [**put \_ SrcWidth**](idxtcompositor-put-srcwidth.md)     | Spécifie la largeur du rectangle source.<br/>             |
| [**mettre la \_ largeur**](idxtcompositor-put-width.md)           | Spécifie la largeur du rectangle cible.<br/>             |



 

## <a name="remarks"></a>Notes

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 




