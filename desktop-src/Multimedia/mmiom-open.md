---
title: Message MMIOM_OPEN (mmsystem. h)
description: Le \_ message MMIOM Open est envoyé à une procédure d’e/s par la fonction mmioOpen pour demander l’ouverture ou la suppression d’un fichier.
ms.assetid: 02b2cf22-21a3-4f49-b90e-7b44478c0168
keywords:
- message MMIOM_OPEN Windows Multimedia
topic_type:
- apiref
api_name:
- MMIOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74cb4c54a7f35fe426cf528d5eb9e076a44bf4b7e06744628ba65fe1bf7cb410
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065369"
---
# <a name="mmiom_open-message"></a>MMIOM \_ ouvrir le message

Le message **MMIOM \_ Open** est envoyé à une procédure d’e/s par la fonction [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) pour demander l’ouverture ou la suppression d’un fichier.


```C++
MMIOM_OPEN 
lParam1 = (LPARAM) lpszFileName 
lParam2 = reserved 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpszFileName"></span><span id="lpszfilename"></span><span id="LPSZFILENAME"></span>*lpszFileName*
</dt> <dd>

Chaîne terminée par le caractère null qui contient le nom du fichier à ouvrir.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Réservé.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne MMSYSERR \_ NOerreur en cas de réussite ou une erreur dans le cas contraire. Les valeurs d’erreur possibles sont les suivantes :



| Condition requise | Valeur |
|--------------------|---------------------------------------------|
| MMIOM \_ CANNOTOPEN  | Impossible d’ouvrir le fichier.               |
| MMIOM \_ OUTOFMEMORY | Mémoire insuffisante pour effectuer l’opération. |



 

## <a name="remarks"></a>Remarques

Le membre **dwFlags** de la structure [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) contient des indicateurs passés à la fonction [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) .

Le membre **lDiskOffset** de la structure [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) est initialisé à zéro. Si cette valeur est incorrecte, la procédure d’e/s doit la corriger.

Si l’application a passé une structure [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) à [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen), la valeur de retour est retournée dans le membre **wErrorRet** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Mmsystem. h (inclure Windows. h)</dt> </dl> |



 

