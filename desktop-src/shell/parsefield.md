---
description: Lit une ligne à partir de Setup. inf et extrait le champ spécifié de la chaîne.
ms.assetid: 621e85f8-af30-4f1f-bab1-b7f824daa363
title: Fonction ParseField (util. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ParseField
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 45c7d5bc692f969ba821b5d3243b312d0883658e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203445"
---
# <a name="parsefield-function"></a>ParseField fonction)

\[La fonction **ParseField** est actuellement censée être utilisée dans la prochaine version du système d’exploitation Microsoft Windows. Il peut être modifié ou non disponible dans les versions ultérieures.\]

Lit une ligne à partir de Setup. inf et extrait le champ spécifié de la chaîne.

## <a name="syntax"></a>Syntaxe


```C++
bool ParseField(
  _In_ LPCTSTR *szData,
  _In_ int     n,
  _In_ LPTSTR  *szBuf,
  _In_ int     iBufLen
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*szData* \[ dans\]
</dt> <dd>

Tapez : **LPCTSTR \** _

Pointeur vers la ligne de Setup. inf.

</dd> <dt>

_n * \[ dans\]
</dt> <dd>

Type : **int**

**Entier** qui indique le champ à extraire.

<dt>



  (0)


</dt> <dd>

Indique le champ avant un signe égal (=).

</dd> <dt>



 (1)


</dt> <dd>

Indique le premier champ.

</dd> </dl> </dd> <dt>

*szBuf* \[ dans\]
</dt> <dd>

Type : **LPTStr \** _

Pointeur vers la mémoire tampon qui reçoit le champ extrait.

</dd> <dt>

_iBufLen * \[ dans\]
</dt> <dd>

Type : **int**

**Entier** qui reçoit la taille de la mémoire tampon qui reçoit le champ extrait.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **bool**

Retourne la **valeur true** si la fonction a réussi et **false** si elle échoue.

## <a name="remarks"></a>Notes

Les champs de la chaîne doivent être séparés par des virgules.

Les espaces de début et de fin sont supprimés.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Util. h</dt> </dl>                             |
| Bibliothèque<br/>                  | <dl> <dt>Shell32. lib</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



 

 




