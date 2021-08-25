---
title: ODJ_UNICODE_STRING
description: Définition du ODJ_UNICODE_STRING IDL
ms.assetid: a7999df0-d961-4fd7-ae5e-65ad79a9c17c
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 3578c62f110eafd053ed97bbe1f8b5015156d02c4b879ff8111ff13f28dfab33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891238"
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
