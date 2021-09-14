---
title: Méthode ISoftKbd SetKeyboardLabelText (Softkbdc. h)
description: La méthode ISoftKbd SetKeyboardLabelText définit le texte de l’étiquette à partir de la disposition d’un clavier conditionnel.
ms.assetid: 86c45c37-fe50-4596-b4c9-960de760a2e0
keywords:
- Infrastructure des services de texte de méthode SetKeyboardLabelText
- SetKeyboardLabelText méthode Text Services Framework, interface ISoftKbd
- ISoftKbd interface Text Services Framework, méthode SetKeyboardLabelText
topic_type:
- apiref
api_name:
- ISoftKbd.SetKeyboardLabelText
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 862341182b9c97a751ba4a130566d5cf18437c2b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311249"
---
# <a name="isoftkbdsetkeyboardlabeltext-method"></a>ISoftKbd :: SetKeyboardLabelText, méthode

La méthode **ISoftKbd :: SetKeyboardLabelText** définit le texte de l’étiquette à partir de la disposition d’un clavier conditionnel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetKeyboardLabelText(
  [in] HKL hKl
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hKl* \[ dans\]
</dt> <dd>

Handle utilisé pour récupérer la disposition installée pour le clavier conditionnel.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode peut retourner l’une de ces valeurs.



| Valeur                                                                                        | Description                                |
|----------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | La méthode a réussi.<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Le paramètre *hKl* n’est pas valide.<br/> |



 

## <a name="requirements"></a>Spécifications



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

[**ISoftKbd::SetKeyboardLabelTextCombination**](isoftkbd-setkeyboardlabeltextcombination.md)
</dt> </dl>

 

 





