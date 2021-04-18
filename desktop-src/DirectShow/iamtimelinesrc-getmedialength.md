---
description: La méthode GetMediaLength récupère la longueur du média de cet objet source.
ms.assetid: 70298d8f-67e7-4774-a7ae-f0b48e4afda7
title: 'IAMTimelineSrc :: GetMediaLength, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaLength
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5cd896ed0890a199f85838a01c4c6ebec6d0895d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540323"
---
# <a name="iamtimelinesrcgetmedialength-method"></a>IAMTimelineSrc :: GetMediaLength, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La `GetMediaLength` méthode récupère la longueur du média de cet objet source.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetMediaLength(
   REFERENCE_TIME *pLength
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pLength* 
</dt> <dd>

Reçoit la longueur du média en unités de 100 nanosecondes.

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

[**IAMTimelineSrc::SetMediaLength**](iamtimelinesrc-setmedialength.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




