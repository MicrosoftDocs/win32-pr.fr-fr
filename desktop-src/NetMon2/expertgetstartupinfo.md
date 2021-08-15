---
description: La fonction ExpertGetStartupInfo récupère les informations de configuration de démarrage de l’expert.
ms.assetid: 15f080ed-50b7-40c6-b283-dbe416a2b0e9
title: ExpertGetStartupInfo, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertGetStartupInfo
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7e4327965dce1c4bca07846a818609e555c16a3a27b0a19204a9971eaf9d642e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366881"
---
# <a name="expertgetstartupinfo-function"></a>ExpertGetStartupInfo fonction)

La fonction **ExpertGetStartupInfo** récupère les informations de configuration de démarrage de l’expert.

## <a name="syntax"></a>Syntaxe


```C++
DWORD WINAPI ExpertGetStartupInfo(
  _In_  HEXPERTKEY         hExpertKey,
  _Out_ PEXPERTSTARTUPINFO pExpertStartupInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hExpertKey* \[ dans\]
</dt> <dd>

Identificateur d’expert unique. Moniteur réseau transmet *hExpertKey* à l’expert lorsqu’il appelle la fonction [Run](run.md) .

</dd> <dt>

*pExpertStartupInfo* \[ à\]
</dt> <dd>

Pointeur vers une structure [EXPERTSTARTUPINFO](expertstartupinfo.md) qui contient des informations de démarrage.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est NMERR \_ Success.

Si la fonction échoue, la valeur de retour est NMERR.

## <a name="remarks"></a>Remarques

La fonction **ExpertGetStartupInfo** est utilisée si l’expert doit déterminer les informations de démarrage utilisées.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




