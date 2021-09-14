---
description: La méthode GetTransAtTime récupère la transition la plus proche de l’heure spécifiée, en fonction des conditions limites spécifiées.
ms.assetid: 33b3686b-5a9d-4eb2-bd40-4d6f569e7d89
title: 'IAMTimelineTransable :: GetTransAtTime, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetTransAtTime
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 77ca7b1c9a5517d849b38ba1ba22216583d7af87
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012190"
---
# <a name="iamtimelinetransablegettransattime-method"></a>IAMTimelineTransable :: GetTransAtTime, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `GetTransAtTime` méthode récupère la transition la plus proche du temps spécifié, en fonction des conditions limites spécifiées.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetTransAtTime(
  [out] IAMTimelineObj **ppObj,
        REFERENCE_TIME Time,
        long           SearchDirection
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppObj* \[ à\]
</dt> <dd>

Reçoit un pointeur vers l’interface [**IAMTimelineObj**](iamtimelineobj.md) de la transition.

</dd> <dt>

*Time* 
</dt> <dd>

Heure à partir de laquelle commencer la recherche, en unités de 100 nanosecondes.

</dd> <dt>

*SearchDirection* 
</dt> <dd>

Membre du type [**d' \_ \_ \_ indicateur de recherche DEXTERF Track**](dexterf-track-search-flags.md) qui spécifie les conditions limites pour la recherche.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne l’une des valeurs **HRESULT** suivantes :



| Code de retour                                                                                  | Description                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>      | Aucune transition n’a été trouvée.<br/>   |
| <dl> <dt>**\_OK**</dt> </dl>         | La transition a été trouvée.<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argument non valide.<br/>          |
| <dl> <dt>**\_pointeur E**</dt> </dl>    | Argument de pointeur **null** .<br/> |



 

## <a name="remarks"></a>Notes

Si la méthode retourne la valeur \_ OK, l’interface **IAMTimelineObj** qu’elle retourne a un nombre de références en attente. Veillez à libérer l’interface une fois que vous avez fini de l’utiliser.

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

[**Interface IAMTimelineTransable**](iamtimelinetransable.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




