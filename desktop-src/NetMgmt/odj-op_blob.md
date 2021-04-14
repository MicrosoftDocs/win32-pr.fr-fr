---
title: OP_BLOB
description: Définition du OP_BLOB IDL
ms.assetid: c215c793-5fad-4baa-97c0-c809040dda1e
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: fab6df11be3bf719f787c40a41a50d948a865474
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/14/2020
ms.locfileid: "104383176"
---
# <a name="op_blob-structure"></a>Structure OP_BLOB

Contient une mémoire tampon d’octets opaque.

## <a name="syntax"></a>Syntaxe

```C++
typedef struct _OP_BLOB
{
    ULONG                       cbBlob;
    [size_is(cbBlob)]   PBYTE   pBlob;
} OP_BLOB, *POP_BLOB;
```

## <a name="members"></a>Membres

### <a name="cbblob"></a>cbBlob

Spécifie la taille de pBlob en octets.

### <a name="pblob"></a>pBlob

Pointe vers une mémoire tampon d’octets.

## <a name="see-also"></a>Voir aussi

[**Définitions IDL de jonction de domaine hors connexion**](odj-idl.md)
