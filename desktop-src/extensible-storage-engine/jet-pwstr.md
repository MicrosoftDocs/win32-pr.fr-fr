---
description: 'En savoir plus sur : JET_PWSTR'
title: JET_PWSTR
TOCTitle: JET_PWSTR
ms:assetid: 6575f0f0-d022-4e70-9f17-c1d884d9e226
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269271(v=EXCHG.10)
ms:contentKeyID: 32765573
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
ms.openlocfilehash: ca4478684e79dfb698dd30bb21132f597129fdac
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479335"
---
# <a name="jet_pwstr"></a>JET_PWSTR


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_pwstr"></a>JET_PWSTR

Le type de données **JET_PWSTR** contient une chaîne **Unicode** terminée par le caractère null (char \* ).

**Windows vista : JET_PWSTR** est introduite dans Windows vista.

```cpp
    typedef __nullterminated WCHAR * JET_PWSTR;
```

### <a name="data-types"></a>Types de données

JET_PWSTR

Chaîne Unicode terminée par un caractère null (char \* ).

### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista.</p> | | <p><strong>Serveur</strong></p> | <p>requiert Windows Server 2008.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 


