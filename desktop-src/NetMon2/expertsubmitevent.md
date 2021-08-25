---
description: La fonction ExpertSubmitEvent indique qu’il existe une condition d’événement et fournit une structure de données qui décrit la condition.
ms.assetid: 2339b530-427b-4028-aef6-c2cdd1353f77
title: ExpertSubmitEvent, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertSubmitEvent
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b6ce73d378e4d8432459a23a76b30ebf4d558a5f82ec230e6841eeeb621aed13
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744219"
---
# <a name="expertsubmitevent-function"></a>ExpertSubmitEvent fonction)

La fonction **ExpertSubmitEvent** indique qu’il existe une condition d’événement et fournit une structure de données qui décrit la condition.

## <a name="syntax"></a>Syntaxe


```C++
DWORD WINAPI ExpertSubmitEvent(
  _In_ HEXPERTKEY   hExpertKey,
  _In_ PNMEVENTDATA pExpertEvent
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hExpertKey* \[ dans\]
</dt> <dd>

Identificateur unique de l’expert. Moniteur réseau transmet *hExpertKey* à l’expert lorsqu’il appelle la fonction [Run](run.md) .

</dd> <dt>

*pExpertEvent* \[ dans\]
</dt> <dd>

Pointeur vers une structure **NMEVENTDATA** qui décrit la condition d’événement.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est NMERR \_ Success.

Si la fonction échoue, la valeur de retour indique la raison de l’échec. Si la valeur de retour est NMERR \_ expert \_ Terminate, l’expert nettoie immédiatement et retourne.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




