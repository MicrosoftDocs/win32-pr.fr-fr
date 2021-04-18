---
title: Méthode ISoftKbd DestroySoftKeyboardWindow (Softkbdc. h)
description: La méthode ISoftKbd DestroySoftKeyboardWindow détruit une fenêtre de clavier temporaire.
ms.assetid: 44030934-7b4a-46c1-95ea-709fc9004e43
keywords:
- Infrastructure des services de texte de méthode DestroySoftKeyboardWindow
- DestroySoftKeyboardWindow méthode Text Services Framework, interface ISoftKbd
- ISoftKbd interface Text Services Framework, méthode DestroySoftKeyboardWindow
topic_type:
- apiref
api_name:
- ISoftKbd.DestroySoftKeyboardWindow
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb0c460912e8b891503771425fc72484fcc471ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106543423"
---
# <a name="isoftkbddestroysoftkeyboardwindow-method"></a>ISoftKbd ::D méthode estroySoftKeyboardWindow

La méthode **ISoftKbd ::D estroysoftkeyboardwindow** détruit une fenêtre de clavier temporaire.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DestroySoftKeyboardWindow();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Valeur                                                                                | Description                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | La méthode a réussi.<br/> |



 

## <a name="remarks"></a>Notes

Cette méthode supprime une fenêtre de clavier temporaire créée précédemment à l’aide d’un appel à [**ISoftKbd :: CreateSoftKeyboardWindow**](isoftkbd-createsoftkeyboardwindow.md).

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

[**ISoftKbd::CreateSoftKeyboardWindow**](isoftkbd-createsoftkeyboardwindow.md)
</dt> </dl>

 

 





