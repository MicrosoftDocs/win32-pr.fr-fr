---
description: La méthode SetDefaultFPS définit la fréquence d’images par défaut de l’objet source.
ms.assetid: ea93acde-3e05-43d5-8130-9ab2ee841b4e
title: 'IAMTimelineSrc :: SetDefaultFPS, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fd15f0606b1a4e4ee1aacdb1b3f56d63a024708b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534786"
---
# <a name="iamtimelinesrcsetdefaultfps-method"></a>IAMTimelineSrc :: SetDefaultFPS, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La `SetDefaultFPS` méthode définit la fréquence d’images par défaut de l’objet source.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetDefaultFPS(
   double FPS
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*i/s* 
</dt> <dd>

Fréquence d’images par défaut, en images par seconde.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK en cas de réussite, ou E \_ INVALIDARG si la fréquence d’images spécifiée est inférieure à zéro.

## <a name="remarks"></a>Notes

Le moteur de rendu utilise cette valeur s’il ne parvient pas à déterminer la fréquence d’images à partir du fichier source d’origine.

Appelez cette méthode uniquement pour les fichiers sources sans fréquence d’images prédéfinie. Pour les fichiers bitmap et JPEG, la fréquence d’images par défaut est zéro, ce qui entraîne le rendu de la source sous la forme d’une image continue. Pour utiliser l’image comme première image dans une séquence DIB, définissez la fréquence d’images sur une valeur supérieure à zéro. Pour plus d’informations, consultez [utilisation des sources](working-with-sources.md).

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IAMTimelineSrc**](iamtimelinesrc.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




