---
description: La structure SET définit un ensemble de valeurs.
ms.assetid: 88e0ffa1-71a2-4a3f-bdf1-964de0adea62
title: DÉFINIR la structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SET
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: fdefc6f1233f820321bae6795f457e345fb5d4b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202867"
---
# <a name="set-structure"></a>DÉFINIR la structure

La structure **Set** définit un ensemble de valeurs.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _SET {
  DWORD nEntries;
  union {
    LPBYTE               lpByteTable;
    LPWORD               lpWordTable;
    LPDWORD              lpDwordTable;
    LPLARGEINT           lpLargeIntTable;
    LPSYSTEMTIME         lpSystemTimeTable;
    LPLABELED_BYTE       lpLabeledByteTable;
    LPLABELED_WORD       lpLabeledWordTable;
    LPLABELED_DWORD      lpLabeledDwordTable;
    LPLABELED_LARGEINT   lpLabeledLargeIntTable;
    LPLABELED_SYSTEMTIME lpLabeledSystemTimeTable;
    LPLABELED_BIT        lpLabeledBit;
    LPVOID               lpVoidTable;
  };
} SET, *LPSET;
```



## <a name="members"></a>Membres

<dl> <dt>

**nEntries**
</dt> <dd>

Nombre total d’entrées dans un jeu.

</dd> <dt>

**lpByteTable**
</dt> <dd>

Pointeur vers un tableau de valeurs d’octets.

</dd> <dt>

**lpWordTable**
</dt> <dd>

Pointeur vers un tableau de valeurs de mot.

</dd> <dt>

**lpDwordTable**
</dt> <dd>

Pointeur vers un tableau de valeurs DWORD.

</dd> <dt>

**lpLargeIntTable**
</dt> <dd>

Pointeur vers un tableau de structures [LARGEINT](largeint.md) .

</dd> <dt>

**lpSystemTimeTable**
</dt> <dd>

Pointeur vers un tableau de valeurs SYSTEMTIME.

</dd> <dt>

**lpLabeledByteTable**
</dt> <dd>

Pointeur vers un tableau de structures d' [ \_ octets étiquetées](labeled-byte.md) . Chaque structure d' **\_ octets étiquetée** définit une valeur et une étiquette. Moniteur réseau affiche une étiquette s’il trouve une valeur correspondante dans le paquet de protocole.

</dd> <dt>

**lpLabeledWordTable**
</dt> <dd>

Pointeur vers un tableau de structures de [ \_ mots étiquetées](labeled-word.md) qui définissent un ensemble de valeurs de mots et d’étiquettes.

</dd> <dt>

**lpLabeledDwordTable**
</dt> <dd>

Pointeur vers un tableau de [structures \_ DWORD étiquetées](labeled-dword.md) qui définissent un ensemble de valeurs et d’étiquettes DWORD.

</dd> <dt>

**lpLabeledLargeIntTable**
</dt> <dd>

Pointeur vers un tableau de [structures \_ LARGEINT étiquetées](labeled-largeint.md) qui définissent un ensemble de valeurs et d’étiquettes LARGEINT.

</dd> <dt>

**lpLabeledSystemTimeTable**
</dt> <dd>

Pointeur vers un tableau de [structures \_ SystemTime étiquetées](labeled-systemtime.md) qui définissent un ensemble de valeurs système et d’étiquettes.

</dd> <dt>

**lpLabeledBit**
</dt> <dd>

Pointeur vers un tableau de [structures \_ binaires étiquetées](labeled-bit.md) qui définissent un jeu de paires de bits étiquetées. Chaque BIT peut spécifier deux étiquettes, une étiquette pour chaque État (0 ou 1) du BIT.

</dd> <dt>

**lpVoidTable**
</dt> <dd>

Pointeur vers un tableau de valeurs.

</dd> </dl>

## <a name="remarks"></a>Notes

La structure **Set** est utilisée pour définir un ensemble de données de comparaison que Moniteur réseau pouvez utiliser pour interpréter la valeur d’une propriété dans un paquet de protocole. Lorsqu’un jeu de données de comparaison est requis, un pointeur vers la structure **Set** est spécifié dans le membre **lpSet** de la structure [PROPERTYINFO](propertyinfo.md) .

La DLL de l’analyseur peut fournir un jeu de valeurs et un ensemble d’étiquettes. Le membre de l' **Union** que vous sélectionnez dans une structure **Set** pointe vers un tableau de structures qui définissent chaque membre d’un jeu.

-   Valeur définie

    Un jeu de valeurs est utilisé lorsque vous souhaitez Moniteur réseau inclure un indicateur in-set ou not-in-set avec la valeur trouvée dans le paquet de protocole. Par exemple, si un jeu de DWORDs est spécifié, Moniteur réseau affiche une étiquette pour chaque valeur DWORD trouvée dans le paquet de protocole, indiquant que la valeur DWORD est ou n’est pas spécifiée dans le jeu.

    Un jeu de valeurs peut être basé sur des types de données BYTE, WORD, DWORD, LARGEINT et SYSTEMTIME.

-   Ensemble d’étiquettes

    Un jeu d’étiquettes est utilisé lorsque vous souhaitez Moniteur réseau afficher une étiquette définie par l’utilisateur au lieu des valeurs de propriété spécifiées dans un jeu.

    Un jeu d’étiquettes peut être basé sur des paires d’étiquettes BYTE, WORD, DWORD, LARGEINT, SYSTEMTIME et BIT.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[\_bit étiqueté](labeled-bit.md)
</dt> <dt>

[PROPERTYINFO](propertyinfo.md)
</dt> </dl>

 

 




