---
title: Méthode ISoftKbd GetSoftKeyboardTextFont (Softkbdc. h)
description: La méthode ISoftKbd GetSoftKeyboardTextFont récupère la police de texte utilisée par un clavier conditionnel.
ms.assetid: 73239359-70b4-47d6-abc5-9fee279ed3a6
keywords:
- Infrastructure des services de texte de méthode GetSoftKeyboardTextFont
- GetSoftKeyboardTextFont méthode Text Services Framework, interface ISoftKbd
- ISoftKbd interface Text Services Framework, méthode GetSoftKeyboardTextFont
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardTextFont
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce939347042415a9060459102cd8a56665ac2de0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105250"
---
# <a name="isoftkbdgetsoftkeyboardtextfont-method"></a>ISoftKbd :: GetSoftKeyboardTextFont, méthode

La méthode **ISoftKbd :: GetSoftKeyboardTextFont** récupère la police de texte utilisée par un clavier conditionnel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetSoftKeyboardTextFont(
  [out] LOGFONTW *pLogFont
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pLogFont* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon dans laquelle cette méthode récupère une structure [**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta) définissant la police du texte pour le clavier conditionnel.

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

[**ISoftKbd::SetSoftKeyboardTextFont**](isoftkbd-setsoftkeyboardtextfont.md)
</dt> </dl>

 

