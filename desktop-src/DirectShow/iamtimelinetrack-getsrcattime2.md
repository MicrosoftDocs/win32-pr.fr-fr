---
description: 'La méthode GetSrcAtTime2 récupère l’objet source le plus proche de l’heure spécifiée, en fonction des conditions limites spécifiées. Cette méthode est équivalente à IAMTimelineTrack :: GetSrcAtTime, mais prend une valeur REFTIME.'
ms.assetid: 11f6545b-478b-4ffd-8344-2bf8585db2a5
title: 'IAMTimelineTrack :: GetSrcAtTime2, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetSrcAtTime2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7a1cd2e91f5f9372654fa9cfefddc7e99f5f4bc69be8fa010815902c44e76dd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117998803"
---
# <a name="iamtimelinetrackgetsrcattime2-method"></a>IAMTimelineTrack :: GetSrcAtTime2, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `GetSrcAtTime2` méthode récupère l’objet source le plus proche de l’heure spécifiée, en fonction des conditions limites spécifiées. Cette méthode est équivalente à [**IAMTimelineTrack :: GetSrcAtTime**](iamtimelinetrack-getsrcattime.md), mais prend une valeur [**REFTIME**](reftime.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetSrcAtTime2(
  [out] IAMTimelineObj **ppSrc,
        REFTIME        Time,
        long           SearchDirection
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppSrc* \[ à\]
</dt> <dd>

Reçoit un pointeur vers l’interface [**IAMTimelineObj**](iamtimelineobj.md) de l’objet source.

</dd> <dt>

*Time* 
</dt> <dd>

Heure de début de la recherche, en secondes.

</dd> <dt>

*SearchDirection* 
</dt> <dd>

Membre du type [**d' \_ \_ \_ indicateur de recherche DEXTERF Track**](dexterf-track-search-flags.md) qui spécifie les conditions limites pour la recherche.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** suivantes :



| Code de retour                                                                                  | Description                                |
|----------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>      | L’objet source n’a pas été trouvé.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>         | A trouvé un objet source.<br/>        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argument non valide.<br/>               |
| <dl> <dt>**\_pointeur E**</dt> </dl>    | Argument de pointeur **null** .<br/>      |



 

## <a name="remarks"></a>Remarques

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Conditions requises



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

 

 




