---
title: Méthode ISoftKbd UnadviseSoftKeyboardEventSink (Softkbdc. h)
description: La méthode ISoftKbd UnadviseSoftKeyboardEventSink supprime un récepteur d’événements de clavier conditionnel.
ms.assetid: 785340bd-c4f6-4c80-a492-6e60d1c1d552
keywords:
- Infrastructure des services de texte de méthode UnadviseSoftKeyboardEventSink
- UnadviseSoftKeyboardEventSink méthode Text Services Framework, interface ISoftKbd
- ISoftKbd interface Text Services Framework, méthode UnadviseSoftKeyboardEventSink
topic_type:
- apiref
api_name:
- ISoftKbd.UnadviseSoftKeyboardEventSink
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a77129d1b5df024964af4ab19318963708d4b3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742788"
---
# <a name="isoftkbdunadvisesoftkeyboardeventsink-method"></a>ISoftKbd :: UnadviseSoftKeyboardEventSink, méthode

La méthode **ISoftKbd :: UnadviseSoftKeyboardEventSink** supprime un récepteur d’événements de clavier conditionnel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT UnadviseSoftKeyboardEventSink(
  [in] TfClientId tid
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*TID* \[ dans\]
</dt> <dd>

Identificateur du client qui possède le récepteur d’événements de clavier conditionnel. Cette valeur a été passée lorsque le récepteur d’événements a été installé à l’aide de [ISoftKbd :: AdviseSoftKeyboardEventSink](isoftkbd-advisesoftkeyboardeventsink.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Valeur                                                                                                   | Description                                                   |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                    | La méthode a réussi.<br/>                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>            | Le paramètre *TID* n’est pas valide.<br/>                    |
| <dl> <dt>**CONNECTER \_ E \_ noconnexion**</dt> </dl> | Le récepteur de notifications identifié par *TID* est introuvable.<br/> |



 

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

[ISoftKbd::AdviseSoftKeyboardEventSink](isoftkbd-advisesoftkeyboardeventsink.md)
</dt> </dl>

 

 





