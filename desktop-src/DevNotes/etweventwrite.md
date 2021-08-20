---
description: 'En savoir plus sur : fonction EtwEventWrite'
title: EtwEventWrite
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EtwEventWrite
api_type:
- HeaderDef
api_location:
- ntetw.h
ms.openlocfilehash: b8e06c2a0922038e37766f44c0b9fcd7c85bbb7fd4fa4bd0841192be9e4e9087
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162100"
---
# <a name="etweventwrite-function"></a>EtwEventWrite fonction)

[la fonction EtwEventWrite et les structures qu’elle retourne sont internes au système d’exploitation et sujettes à changement d’une version de Windows à une autre.]

Écrit un événement de base dans une session.

## <a name="syntax"></a>Syntaxe

```C++
ULONG 
EVNTAPI
EtwEventWrite(
    __in REGHANDLE RegHandle,
    __in PCEVENT_DESCRIPTOR EventDescriptor,
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

la fonction EtwEventWrite et les structures qu’elle retourne sont internes au système d’exploitation et peuvent être modifiées d’une version de Windows à une autre. Pour maintenir la compatibilité de votre application, il est préférable d’utiliser à la place des fonctions publiques.

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
