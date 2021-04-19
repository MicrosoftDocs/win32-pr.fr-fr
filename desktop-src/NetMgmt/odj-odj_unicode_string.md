---
title: ODJ_UNICODE_STRING
description: Définition du ODJ_UNICODE_STRING IDL
ms.assetid: a7999df0-d961-4fd7-ae5e-65ad79a9c17c
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f1134d7b95cca6948932bf9d79fe976d6745448a
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/14/2020
ms.locfileid: "106511719"
---
# <a name="odj_unicode_string-structure"></a>Structure ODJ_UNICODE_STRING

Contient une chaîne Unicode.

## <a name="syntax"></a>Syntaxe

```C++
typedef struct _ODJ_UNICODE_STRING
{
    USHORT Length;
    USHORT MaximumLength;
    [size_is(MaximumLength/2), length_is(Length/2)] PWSTR Buffer;
} ODJ_UNICODE_STRING, *PODJ_UNICODE_STRING;
```

## <a name="members"></a>Membres

### <a name="length"></a>Longueur

Doit être défini sur le nombre d’octets dans la mémoire tampon contenant la chaîne, à l’exclusion de la marque de fin NULL.

### <a name="maximumlength"></a>MaximumLength

Elle doit être définie sur le nombre total d’octets dans la mémoire tampon, à l’exclusion de la marque de fin NULL.

### <a name="buffer"></a>Buffer

Il doit s'agir d'une chaîne Unicode.

## <a name="see-also"></a>Voir aussi

[**Définitions IDL de jonction de domaine hors connexion**](odj-idl.md)
