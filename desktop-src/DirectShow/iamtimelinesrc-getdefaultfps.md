---
description: La méthode GetDefaultFPS récupère la fréquence d’images par défaut de l’objet source. Le moteur de rendu utilise cette valeur s’il ne parvient pas à déterminer la fréquence d’images à partir de la source d’origine.
ms.assetid: c167cd85-e9bb-46ff-9b35-c88898a6c5a3
title: 'IAMTimelineSrc :: GetDefaultFPS, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 92154a4c97c46307a764a7dba22ff2e003621db59cdb962ff025635022a5384b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131209"
---
# <a name="iamtimelinesrcgetdefaultfps-method"></a>IAMTimelineSrc :: GetDefaultFPS, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `GetDefaultFPS` méthode récupère la fréquence d’images par défaut de l’objet source. Le moteur de rendu utilise cette valeur s’il ne parvient pas à déterminer la fréquence d’images à partir de la source d’origine.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetDefaultFPS(
   double *pFPS
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFPS* 
</dt> <dd>

Reçoit la fréquence d’images par défaut, en images par seconde.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

La fréquence d’images par défaut n’est pas requise si le format de fichier spécifie la fréquence d’images. C’est le cas pour les formats audio et vidéo.

Si la source est une image bitmap ou JPEG, le moteur de rendu l’utilise comme première image dans une séquence de bitmaps indépendantes du périphérique (DIB, Device-Independent Bitmap), avec une fréquence d’images égale à la fréquence d’images par défaut. Pour afficher une image statique plutôt qu’une séquence DIB, définissez la fréquence d’images par défaut sur 0.

Si la source est une image GIF, ne définissez pas la fréquence d’images. Pour les images GIF animées, le fichier GIF spécifie le délai entre chaque image.

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

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

 

 




