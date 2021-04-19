---
description: La méthode CheckStreamState détermine si un exemple de support doit être remis ou ignoré.
ms.assetid: 1533f4b9-e13e-458b-9614-96d733cef4ed
title: Méthode CBaseStreamControl. CheckStreamState (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.CheckStreamState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e469e288e853ca88a0cf15c209882a8114e33509
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523956"
---
# <a name="cbasestreamcontrolcheckstreamstate-method"></a>Méthode CBaseStreamControl. CheckStreamState

La `CheckStreamState` méthode détermine si un échantillon de média doit être remis ou ignoré.

## <a name="syntax"></a>Syntaxe


```C++
enum CheckStreamState(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSample* 
</dt> <dd>

Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs suivantes.



| Code de retour                                                                                       | Description                     |
|---------------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**FLUX \_ ignoré**</dt> </dl> | Ignorez cet exemple.<br/> |
| <dl> <dt>**flux \_ de flux**</dt> </dl>    | Fournissez cet exemple.<br/> |



 

## <a name="remarks"></a>Notes

Appelez cette méthode lorsque votre code confidentiel reçoit un exemple. Fournissez l’exemple uniquement si la valeur de retour est flux continu \_ . Si la valeur de retour est une annulation de flux \_ , ignorez l’exemple.

Si le code PIN ignore les exemples, il doit marquer l’exemple suivant qu’il remet comme discontinu, en appelant la méthode [**IMediaSample :: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) .

Si votre filtre implémente l’interface [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) pour compter le nombre de frames qu’il supprime, ne comptez pas une trame ignorée en tant que frame supprimé.

Lorsque la valeur de retour est une suppression de flux \_ , la méthode se bloque jusqu’à ce que le temps de référence atteigne l’heure de début de l’exemple. Cela empêche votre pin d’ignorer trop rapidement les exemples. Si le filtre est suspendu, le temps d’attente est infini, jusqu’à ce que le filtre exécute, arrête ou vide les données. (Les modifications d’état de filtre et la diffusion en continu se produisent sur des threads distincts, donc cela ne provoque aucun blocage).

L’énumération **CBaseStreamControl :: StreamControlState** est définie comme suit :


```C++
enum StreamControlState{ 
    STREAM_FLOWING = 0x1000,
    STREAM_DISCARDING
};
```



## <a name="examples"></a>Exemples

L’exemple suivant suppose que le code confidentiel utilise une variable membre nommée m \_ fLastSampleDiscarded pour effectuer le suivi des discontinuités.


```C++
CMyPin::Receive(IMediaSample *pSample)
{
    if (!pSample) return E_POINTER;

    int iStreamState = CheckStreamState(pSample);
    if (iStreamState == STREAM_FLOWING) 
    {
        if (m_fLastSampleDiscarded)
            pSample->SetDiscontinuity(TRUE);
        m_fLastSampleDiscarded = FALSE;
        /* Deliver the sample. */
    } 
    else 
    {
        m_fLastSampleDiscarded = TRUE;  
       // Discard this sample. Do not deliver it.
    }
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Strmctl. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseStreamControl, classe**](cbasestreamcontrol.md)
</dt> </dl>

 

 




