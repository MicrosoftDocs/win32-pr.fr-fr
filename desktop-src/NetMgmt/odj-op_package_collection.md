---
title: OP_PACKAGE_PART_COLLECTION
description: Définition du OP_PACKAGE_PART_COLLECTION IDL
ms.assetid: a7abf011-0335-4869-b4d9-144b2f392241
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f8eb61397045a382fe5933025a4eeda2f563e838
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/14/2020
ms.locfileid: "104032045"
---
# <a name="op_package_part_collection-structure"></a>Structure OP_PACKAGE_PART_COLLECTION

Spécifie une structure qui contient un tableau de structures OP_PACKAGE_PART.

## <a name="syntax"></a>Syntaxe

```C++
typedef struct _OP_PACKAGE_PART_COLLECTION
{
    ULONG                                 cParts;
    [size_is(cParts)]   POP_PACKAGE_PART  pParts;
    OP_BLOB                               Extension;
} OP_PACKAGE_PART_COLLECTION, *POP_PACKAGE_PART_COLLECTION;
```

## <a name="members"></a>Membres

### <a name="cparts"></a>cParts

Contient le nombre d’éléments dans pParts.

### <a name="pparts"></a>pParts

Contient un tableau de structures OP_PACKAGE_PART.

### <a name="extension"></a>Extension

Réservé pour une utilisation ultérieure et doit être défini sur tous les zéros.

## <a name="see-also"></a>Voir aussi

[**Définitions IDL de jonction de domaine hors connexion**](odj-idl.md)

[**\_composant de package op \_**](odj-op_package_part.md)

[**\_objet BLOB op**](odj-op_blob.md)

