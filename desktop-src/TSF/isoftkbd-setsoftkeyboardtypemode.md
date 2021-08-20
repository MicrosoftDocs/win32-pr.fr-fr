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
ms.openlocfilehash: 50a43fd160444c2c1d29226aadb898ca60eec6038759452ca8451466337f1b3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117952485"
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



 

## <a name="requirements"></a>Conditions requises



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

[**ISoftKbd::GetSoftKeyboardTypeMode**](isoftkbd-getsoftkeyboardtypemode.md)
</dt> <dt>

[**TYPEMODE**](typemode.md)
</dt> </dl>

 

 





