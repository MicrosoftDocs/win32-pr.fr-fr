---
description: La méthode SetCallback spécifie une méthode de rappel à appeler sur les exemples entrants.
ms.assetid: b84d3f52-b986-492a-a8b9-1d98618dcdd3
title: 'ISampleGrabber :: SetCallback, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetCallback
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 46e0565c314bab86967ee0d5dabee6ba449a87dd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126857470"
---
# <a name="isamplegrabbersetcallback-method"></a>ISampleGrabber :: SetCallback, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La méthode **SetCallback** spécifie une méthode de rappel à appeler sur les exemples entrants.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetCallback(
   ISampleGrabberCB *pCallback,
   long             WhichMethodToCallback
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pCallback* 
</dt> <dd>

Pointeur vers une interface [**ISampleGrabberCB**](isamplegrabbercb.md) contenant la méthode de rappel, ou **null** pour annuler le rappel.

</dd> <dt>

*WhichMethodToCallback* 
</dt> <dd>

Index qui spécifie la méthode de rappel. Il doit s’agir de l’une des valeurs suivantes.



| Valeur | Description                                                                                                                                                                                     |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | L’exemple de filtre d’accrochage appelle la méthode [**ISampleGrabberCB :: SampleCB**](isamplegrabbercb-samplecb.md) . Cette méthode reçoit un pointeur [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) .               |
| 1     | L’exemple de filtre d’accrochage appelle la méthode [**ISampleGrabberCB :: BufferCB**](isamplegrabbercb-buffercb.md) . Cette méthode reçoit un pointeur vers la mémoire tampon contenue dans l’exemple de média. |



 

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Le thread de traitement des données se bloque jusqu’à ce que la méthode de rappel retourne. Si le rappel ne retourne pas rapidement, il peut interférer avec la lecture.

Le filtre n’appelle pas la fonction de rappel pour les exemples de préroll, ou pour les exemples dans lesquels le membre **dwStreamId** de la structure de [**\_ \_ Propriétés am SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) est autre chose que le \_ média de flux \_ .

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Utilisation de l’exemple d’accrochage](using-the-sample-grabber.md)
</dt> <dt>

[**Interface ISampleGrabber**](isamplegrabber.md)
</dt> </dl>

 

 




