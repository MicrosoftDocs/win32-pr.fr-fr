---
description: Recherche l’instance suivante de la propriété spécifiée par le paramètre hProperty.
ms.assetid: f77cb92b-5936-4349-bf66-643c16e9e0df
title: FindPropertyInstanceRestart, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindPropertyInstanceRestart
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: d1e731bb00b28bb62862dd18fbd6031fa973fe38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519253"
---
# <a name="findpropertyinstancerestart-function"></a>FindPropertyInstanceRestart fonction)

La fonction **FindPropertyInstanceRestart** recherche l’instance suivante de la propriété spécifiée par le paramètre *hProperty* .

## <a name="syntax"></a>Syntaxe


```C++
LPPROPERTYINST WINAPI FindPropertyInstanceRestart(
  _In_ HFRAME         hFrame,
  _In_ HPROPERTY      hProperty,
  _In_ LPPROPERTYINST *lpRestartKey,
  _In_ BOOL           DirForward
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hFrame* \[ dans\]
</dt> <dd>

Handle du frame. Le descripteur de frame peut être récupéré par un appel à la fonction [GetFrame](getframe.md) .

</dd> <dt>

*hProperty* \[ dans\]
</dt> <dd>

Handle vers la propriété à rechercher. Le descripteur de propriété peut être récupéré par un appel à la fonction [GetProperty](getproperty.md) .

</dd> <dt>

*lpRestartKey* \[ dans\]
</dt> <dd>

Pointeur vers l’instance de propriété utilisée comme point de départ de la recherche. Si le paramètre *lpRestartKey* a la valeur **null**, la recherche commence au début du frame ou à la fin du frame, selon la valeur du paramètre *DirForward* .

Si *lpRestartKey* pointe vers la **valeur null**, la recherche commence au début du frame si *DirForward* a la **valeur true** ou à la fin du frame si le paramètre a la **valeur false**.

</dd> <dt>

*DirForward* \[ dans\]
</dt> <dd>

Indicateur du sens de la recherche. Si la valeur est **true**, la recherche passe de l’emplacement actuel à la fin du frame. Si la valeur est **false**, la recherche passe de l’emplacement actuel au début du frame.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est le prochain **LPPROPERTYINST** valide.

Si la fonction échoue, la valeur de retour est **null**.

## <a name="remarks"></a>Notes

Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **FindPropertyInstanceRestart** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[GetFrame](getframe.md)
</dt> <dt>

[GetProperty](getproperty.md)
</dt> </dl>

 

 




