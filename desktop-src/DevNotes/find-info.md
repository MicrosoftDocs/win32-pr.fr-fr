---
description: Contient les informations de contexte de recherche.
ms.assetid: 4b865563-98c2-459b-bb2b-75420d51d6a7
title: Structure FIND_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FIND_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 7d6b6dea42c008178c22f6e342a64b2f8d193ec5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513304"
---
# <a name="find_info-structure"></a>Rechercher la \_ structure des informations

Contient les informations de contexte de recherche.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _FIND_INFO {
  TAGID     tiIndex;
  TAGID     tiCurrent;
  TAGID     tiEndIndex;
  TAG       tName;
  DWORD     dwIndexRec;
  DWORD     dwFlags;
  ULONGLONG ullKey;
  union {
    LPCTSTR szName;
    DWORD   dwName;
    GUID    *pguidName;
  };
} FIND_INFO, *PFIND_INFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**tiIndex**
</dt> <dd>

**TagId** de l’index dans lequel effectuer la recherche.

</dd> <dt>

**tiCurrent**
</dt> <dd>

**TagId** pour l’élément actuel qui a été localisé.

</dd> <dt>

**tiEndIndex**
</dt> <dd>

**TagId** pour le dernier enregistrement après FindFirst si l’index est unique.

</dd> <dt>

**tName**
</dt> <dd>

Type de l’élément à localiser. Consultez [types de balises](tag-types.md).

</dd> <dt>

**dwIndexRec**
</dt> <dd>

Compteur interne utilisé pour effectuer le suivi de l’emplacement de début de l’opération de recherche suivante dans l’index.

</dd> <dt>

**dwFlags**
</dt> <dd>

Ce membre peut être 0 ou **SHIMDB \_ \_ \_ clé unique d’index** (0x00000001), qui indique qu’il s’agit d’un index de clé unique.

</dd> <dt>

**ullKey**
</dt> <dd>

Clé de l’entrée en cours.

</dd> <dt>

**szName**
</dt> <dd>

Chaîne actuelle (si le type de balise est le **type de balise \_ \_ STRINGREF**).

</dd> <dt>

**dwName**
</dt> <dd>

Valeur **DWORD** actuelle (si le type de balise **est \_ \_ DWORD type de balise**).

</dd> <dt>

**pguidName**
</dt> <dd>

La valeur actuelle du GUID (si le type de balise est **\_ \_ Binary type de balise** et la balise est **tag \_ Database \_ ID**).

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SdbFindFirstDWORDIndexedTag**](sdbfindfirstdwordindexedtag.md)
</dt> </dl>

 

 




