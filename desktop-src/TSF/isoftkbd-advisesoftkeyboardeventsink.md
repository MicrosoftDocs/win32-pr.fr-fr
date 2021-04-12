---
title: Méthode ISoftKbd AdviseSoftKeyboardEventSink (Softkbdc. h)
description: La méthode ISoftKbd AdviseSoftKeyboardEventSink installe un récepteur d’événements de clavier logiciel pour gérer les notifications OnKeySelection à partir du clavier logiciel.
ms.assetid: f7a441dc-7bef-4fc0-bc62-c153a55a844c
keywords:
- Infrastructure des services de texte de méthode AdviseSoftKeyboardEventSink
- AdviseSoftKeyboardEventSink méthode Text Services Framework, interface ISoftKbd
- ISoftKbd interface Text Services Framework, méthode AdviseSoftKeyboardEventSink
topic_type:
- apiref
api_name:
- ISoftKbd.AdviseSoftKeyboardEventSink
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ab17de2104c6104b044f027152cfc45cca968b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385048"
---
# <a name="isoftkbdadvisesoftkeyboardeventsink-method"></a>ISoftKbd :: AdviseSoftKeyboardEventSink, méthode

La méthode **ISoftKbd :: AdviseSoftKeyboardEventSink** installe un récepteur d’événements de clavier logiciel pour gérer les notifications OnKeySelection à partir du clavier logiciel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AdviseSoftKeyboardEventSink(
  [in]  DWORD    dwKeyboardId,
  [in]  REFIID   riid,
  [in]  IUnknown *punk,
  [out] DWORD    *pdwCookie
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwKeyboardId* \[ dans\]
</dt> <dd>

Identificateur du clavier conditionnel.

</dd> <dt>

*riid* \[ dans\]
</dt> <dd>

Identificateur d’interface de l’interface du récepteur.

</dd> <dt>

*punk* \[ dans\]
</dt> <dd>

Pointeur vers [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) pour l’interface du récepteur spécifiée par *riid*. Ce paramètre ne peut pas avoir la valeur **null**.

</dd> <dt>

*pdwCookie* \[ à\]
</dt> <dd>

Pointeur vers la mémoire tampon dans laquelle cette méthode récupère le « cookie » de clavier logiciel utilisé pour la connexion au client. Le cookie doit être unique pour chaque connexion.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Valeur                                                                                        | Description                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | La méthode a réussi.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Un ou plusieurs paramètres ne sont pas valides.<br/> |



 

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

[**ISoftKbd::UnadviseSoftKeyboardEventSink**](isoftkbd-unadvisesoftkeyboardeventsink.md)
</dt> </dl>

 

