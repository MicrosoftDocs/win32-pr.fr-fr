---
description: La méthode Remove supprime cet objet de la chronologie (y compris les sous-objets, mais pas les enfants), à des fins de réinsertion ailleurs.
ms.assetid: 118a08a5-abba-47df-8aeb-42ce8c8ed2ba
title: 'IAMTimelineObj :: Remove, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.Remove
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 356f7239cbdbe3972f11fcc95dd9bf44dc1b06d086a8e44c9131c0061f3ec211
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118155262"
---
# <a name="iamtimelineobjremove-method"></a>IAMTimelineObj :: Remove, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `Remove` méthode supprime cet objet de la chronologie (y compris les sous-objets, mais pas les enfants), à des fins de réinsertion ailleurs.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Remove();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Appelez cette méthode uniquement si l’application Insère immédiatement l’objet dans la chronologie. Il s’agit d’une opération non valide pour appeler cette méthode sans réinsérer l’objet. Pour supprimer définitivement un objet, appelez [**IAMTimelineObj :: RemoveAll**](iamtimelineobj-removeall.md).

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

[**Interface IAMTimelineObj**](iamtimelineobj.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




