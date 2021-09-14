---
description: 'En savoir plus sur : JET_PCSTR'
title: JET_PCSTR
TOCTitle: JET_PCSTR
ms:assetid: 5826e6b9-5297-421f-abaa-016708bf16f6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269254(v=EXCHG.10)
ms:contentKeyID: 32765556
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
ms.openlocfilehash: 6a698afffb415bb4418f46cfe16091ceda03cb59
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126917292"
---
# <a name="jet_pcstr"></a>JET_PCSTR


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_pcstr"></a>JET_PCSTR

Le type de données **JET_PCSTR** contient une chaîne **ASCII** constante (Char) terminée par un caractère null \* .

**Windows vista : JET_PCSTR** est introduite dans Windows vista.

```cpp
    typedef __nullterminated const char *  JET_PCSTR;
```

### <a name="data-types"></a>Types de données

JET_PCSTR

Chaîne ASCII constante (Char) terminée par un caractère null \* .

### <a name="requirements"></a>Spécifications


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista.</p> | 
| <p><strong>Serveur</strong></p> | <p>requiert Windows Server 2008.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 


