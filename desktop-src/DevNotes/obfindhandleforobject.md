---
description: Récupère un handle d’objet pour l’objet spécifié associé au processus spécifié.
ms.assetid: c7b371c3-02c0-4137-ad9d-dd07a74fe2a5
title: ObFindHandleForObject, fonction (Ntosp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObFindHandleForObject
api_type:
- LibDef
api_location:
- Ntoskrnl.lib
- Ntoskrnl.dll
ms.openlocfilehash: 7ba87d05d4264f3bb160bae16053a338e38e2145
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860789"
---
# <a name="obfindhandleforobject-function"></a>ObFindHandleForObject fonction)

\[Cette fonction est obsolète et peut être modifiée ou non disponible dans les futures versions de Windows. Évitez d’utiliser cette fonction.\]

Récupère un handle d’objet pour l’objet spécifié associé au processus spécifié.

## <a name="syntax"></a>Syntaxe


```C++
BOOLEAN WINAPI ObFindHandleForObject(
  _In_     PEPROCESS Process,
  _In_     PVOID     Object,
  _In_opt_ PVOID     Reserved1,
  _In_opt_ PVOID     Reserved2,
  _Out_    PHANDLE   Handle
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Processus* \[ dans\]
</dt> <dd>

Processus. Ce descripteur est retourné par la fonction **IoGetCurrentProcess** ou **PsGetCurrentProcess** .

</dd> <dt>

*Objet* \[ dans\]
</dt> <dd>

Pointeur vers l’objet.

</dd> <dt>

*Reserved1* \[ dans, facultatif\]
</dt> <dd>

Réservé.

</dd> <dt>

*Reserved2* \[ dans, facultatif\]
</dt> <dd>

Réservé.

</dd> <dt>

*Gérer* \[ à\]
</dt> <dd>

Handle d’objet.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La fonction retourne la **valeur true** si une correspondance est trouvée et la **valeur false** dans le cas contraire.

## <a name="remarks"></a>Notes

Cette fonction est disponible dans Ntoskrnl.exe et peut être appelée uniquement à partir du mode noyau. La bibliothèque d’importation correspondante est disponible via le kit WDK (Windows Driver Kit).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Ntosp. h</dt> </dl>      |
| Bibliothèque<br/>                  | <dl> <dt>Ntoskrnl. lib</dt> </dl> |



 

 




