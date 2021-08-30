---
title: ITsSbSession propriété InitialProgram
description: Récupère ou spécifie le programme initial pour cette session.
ms.assetid: c299c4f7-3c5f-468f-9fc7-81eac322dfa2
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété InitialProgram
- Services Bureau à distance de la propriété InitialProgram, interface ITsSbSession
- Services Bureau à distance de l’interface ITsSbSession, propriété InitialProgram
topic_type:
- apiref
api_name:
- ITsSbSession.InitialProgram
- ITsSbSession.get_InitialProgram
- ITsSbSession.put_InitialProgram
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc1ec332283c6eb68d915c7fa0aa92070af1fb34f572d7a27adb058fa40de433
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989889"
---
# <a name="itssbsessioninitialprogram-property"></a>ITsSbSession :: InitialProgram, propriété

Récupère ou spécifie le programme initial pour cette session. Le programme initial est le programme qui est lancé au démarrage de la session utilisateur.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_InitialProgram(
  [in]          BSTR Application
);

HRESULT get_InitialProgram(
  [out, retval] BSTR *app
);
```



## <a name="property-value"></a>Valeur de la propriété

Variable **BSTR** qui contient le programme initial.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                       |
| MIDL<br/>                      | <dl> <dt>Sbtsv. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITsSbSession**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





