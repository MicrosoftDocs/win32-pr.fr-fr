---
description: Écrit une valeur de mot dans la base de données spécifiée.
ms.assetid: 8f921e14-4a82-4d8e-83fa-beb78118ecb8
title: SdbWriteWORDTag fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 75a5b3eb430901de36d5aca325f928aae266bc39
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523316"
---
# <a name="sdbwritewordtag-function"></a>SdbWriteWORDTag fonction)

Écrit une valeur de **mot** dans la base de données spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI SdbWriteWORDTag(
  _In_ PDB  pdb,
  _In_ TAG  tTag,
  _In_ WORD wData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

fichier *PDB* \[ dans\]
</dt> <dd>

Handle de la base de données de shims.

</dd> <dt>

*tTag* \[ dans\]
</dt> <dd>

BALIse pour l’entrée. Cette BALIse doit être de **type \_ \_ mot de balise**.

</dd> <dt>

*wData* \[ dans\]
</dt> <dd>

La valeur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La fonction retourne **true** en cas de réussite ou **false** en cas d’échec.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SdbWriteBinaryTag**](sdbwritebinarytag.md)
</dt> <dt>

[**SdbWriteDWORDTag**](sdbwritedwordtag.md)
</dt> <dt>

[**SdbWriteQWORDTag**](sdbwriteqwordtag.md)
</dt> <dt>

[**SdbWriteStringTag**](sdbwritestringtag.md)
</dt> </dl>

 

 




