---
description: 'En savoir plus sur : JET_PCWSTR'
title: JET_PCWSTR
TOCTitle: JET_PCWSTR
ms:assetid: fef64bb9-c2e0-4cfb-8138-c98ae6f50952
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294145(v=EXCHG.10)
ms:contentKeyID: 32765759
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1eda03d9c08e0e18f1a60e088405919f3982e9de
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476151"
---
# <a name="jet_pcwstr"></a>JET_PCWSTR


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_pcwstr"></a>JET_PCWSTR

Le type de données **JET_PCWSTR** contient une chaîne **Unicode** constante, qui se termine par un caractère null (char \* ).

**Windows vista : JET_PCWSTR** est introduite dans Windows vista.

```cpp
    typedef __nullterminated const WCHAR * JET_PCWSTR;
```

### <a name="data-types"></a>Types de données

JET_PCWSTR

Chaîne Unicode constante (Char) terminée par un caractère null \* .

### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista.</p> | | <p><strong>Serveur</strong></p> | <p>requiert Windows Server 2008.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 


