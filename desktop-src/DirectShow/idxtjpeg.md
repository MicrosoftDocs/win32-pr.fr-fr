---
description: L’interface IDxtJpeg définit les propriétés de la transition de réinitialisation SMPTE. Cette interface est utilisée en interne par les services de modification DirectShow (DES) lors du rendu de la transition de réinitialisation SMPTE.
ms.assetid: ce1920d4-ebe5-42d1-a2eb-d71ddeaf14fe
title: Interface IDxtJpeg (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e9c32bee3f4041abaa9529036b7bc78250ac2487
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523973"
---
# <a name="idxtjpeg-interface"></a>Interface IDxtJpeg

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

L' `IDxtJpeg` interface définit les propriétés de la transition de [réinitialisation SMPTE](smpte-wipe-transition.md) .

Cette interface est utilisée en interne par les services de modification DirectShow (DES) lors du rendu de la transition de réinitialisation SMPTE. Les applications DES n’ont pas besoin d’utiliser cette interface. Pour définir les propriétés d’une transition dans DES, utilisez l’interface [**IPropertySetter**](ipropertysetter.md) .

## <a name="members"></a>Membres

L’interface **IDxtJpeg** hérite de **IDXEffect**. **IDxtJpeg** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IDxtJpeg** possède ces méthodes.



| Méthode                                                     | Description                                                                               |
|:-----------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**ApplyChanges**](idxtjpeg-applychanges.md)              | Applique toutes les propriétés qui ont été modifiées.<br/>                                      |
| [**Obtient la \_ CouleurBordure**](idxtjpeg-get-bordercolor.md)       | Récupère la couleur de la bordure autour des bords du motif de réinitialisation.<br/>        |
| [**Obtient \_ BorderSoftness**](idxtjpeg-get-bordersoftness.md) | Récupère la largeur de la zone floue autour des bords du motif de réinitialisation.<br/> |
| [**accéder à \_ BorderWidth**](idxtjpeg-get-borderwidth.md)       | Récupère la largeur de la bordure unie le long des bords du motif de réinitialisation.<br/>   |
| [**Obtient \_ MaskName**](idxtjpeg-get-maskname.md)             | Récupère le nom d’un fichier JPEG à utiliser comme masque de réinitialisation.<br/>                 |
| [**Obtient \_ MaskNum**](idxtjpeg-get-masknum.md)               | Récupère le code de réinitialisation SMPTE de la réinitialisation.<br/>                                     |
| [**Obtient les \_ offsets**](idxtjpeg-get-offsetx.md)               | Récupère le décalage horizontal de l’origine de la réinitialisation.<br/>                            |
| [**recevoir un \_ décalage**](idxtjpeg-get-offsety.md)               | Récupère le décalage vertical de l’origine de la réinitialisation.<br/>                              |
| [**Obtient \_ ReplicateX**](idxtjpeg-get-replicatex.md)         | Récupère le nombre de fois que le modèle de réinitialisation est répliqué horizontalement.<br/>     |
| [**être \_ répliqué**](idxtjpeg-get-replicatey.md)         | Récupère le nombre de fois où le modèle de réinitialisation est répliqué verticalement.<br/>       |
| [**récupération \_ ScaleX**](idxtjpeg-get-scalex.md)                 | Récupère la quantité d’étirement horizontal de la réinitialisation.<br/>              |
| [**faire \_ évoluer**](idxtjpeg-get-scaley.md)                 | Récupère la valeur de l’étirement vertical de la réinitialisation.<br/>                |
| [**LoadDefSettings**](idxtjpeg-loaddefsettings.md)        | Restaure les paramètres par défaut de la transition de réinitialisation.<br/>                          |
| [**Placer la \_ CouleurBordure**](idxtjpeg-put-bordercolor.md)       | Spécifie la couleur de la bordure autour des bords du motif de la réinitialisation.<br/>        |
| [**put \_ BorderSoftness**](idxtjpeg-put-bordersoftness.md) | Spécifie la largeur de la zone floue autour des bords du motif de réinitialisation.<br/> |
| [**placer \_ BorderWidth**](idxtjpeg-put-borderwidth.md)       | Spécifie la largeur de la bordure unie le long des bords du motif de réinitialisation.<br/>   |
| [**put \_ MaskName**](idxtjpeg-put-maskname.md)             | Spécifie le nom d’un fichier JPEG à utiliser comme masque de réinitialisation.<br/>                     |
| [**put \_ MaskNum**](idxtjpeg-put-masknum.md)               | Spécifie le code de réinitialisation SMPTE de la réinitialisation.<br/>                                     |
| [**put \_ OffsetX**](idxtjpeg-put-offsetx.md)               | Spécifie le décalage horizontal de l’origine de la réinitialisation.<br/>                            |
| [**placer un \_ décalage**](idxtjpeg-put-offsety.md)               | Spécifie le décalage vertical de l’origine de la réinitialisation.<br/>                              |
| [**put \_ ReplicateX**](idxtjpeg-put-replicatex.md)         | Spécifie le nombre de fois que le modèle de réinitialisation est répliqué horizontalement.<br/>     |
| [**mise en \_ réplique**](idxtjpeg-put-replicatey.md)         | Spécifie le nombre de fois que le modèle de réinitialisation est répliqué verticalement.<br/>       |
| [**placer \_ ScaleX**](idxtjpeg-put-scalex.md)                 | Spécifie la quantité d’étirement horizontal de la réinitialisation.<br/>              |
| [**mettre à l' \_ échelle**](idxtjpeg-put-scaley.md)                 | Spécifie la quantité d’étirement vertical de la réinitialisation.<br/>                |



 

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



 

 




