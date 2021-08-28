---
description: La méthode GetFileCapabilities récupère une liste de fonctionnalités de fichier à partir du fichier actif.
ms.assetid: 0d24efd2-d411-4fb3-95c2-4742a58aeb5e
title: 'ISCardFileAccess :: GetFileCapabilities, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.GetFileCapabilities
api_type:
- COM
api_location: ''
ms.openlocfilehash: 650e0609f0498e103c3712f692bfedbff733b3076330feee78460ac9b571bc96
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119481189"
---
# <a name="iscardfileaccessgetfilecapabilities-method"></a>ISCardFileAccess :: GetFileCapabilities, méthode

\[La méthode **GetFileCapabilities** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **GetFileCapabilities** récupère une liste de fonctionnalités de fichier à partir du fichier actif.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetFileCapabilities(
  [in, out] LPTLV_TABLE *ppProperties,
  [in, out] LONG        *plProperties,
  [in]      SCARD_FLAGS Flags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppProperties* \[ in, out\]
</dt> <dd>

Structures de pointeur vers TLV (balise, longueur, valeur). En entrée, ce paramètre indique les fichiers pour lesquels obtenir des propriétés ; lors de la sortie, ce paramètre contient les propriétés. L’exemple suivant est une définition de la structure TLV.


```C++
#include <windows.h>

typedef struct
{
  DWORD  Tag;
  DWORD  Length;
  BYTE[]  Value;
  BOOL  Valid;
} TLV;
```



Pour plus d’informations sur les structures TLV, consultez [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/) .

</dd> <dt>

*plProperties* \[ in, out\]
</dt> <dd>

Pointeur vers le nombre d’entrées TLV dans *ppProperties*.

</dd> <dt>

*Indicateurs* \[ dans\]
</dt> <dd>

Spécifie si la messagerie sécurisée doit être utilisée et les données préallouées.

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

**\_ \_ messagerie sécurisée SC FL \_**
</dt><span id="SC_FL_PREALLOCATED"></span><span id="sc_fl_preallocated"></span><dt>

**SC \_ FL \_ préalloué**
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne l’une des valeurs possibles suivantes.



| Code de retour                                                                                   | Description                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | L’opération s’est terminée avec succès.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Paramètre non valide.<br/>                    |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Un pointeur incorrect a été passé.<br/>          |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante.<br/>                        |



 

## <a name="remarks"></a>Remarques

Pour obtenir la liste de toutes les méthodes définies par cette interface, consultez [**ISCardFileAccess**](iscardfileaccess.md).

Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de [*carte*](../secgloss/s-gly.md) à puce si une fonction de carte à puce a été appelée pour terminer la demande. Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/> |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ISCardFileAccess**](iscardfileaccess.md)
</dt> </dl>

 

 
