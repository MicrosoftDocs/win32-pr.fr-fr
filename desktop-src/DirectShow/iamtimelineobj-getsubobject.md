---
description: La méthode GetSubObject récupère le sous-objet associé à cet objet.
ms.assetid: 478597d6-ae13-4fa9-a928-19893f378f1a
title: 'IAMTimelineObj :: GetSubObject, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetSubObject
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 74f14658db5ffbaf100925f26573a08b592f6510
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542362"
---
# <a name="iamtimelineobjgetsubobject-method"></a>IAMTimelineObj :: GetSubObject, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La `GetSubObject` méthode récupère le sous-objet associé à cet objet.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetSubObject(
  [out, retval] IUnknown **pVal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pval* \[ out, retval\]
</dt> <dd>

Reçoit un pointeur vers l’interface **IUnknown** de l’objet. Si l’objet n’a pas de sous-objet, la valeur est définie sur **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Chaque objet Timeline peut contenir un pointeur vers un sous-objet associé.

Si la valeur retournée dans *pval* n’est pas **null**, l’interface **IUnknown** a un nombre de références en attente. Veillez à libérer l’interface une fois que vous avez fini de l’utiliser.

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

[**Interface IAMTimelineObj**](iamtimelineobj.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




