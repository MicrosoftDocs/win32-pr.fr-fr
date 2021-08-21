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
ms.openlocfilehash: 737602777e02e4cdf88d2e07e3037ae940d257036a03a415271e4a6e1291dc7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117677927"
---
# <a name="parsefield-function"></a>ParseField fonction)

\[la fonction **ParseField** est actuellement censée être utilisée dans la prochaine version du système d’exploitation Microsoft Windows. Il peut être modifié ou non disponible dans les versions ultérieures.\]

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

Type : **LPCTSTR \***

Pointeur vers la ligne de Setup. inf.

</dd> <dt>

*n* \[ dans\]
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

Type : **LPTStr \***

Pointeur vers la mémoire tampon qui reçoit le champ extrait.

</dd> <dt>

*iBufLen* \[ dans\]
</dt> <dd>

Type : **int**

**Entier** qui reçoit la taille de la mémoire tampon qui reçoit le champ extrait.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **bool**

Retourne la **valeur true** si la fonction a réussi et **false** si elle échoue.

## <a name="remarks"></a>Remarques

Les champs de la chaîne doivent être séparés par des virgules.

Les espaces de début et de fin sont supprimés.

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Util. h</dt> </dl>                             |
| Bibliothèque<br/>                  | <dl> <dt>Shell32. lib</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



 

 




