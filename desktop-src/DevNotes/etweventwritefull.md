---
description: Écrit un événement complet dans une session.
title: EtwEventWriteFull
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EtwEventWriteFull
api_type:
- HeaderDef
api_location:
- ntetw.h
ms.openlocfilehash: 1fd25931e6a58b97e052ecd7da43bd651688d2bf726d8b5ba2acd84ce820be7a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653428"
---
# <a name="etweventwritefull-function"></a>EtwEventWriteFull fonction)

[la fonction EtwEventWriteFull et les structures qu’elle retourne sont internes au système d’exploitation et sujettes à changement d’une version de Windows à une autre.]

Écrit un événement complet dans une session.

## <a name="syntax"></a>Syntaxe

```C++
ULONG
EVNTAPI
EtwEventWriteFull(
    __in REGHANDLE RegHandle,
    __in PCEVENT_DESCRIPTOR EventDescriptor,
    __in USHORT EventProperty,
    __in_opt LPCGUID ActivityId,
    __in_opt LPCGUID RelatedActivityId,
    __in ULONG UserDataCount,
    __in_ecount_opt(UserDataCount) PEVENT_DATA_DESCRIPTOR UserData
    );
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*RegHandle*
</dt> <dd>

RegHandle pour le fournisseur.

</dd> <dt>

*EventDescriptor* 
</dt> <dd>

Descripteur d’événement de l’événement à enregistrer.

</dd> <dt>

*EventProperty*
</dt> <dd>

Indicateur donné par l’utilisateur.

</dd> <dt>

*ActivityId*
</dt> <dd>

ID d’activité.

</dd> <dt>

*RelatedActivityId*
</dt> <dd>

ID d’activité associé.

</dd> <dt>

*UserDataCount*
</dt> <dd>

Nombre d’éléments de données utilisateur.

</dd> <dt>

*UserData*
</dt> <dd>

Pointeur vers un tableau d’éléments de données utilisateur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Code d’erreur Win32.

## <a name="remarks"></a>Remarques

la fonction EtwEventWriteFull et les structures qu’elle retourne sont internes au système d’exploitation et peuvent être modifiées d’une version de Windows à une autre. Pour maintenir la compatibilité de votre application, il est préférable d’utiliser à la place des fonctions publiques.


## <a name="requirements"></a>Configuration requise
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plateforme cible** | Windows |
| **En-tête** | ntetw. h |

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[EventWrite](/windows/desktop/api/evntprov/nf-evntprov-eventwrite)
</dt> <dt>

[EventWriteEx](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex)
</dt></dl>
