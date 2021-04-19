---
title: Méthode ISoftKbd SetSoftKeyboardTextFont (Softkbdc. h)
description: La méthode ISoftKbd SetSoftKeyboardTextFont définit la police de texte utilisée par un clavier conditionnel.
ms.assetid: 14705723-4592-40ef-9ebb-1c44c10c3cda
keywords:
- Infrastructure des services de texte de méthode SetSoftKeyboardTextFont
- SetSoftKeyboardTextFont méthode Text Services Framework, interface ISoftKbd
- ISoftKbd interface Text Services Framework, méthode SetSoftKeyboardTextFont
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardTextFont
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ff0a9adce61bc1a671d28c6e5d6ac5b6d329b42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511167"
---
# <a name="isoftkbdsetsoftkeyboardtextfont-method"></a>ISoftKbd :: SetSoftKeyboardTextFont, méthode

La méthode **ISoftKbd :: SetSoftKeyboardTextFont** définit la police de texte utilisée par un clavier conditionnel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetSoftKeyboardTextFont(
  [in] LOGFONTW *pLogFont
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pLogFont* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta) définissant la police du texte pour le clavier conditionnel.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Valeur                                                                                        | Description                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | La méthode a réussi.<br/>           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Le paramètre *pLogFont* n’est pas valide.<br/> |



 

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

[**ISoftKbd::GetSoftKeyboardTextFont**](isoftkbd-getsoftkeyboardtextfont.md)
</dt> </dl>

 

