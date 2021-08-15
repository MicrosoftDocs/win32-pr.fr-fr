---
title: Méthode ISoftKbd GetSoftKeyboardTypeMode (Softkbdc. h)
description: La méthode ISoftKbd GetSoftKeyboardTypeMode récupère le mode de type pour un clavier conditionnel.
ms.assetid: 77294652-b82e-4b69-bb55-5ebebc3c97c7
keywords:
- Infrastructure des services de texte de méthode GetSoftKeyboardTypeMode
- GetSoftKeyboardTypeMode méthode Text Services Framework, interface ISoftKbd
- ISoftKbd interface Text Services Framework, méthode GetSoftKeyboardTypeMode
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardTypeMode
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab1205f0d9f59e027db75d2df580917392c445e812425c714b1688ce784a68ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117952576"
---
# <a name="isoftkbdgetsoftkeyboardtypemode-method"></a>ISoftKbd :: GetSoftKeyboardTypeMode, méthode

La méthode **ISoftKbd :: GetSoftKeyboardTypeMode** récupère le mode de type pour un clavier conditionnel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetSoftKeyboardTypeMode(
  [out] TYPEMODE *lpTypeMode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpTypeMode* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon dans laquelle cette méthode récupère le mode de type. Les valeurs possibles sont définies pour l’énumération [**TYPEMODE**](typemode.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Valeur                                                                                        | Description                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | La méthode a réussi.<br/>             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Le paramètre *lpTypeMode* n’est pas valide.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| Composant redistribuable<br/>          | TSF 1,0 sur Windows 2000 Professional<br/>                                        |
| En-tête<br/>                   | <dl> <dt>Softkbdc. h</dt> </dl>  |
| MIDL<br/>                      | <dl> <dt>Softkbd. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> <dt>

[**ISoftKbd::SetSoftKeyboardTypeMode**](isoftkbd-setsoftkeyboardtypemode.md)
</dt> <dt>

[**TYPEMODE**](typemode.md)
</dt> </dl>

 

 





