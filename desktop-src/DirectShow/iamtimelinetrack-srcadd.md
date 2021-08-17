---
description: La méthode SrcAdd ajoute une source à la piste.
ms.assetid: 71c62e92-02d6-4c6f-8121-2052d6cc832c
title: 'IAMTimelineTrack :: SrcAdd, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.SrcAdd
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e705f840a073ee6796776f6f68c7b57df0bd972facf8f7a586792519735bfb3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117998749"
---
# <a name="iamtimelinetracksrcadd-method"></a>IAMTimelineTrack :: SrcAdd, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `SrcAdd` méthode ajoute une source à la piste.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SrcAdd(
   IAMTimelineObj *pSrc
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSrc* 
</dt> <dd>

Pointeur vers l’interface [**IAMTimelineObj**](iamtimelineobj.md) de l’objet source.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK en cas de réussite. Retourne E \_ nointerface si l’objet n’est pas un objet source. Sinon, retourne une valeur **HRESULT** indiquant la cause de l’erreur.

## <a name="remarks"></a>Remarques

Définissez les heures de début et de fin de la source avant d’appeler cette méthode. (Appelez [**IAMTimelineObj :: SetStartStop**](iamtimelineobj-setstartstop.md).)

Actuellement, les ne peuvent pas afficher simultanément plus de 75 sources compressées avec des codecs VCM (Video Compression Manager). En outre, si le projet dans son ensemble contient plus de 75 de telles sources, vous devez utiliser la reconnexion dynamique ou DES ne peuvent pas afficher un aperçu du projet. Pour plus d’informations, consultez [**IRenderEngine :: SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).

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

[**Interface IAMTimelineTrack**](iamtimelinetrack.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




