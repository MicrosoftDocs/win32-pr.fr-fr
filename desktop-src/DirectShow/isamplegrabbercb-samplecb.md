---
description: La méthode SampleCB est une méthode de rappel qui reçoit un pointeur vers l’exemple de média.
ms.assetid: e919b694-75cb-48c6-8427-5a7a886e0ff3
title: 'ISampleGrabberCB :: SampleCB, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabberCB.SampleCB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e98377050ec98cdccaedd54119afb6cdaccbaee56256f1406bb190d3ea875bb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817511"
---
# <a name="isamplegrabbercbsamplecb-method"></a>ISampleGrabberCB :: SampleCB, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée des futures versions de Windows.\]

 

La `SampleCB` méthode est une méthode de rappel qui reçoit un pointeur vers l’exemple de média.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SampleCB(
   double       SampleTime,
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*SampleTime* 
</dt> <dd>

Heure de début de l’échantillon, en secondes.

</dd> <dt>

*pSample* 
</dt> <dd>

Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK en cas de réussite, ou un code d’erreur **HRESULT** dans le cas contraire.

## <a name="remarks"></a>Remarques

Pour configurer le rappel, appelez [**ISampleGrabber :: SetCallback**](isamplegrabber-setcallback.md).

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

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> <dt>

[**Interface ISampleGrabberCB**](isamplegrabbercb.md)
</dt> </dl>

 

 




