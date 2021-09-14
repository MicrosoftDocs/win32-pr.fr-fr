---
description: La \_ structure d’événement Update met à jour les événements. Cette structure est repassée à l’application appelante via la procédure de rappel de l’état de l’événement par le NPP.
ms.assetid: 6896be5a-f986-44ff-a18b-010f7b9858aa
title: Structure de UPDATE_EVENT (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UPDATE_EVENT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3da45020a68114182a71b25ff9bba380d3f89eee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127229584"
---
# <a name="update_event-structure"></a>METTRE à jour la \_ structure d’événement

La structure d' **\_ événement Update** met à jour les événements. Cette structure est repassée à l’application appelante via la procédure de rappel de l’état de l’événement par le NPP.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _UPDATE_EVENT {
  USHORT       Event;
  DWORD        Action;
  DWORD        Status;
  DWORD        Value;
  __int64      TimeStamp;
  DWORD_PTR    lpUserContext;
  DWORD_PTR    lpReserved;
  UINT         FramesDropped;
  union {
    DWORD                        Reserved;
    LPFRAMETABLE                 lpFrameTable;
    DWORD_PTR                    lpPacketQueue;
    SECURITY_PERMISSION_RESPONSE SecurityResponse;
  };
  LPSTATISTICS lpFinalStats;
} UPDATE_EVENT, *PUPDATE_EVENT;
```



## <a name="members"></a>Membres

<dl> <dt>

**Event**
</dt> <dd>

Événement réel en cours d’enregistrement.

</dd> <dt>

**Action**
</dt> <dd>

Action entreprise.

</dd> <dt>

**État**
</dt> <dd>

Indication de l’état du réseau.

</dd> <dt>

**Valeur**
</dt> <dd>

Variable de compteur auxiliaire.

</dd> <dt>

**Confirmé**
</dt> <dd>

Événements marqués, en microsecondes.

</dd> <dt>

**lpUserContext**
</dt> <dd>

Contexte utilisateur donné par l’application.

</dd> <dt>

**lpReserved**
</dt> <dd>

Utilisation d’un pilote ou d’un NAL.

</dd> <dt>

**FramesDropped**
</dt> <dd>

Frames RTF supprimés dans la mémoire tampon spécifiée.

</dd> <dt>

**Reserved**
</dt> <dd>

Aucune donnée n’est renvoyée avec cette option de commutateur.

</dd> <dt>

**lpFrameTable**
</dt> <dd>

RTF uniquement.

</dd> <dt>

**lpPacketQueue**
</dt> <dd>

Pour les transmissions.

</dd> <dt>

**SecurityResponse**
</dt> <dd>

Réponse du moniteur de sécurité à distance.

</dd> <dt>

**lpFinalStats**
</dt> <dd>

Cela n’est fourni que pour les arrêts non liés à la sécurité (par exemple, les déclencheurs).

</dd> </dl>

## <a name="remarks"></a>Remarques

Les utilisateurs C++ doivent noter que la déclaration pour ce rappel doit se trouver dans la partie publique du fichier d’en-tête :

``` syntax
static WINAPI DWORD NetworkCallback( UPDATE_EVENT events);
```

L’implémentation doit être dans la section protégée du fichier. cpp :

``` syntax
DWORD WINAPI ClassName::NetworkCallback( UPDATE_EVENT events) {};
```

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




