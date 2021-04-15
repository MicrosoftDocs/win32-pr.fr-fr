---
description: Indique l’état actuel d’un expert en cours d’exécution.
ms.assetid: 49107459-599c-4710-8935-4b2c789081de
title: EXPERTSTATUS, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTSTATUS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: a9e201b692bb82c78f88a35f22f2688d096f1771
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525156"
---
# <a name="expertstatus-structure"></a>EXPERTSTATUS, structure

La structure **EXPERTSTATUS** indique l’état actuel d’un expert en cours d’exécution.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  EXPERTSTATUSENUMERATION Status;
  DWORD                   SubStatus;
  DWORD                   PercentDone;
  DWORD                   Frame;
  char                    szStatusText[EXPERTSTRINGLENGTH];
} EXPERTSTATUS, *PEXPERTSTATUS;
```



## <a name="members"></a>Membres

<dl> <dt>

**État**
</dt> <dd>

Valeur actuelle de l’État expert définie par l’énumération [**EXPERTSTATUSENUMERATION**](expertstatusenumeration.md) .

</dd> <dt>

**Sous-état**
</dt> <dd>

Valeur du sous-état.

</dd> <dt>

**PercentDone**
</dt> <dd>

Pourcentage d’achèvement de l’analyse d’experts des données réseau.

</dd> <dt>

**Frame**
</dt> <dd>

Numéro de frame.

</dd> <dt>

**szStatusText**
</dt> <dd>

Texte qui décrit l’état de l’expert.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




