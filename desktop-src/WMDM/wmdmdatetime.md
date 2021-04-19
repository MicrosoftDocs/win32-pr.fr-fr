---
title: WMDMDATETIME, structure
description: La structure WMDMDATETIME contient une date et une heure.
ms.assetid: 47f3994d-66c6-47e4-803d-0c98c70eccc8
keywords:
- Structure WMDMDATETIME Windows Media Gestionnaire de périphériques
- Pointeur de structure PWMDMDATETIME Windows Media Gestionnaire de périphériques
topic_type:
- apiref
api_name:
- WMDMDATETIME
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07acf706aa63a21edd27fb2ac206db3039249055
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528375"
---
# <a name="wmdmdatetime-structure"></a>WMDMDATETIME, structure

La structure **WMDMDATETIME** contient une date et une heure.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _WMDMDATETIME {
  WORD wYear;
  WORD wMonth;
  WORD wDay;
  WORD wHour;
  WORD wMinute;
  WORD wSecond;
} WMDMDATETIME, *PWMDMDATETIME;
```



## <a name="members"></a>Membres

<dl> <dt>

**wYear**
</dt> <dd>

Mot contenant l’année à quatre chiffres.

</dd> <dt>

**wMonth**
</dt> <dd>

Mot contenant le mois (1-12).

</dd> <dt>

**wDay**
</dt> <dd>

Mot contenant le jour du mois (1-31).

</dd> <dt>

**wHour**
</dt> <dd>

Mot contenant l’heure (0-23).

</dd> <dt>

**wMinute**
</dt> <dd>

Mot contenant la minute (0-59).

</dd> <dt>

**wSecond**
</dt> <dd>

Mot contenant le deuxième (0-59).

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMDSPStorage :: GetDate**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getdate)
</dt> <dt>

[**IWMDMStorage :: GetDate**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getdate)
</dt> <dt>

[**WMDMRIGHTS**](wmdmrights.md)
</dt> <dt>

[**Structures**](structures.md)
</dt> </dl>

 

 





