---
description: 'La méthode GetTransAtTime2 récupère la transition la plus proche de l’heure spécifiée, en fonction des conditions limites spécifiées. Cette méthode est équivalente à IAMTimelineTransable :: GetTransAtTime, mais prend un paramètre REFTIME.'
ms.assetid: b51b53ec-4b56-4900-98b5-427d752354b0
title: 'IAMTimelineTransable :: GetTransAtTime2, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetTransAtTime2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6b3de498791a634ea651da46ba9c95557ca12b87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541512"
---
# <a name="iamtimelinetransablegettransattime2-method"></a>IAMTimelineTransable :: GetTransAtTime2, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La `GetTransAtTime2` méthode récupère la transition la plus proche du temps spécifié, en fonction des conditions limites spécifiées. Cette méthode est équivalente à [**IAMTimelineTransable :: GetTransAtTime**](iamtimelinetransable-gettransattime.md), mais prend un paramètre [**REFTIME**](reftime.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetTransAtTime2(
  [out] IAMTimelineObj **ppObj,
        REFTIME        Time,
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

Heure à partir de laquelle commencer la recherche, en secondes.

</dd> <dt>

*SearchDirection* 
</dt> <dd>

Membre du type [**d' \_ \_ \_ indicateur de recherche DEXTERF Track**](dexterf-track-search-flags.md) qui spécifie les conditions limites pour la recherche.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** suivantes :



| Code de retour                                                                                  | Description                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>      | Aucune transition n’a été trouvée.<br/>   |
| <dl> <dt>**\_OK**</dt> </dl>         | La transition a été trouvée.<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argument non valide.<br/>          |
| <dl> <dt>**\_pointeur E**</dt> </dl>    | Argument de pointeur **null** .<br/> |



 

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



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IAMTimelineTransable**](iamtimelinetransable.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




