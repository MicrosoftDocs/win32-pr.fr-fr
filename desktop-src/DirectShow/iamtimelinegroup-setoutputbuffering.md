---
description: La méthode SetOutputBuffering spécifie le nombre d’images rendues à l’avance pendant la version préliminaire.
ms.assetid: 6e69b196-a6ce-4ce0-8c48-58b1738fb197
title: 'IAMTimelineGroup :: SetOutputBuffering, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetOutputBuffering
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8187918a4f6d04df9c8c0eaff387a092f18181071ce6ba41c83de44fcb095bbe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915189"
---
# <a name="iamtimelinegroupsetoutputbuffering-method"></a>IAMTimelineGroup :: SetOutputBuffering, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `SetOutputBuffering` méthode spécifie le nombre d’images rendues à l’avance pendant la version préliminaire.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetOutputBuffering(
  [in] int nBuffer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nBuffer* \[ dans\]
</dt> <dd>

Nombre d’images à mettre en mémoire tampon pendant la version préliminaire. Doit être supérieur ou égal à deux.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Une mémoire tampon plus grande requiert plus de mémoire, mais peut entraîner un aperçu plus lisse, en particulier lors d’effets ou de transitions qui nécessitent plus de temps pour le rendu. La mémoire tampon par défaut est de 30 frames.

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

[**Interface IAMTimelineGroup**](iamtimelinegroup.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




