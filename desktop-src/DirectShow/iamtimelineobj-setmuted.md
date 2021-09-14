---
description: La méthode SetMuted définit l’État muet de l’objet. Un objet muet n’est pas rendu, mais il reste dans la chronologie.
ms.assetid: 5dcd8533-8e58-4553-ac01-928723485f5d
title: 'IAMTimelineObj :: SetMuted, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetMuted
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ac3f5b798ef56251fa64b55a92ae1e94e2fd61b8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094745"
---
# <a name="iamtimelineobjsetmuted-method"></a>IAMTimelineObj :: SetMuted, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `SetMuted` méthode définit l’État muet de l’objet. Un objet muet n’est pas rendu, mais il reste dans la chronologie.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetMuted(
   BOOL newVal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*newVal* 
</dt> <dd>

Indicateur qui spécifie l’État muet. Si la **valeur est true**, l’objet et tous ses enfants sont muets.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

La désactivation d’un objet désactive également tous les enfants contenus dans l’objet. Par exemple, si vous désactivez une piste, les transitions, les sources et les effets de cette piste sont également muets. Une fois que l’objet n’est plus muet, ses enfants reviennent à leur état précédent, qui peut être muet ou muet.

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

[**Interface IAMTimelineObj**](iamtimelineobj.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




