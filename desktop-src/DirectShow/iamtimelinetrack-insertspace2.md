---
description: 'La méthode InsertSpace2 fractionne tous les objets qui existent à l’heure spécifiée et insère de l’espace entre eux. Cette méthode est équivalente à IAMTimelineTrack :: InsertSpace, mais prend des valeurs REFTIME.'
ms.assetid: 818a1dad-0c8d-4728-82d6-cd52c6c830a2
title: 'IAMTimelineTrack :: InsertSpace2, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.InsertSpace2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 401c20d766fe9751c35cb59c03bca739494b3f8a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126857577"
---
# <a name="iamtimelinetrackinsertspace2-method"></a>IAMTimelineTrack :: InsertSpace2, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `InsertSpace2` méthode fractionne tous les objets qui existent à l’heure spécifiée et insère de l’espace entre eux. Cette méthode est équivalente à [**IAMTimelineTrack :: InsertSpace**](iamtimelinetrack-insertspace.md), mais prend des valeurs [**REFTIME**](reftime.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT InsertSpace2(
   REFTIME rtStart,
   REFTIME rtEnd
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*rtStart* 
</dt> <dd>

Heure à laquelle le fractionnement est créé, et le point de départ de l’espace inséré, en secondes.

</dd> <dt>

*rtEnd* 
</dt> <dd>

Point de terminaison de l’espace inséré, en secondes.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **HRESULT** . Les valeurs de retour possibles sont les suivantes :



| Code de retour                                                                                   | Description                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>       | Il n’y a aucun objet à l’heure spécifiée.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>          | Réussite.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Argument non valide.<br/>                           |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante.<br/>                        |



 

## <a name="remarks"></a>Notes

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

[**Interface IAMTimelineTrack**](iamtimelinetrack.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




