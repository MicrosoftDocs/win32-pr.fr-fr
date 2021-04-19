---
description: 'La méthode GetMediaLength2 récupère la longueur du média de cet objet source. Cette méthode est équivalente à IAMTimelineSrc :: GetMediaLength, mais prend des valeurs REFTIME.'
ms.assetid: 96685e00-4e16-4205-a6ad-8b83cf2f8c29
title: 'IAMTimelineSrc :: GetMediaLength2, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaLength2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: caee510db9ddeda1923327176a634a9011601e4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528369"
---
# <a name="iamtimelinesrcgetmedialength2-method"></a>IAMTimelineSrc :: GetMediaLength2, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La `GetMediaLength2` méthode récupère la longueur du média de cet objet source. Cette méthode est équivalente à [**IAMTimelineSrc :: GetMediaLength**](iamtimelinesrc-getmedialength.md), mais prend des valeurs [**REFTIME**](reftime.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetMediaLength2(
   REFTIME *pLength
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pLength* 
</dt> <dd>

Reçoit la durée du média en secondes.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** suivantes :



| Code de retour                                                                                     | Description                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>            | Opération réussie.<br/>                                |
| <dl> <dt>**\_NOTDETERMINED E**</dt> </dl> | Les temps de support ne sont pas définis sur cet objet.<br/> |
| <dl> <dt>**\_pointeur E**</dt> </dl>       | Argument de pointeur **null** .<br/>              |



 

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

[**Interface IAMTimelineSrc**](iamtimelinesrc.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




