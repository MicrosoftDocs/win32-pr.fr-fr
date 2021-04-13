---
title: Méthode ISoftKbd SelectSoftKeyboard (Softkbdc. h)
description: La méthode ISoftKbd SelectSoftKeyboard sélectionne le clavier logiciel spécifié.
ms.assetid: 7e85d346-3741-457d-aadd-11d3a6710e85
keywords:
- Infrastructure des services de texte de méthode SelectSoftKeyboard
- SelectSoftKeyboard méthode Text Services Framework, interface ISoftKbd
- ISoftKbd interface Text Services Framework, méthode SelectSoftKeyboard
topic_type:
- apiref
api_name:
- ISoftKbd.SelectSoftKeyboard
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbda9399297e9776e7fbd7cecb364fd7f6cd4604
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509066"
---
# <a name="isoftkbdselectsoftkeyboard-method"></a>ISoftKbd :: SelectSoftKeyboard, méthode

La méthode **ISoftKbd :: SelectSoftKeyboard** sélectionne le clavier logiciel spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SelectSoftKeyboard(
  [in] DWORD dwKeyboardId
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwKeyboardId* \[ dans\]
</dt> <dd>

Identificateur du clavier conditionnel à sélectionner.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Valeur                                                                                        | Description                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | La méthode a réussi.<br/>               |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Le paramètre *dwKeyboardId* n’est pas valide.<br/> |



 

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
</dt> </dl>

 

 





