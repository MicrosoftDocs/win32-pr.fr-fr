---
title: ODJ_BLOB
description: Définition du ODJ_BLOB IDL
ms.assetid: ada2c597-9ab9-4cc0-b5ba-4b533eec5502
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 079ea531b0cb392539679c10574c0cc0f1601318
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/14/2020
ms.locfileid: "104463890"
---
# <a name="odj_blob-structure"></a>Structure ODJ_BLOB

Spécifie une structure contenant soit une structure de ODJ_WIN7BLOB sérialisée, soit une structure de OP_PACKAGE sérialisée.

## <a name="syntax"></a>Syntaxe

```c++
typedef struct _ODJ_BLOB
{
    ULONG ulODJFormat;
    ULONG cbBlob;
    [size_is(cbBlob)] PBYTE pBlob;
} ODJ_BLOB, *PODJ_BLOB;

```

## <a name="members"></a>Membres

### <a name="ulodjformat"></a>ulODJFormat

Spécifie la version logique de la structure et doit être défini sur l’une des valeurs suivantes :

|Valeur|Signification|
| --- | --- |
|ODJ_WIN7_FORMAT (0x00000001)|Les octets contenus dans pBlob doivent contenir une structure ODJ_WIN7_BLOB sérialisée.|
|ODJ_WIN8_FORMAT (0x00000002)|Les octets contenus dans pBlob doivent contenir une structure OP_PACKAGE sérialisée.|

### <a name="cbblob"></a>cbBlob

Doit être défini sur le nombre d’octets dans le tableau pBlob.

### <a name="pblob"></a>pBlob

Pointe vers une mémoire tampon d’octets qui contient une structure sérialisée telle que spécifiée par ulODJFormat ci-dessus.

## <a name="see-also"></a>Voir aussi

[**Définitions IDL de jonction de domaine hors connexion**](odj-idl.md)

