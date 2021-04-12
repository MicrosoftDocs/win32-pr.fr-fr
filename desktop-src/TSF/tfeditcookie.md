---
title: TfEditCookie (msctf. h)
description: Le type de données TfEditCookie identifie une session d’édition qui a un verrou.
ms.assetid: 1de17286-5d56-4302-a144-5fe6ca7d5557
keywords:
- TfEditCookie
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69281bc38b5df6c22dd5306877aecdb8025af84a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032312"
---
# <a name="tfeditcookie"></a>TfEditCookie

Le type de données **TfEditCookie** identifie une session d’édition qui a un verrou.


```C++
typedef DWORD TfEditCookie;
```



## <a name="remarks"></a>Notes

Le type de données **TfEditCookie** est fourni par le gestionnaire TSF et est utilisé par un client (application ou service de texte) pour identifier une session d’édition avec un verrou en lecture seule ou en lecture/écriture dans différentes méthodes.

Une valeur **TfEditCookie** est obtenue de l’une des manières suivantes.

-   Le client appelle [ITfDocumentMgr :: CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext).
-   Le gestionnaire TSF appelle la méthode client [ITfEditSession ::D oeditsession](/windows/desktop/api/Msctf/nf-msctf-itfeditsession-doeditsession) .
-   Le gestionnaire TSF appelle la méthode cliente [ITfCompositionSink :: OnCompositionTerminated](/windows/desktop/api/Msctf/nf-msctf-itfcompositionsink-oncompositionterminated) .
-   Le gestionnaire TSF appelle la méthode cliente [ITfCleanupContextSink :: OnCleanupContext](/windows/desktop/api/Msctf/nf-msctf-itfcleanupcontextsink-oncleanupcontext) .
-   Le gestionnaire TSF appelle la méthode cliente [ITfTextEditSink :: OnEndEdit](/windows/desktop/api/Msctf/nf-msctf-itftexteditsink-onendedit) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]<br/>                    |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]<br/>                          |
| Composant redistribuable<br/>          | TSF 1,0 sur Windows 2000 professionnel<br/>                                      |
| En-tête<br/>                   | <dl> <dt>Msctf. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Msctf. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITfCleanupContextSink::OnCleanupContext**](/windows/desktop/api/Msctf/nf-msctf-itfcleanupcontextsink-oncleanupcontext)
</dt> <dt>

[**ITfCompositionSink::OnCompositionTerminated**](/windows/desktop/api/Msctf/nf-msctf-itfcompositionsink-oncompositionterminated)
</dt> <dt>

[**ITfDocumentMgr :: CreateContext**](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext)
</dt> <dt>

[**ITfEditSession ::D oEditSession**](/windows/desktop/api/Msctf/nf-msctf-itfeditsession-doeditsession)
</dt> <dt>

[**ITfTextEditSink::OnEndEdit**](/windows/desktop/api/Msctf/nf-msctf-itftexteditsink-onendedit)
</dt> </dl>

 

 





