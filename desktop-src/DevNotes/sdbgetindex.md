---
description: Récupère l’index pour la balise et le type de clé spécifiés à partir de la base de données spécifiée.
ms.assetid: 5fa44252-ba26-43ed-9de0-5917e4ec797c
title: SdbGetIndex fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetIndex
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 36bfa9df62aba2ce8fb1df637c802369ca35911bd02c9876ea6b649c66698685
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118666474"
---
# <a name="sdbgetindex-function"></a>SdbGetIndex fonction)

Récupère l’index pour la balise et le type de clé spécifiés à partir de la base de données spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
TAGID WINAPI SdbGetIndex(
  _In_      PDB     pdb,
  _In_      TAG     tWhich,
  _In_      TAG     tKey,
  _Out_opt_ LPDWORD lpdwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

fichier *PDB* \[ dans\]
</dt> <dd>

Handle de la base de données de shims.

</dd> <dt>

*tWhich* \[ dans\]
</dt> <dd>

BALIse.

</dd> <dt>

*tKey* \[ dans\]
</dt> <dd>

Type de clé.

</dd> <dt>

*lpdwFlags* \[ out, facultatif\]
</dt> <dd>

Ce paramètre peut être égal à 0 ou à la **\_ \_ \_ clé unique de l’index SHIMDB** (0x00000001).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**TagId** de l’index ou **TagId \_ null**.

## <a name="remarks"></a>Remarques

L’index résultant peut être utilisé pour les opérations de lecture.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




