---
title: Méthode ISoftKbd SetKeyboardLabelTextCombination (Softkbdc. h)
description: La méthode ISoftKbd SetKeyboardLabelTextCombination définit une combinaison d’étiquette et de texte utilisée pour décrire un clavier conditionnel.
ms.assetid: fe054eae-1a44-41ad-9a44-bc0b46df7c7b
keywords:
- Infrastructure des services de texte de méthode SetKeyboardLabelTextCombination
- SetKeyboardLabelTextCombination méthode Text Services Framework, interface ISoftKbd
- ISoftKbd interface Text Services Framework, méthode SetKeyboardLabelTextCombination
topic_type:
- apiref
api_name:
- ISoftKbd.SetKeyboardLabelTextCombination
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f98dad124455625f0da3ada1a717c692437398
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509738"
---
# <a name="isoftkbdsetkeyboardlabeltextcombination-method"></a>ISoftKbd :: SetKeyboardLabelTextCombination, méthode

La méthode **ISoftKbd :: SetKeyboardLabelTextCombination** définit une combinaison d’étiquette et de texte utilisée pour décrire un clavier conditionnel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetKeyboardLabelTextCombination(
  [in] DWORD nModifierCombination
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nModifierCombination* \[ dans\]
</dt> <dd>

Combinaison d’étiquette et de texte utilisée pour décrire le clavier conditionnel.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Valeur                                                                                        | Description                                                 |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | La méthode a réussi.<br/>                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Le paramètre *nModifierCombination* n’est pas valide.<br/> |



 

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

[**ISoftKbd::SetKeyboardLabelText**](isoftkbd-setkeyboardlabeltext.md)
</dt> </dl>

 

 





