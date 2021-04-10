---
title: SID_IDENTIFIER_AUTHORITY
description: Définition du SID_IDENTIFIER_AUTHORITY IDL
ms.assetid: 88fe41f4-1c67-4290-ac21-fd43ff12d825
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: d9a80ed0717a279f39ac7a105a95807911232c82
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/14/2020
ms.locfileid: "104102525"
---
# <a name="sid_identifier_authority-structure"></a>Structure SID_IDENTIFIER_AUTHORITY

Contient une autorité d’identificateur de SID.

## <a name="syntax"></a>Syntaxe

```C++
typedef struct _SID_IDENTIFIER_AUTHORITY
{
    UCHAR Value[6];
} SID_IDENTIFIER_AUTHORITY, *PSID_IDENTIFIER_AUTHORITY;
```

## <a name="members"></a>Membres

### <a name="value"></a>Valeur

Doit être défini sur les six octets de l’autorité d’identificateur SID.

## <a name="see-also"></a>Voir aussi

[**Définitions IDL de jonction de domaine hors connexion**](odj-idl.md)