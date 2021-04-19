---
description: La structure du DÉCLENCHEur indique une action que le pilote doit prendre à un moment donné.
ms.assetid: 63541796-b0d8-456c-8544-697fedbe05f7
title: Structure de DÉCLENCHEur (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TRIGGER
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: d9b385557e3c34bdf75f2bf959d4e5e3e47e0750
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528270"
---
# <a name="trigger-structure"></a>Structure de DÉCLENCHEur

La structure du **déclencheur** indique une action que le pilote doit prendre à un moment donné.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _TRIGGER {
  BOOL         TriggerActive;
  BYTE         TriggerType;
  BYTE         TriggerAction;
  DWORD        TriggerFlags;
  PATTERNMATCH TriggerPatternMatch;
  DWORD        TriggerBufferSize;
  DWORD        Reserved;
} TRIGGER, *LPTRIGGER;
```



## <a name="members"></a>Membres

<dl> <dt>

**TriggerActive**
</dt> <dd>

Valeur booléenne qui détermine si le pilote doit faire l’objet d’une attention particulière.

</dd> <dt>

**TriggerType**
</dt> <dd>

Code d’opération du déclencheur.

</dd> <dt>

**TriggerAction**
</dt> <dd>

Action que le déclencheur doit exécuter s’il est déclenché.

</dd> <dt>

**TriggerFlags**
</dt> <dd>

Indicateurs de déclencheur.

</dd> <dt>

**TriggerPatternMatch**
</dt> <dd>

Le modèle de déclencheur correspond.

</dd> <dt>

**TriggerBufferSize**
</dt> <dd>

Taille de la mémoire tampon du déclencheur.

</dd> <dt>

**Reserved**
</dt> <dd>

Réservé.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




