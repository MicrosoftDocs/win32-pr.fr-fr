---
title: Méthode ISoftKbd SetSoftKeyboardTypeMode (Softkbdc. h)
description: La méthode ISoftKbd SetSoftKeyboardTypeMode définit le mode de saisie d’un clavier conditionnel.
ms.assetid: 0b5b5056-59b3-41c7-bc43-70b5c3cd51c2
keywords:
- Infrastructure des services de texte de méthode SetSoftKeyboardTypeMode
- SetSoftKeyboardTypeMode méthode Text Services Framework, interface ISoftKbd
- ISoftKbd interface Text Services Framework, méthode SetSoftKeyboardTypeMode
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardTypeMode
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55c01465debc42926888e2cb12a3a5b9d884498b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466303"
---
# <a name="isoftkbdsetsoftkeyboardtypemode-method"></a>ISoftKbd :: SetSoftKeyboardTypeMode, méthode

La méthode **ISoftKbd :: SetSoftKeyboardTypeMode** définit le mode de saisie d’un clavier conditionnel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetSoftKeyboardTypeMode(
  [in] TYPEMODE TypeMode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*TypeMode* \[ dans\]
</dt> <dd>

Mode de type. Les valeurs possibles sont définies pour l’énumération [**TYPEMODE**](typemode.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Valeur                                                                                        | Description                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | La méthode a réussi.<br/>           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Le paramètre *TypeMode* n’est pas valide.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| Composant redistribuable<br/>          | TSF 1,0 sur Windows 2000 professionnel<br/>                                        |
| En-tête<br/>                   | <dl> <dt>Softkbdc. h</dt> </dl>  |
| MIDL<br/>                      | <dl> <dt>Softkbd. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> <dt>

[**ISoftKbd::GetSoftKeyboardTypeMode**](isoftkbd-getsoftkeyboardtypemode.md)
</dt> <dt>

[**TYPEMODE**](typemode.md)
</dt> </dl>

 

 





