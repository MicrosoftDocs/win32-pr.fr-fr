---
description: 'En savoir plus sur : JET_OSSNAPID'
title: JET_OSSNAPID
TOCTitle: JET_OSSNAPID
ms:assetid: 89b15492-674a-46e4-8aea-991df4f22a6f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269325(v=EXCHG.10)
ms:contentKeyID: 32765615
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
ms.openlocfilehash: d6185f17c16cbdb2a45e172a14af346c3519aa12
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468366"
---
# <a name="jet_ossnapid"></a>JET_OSSNAPID


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_ossnapid"></a>JET_OSSNAPID

Le type de données **JET_OSSNAPID** contient un descripteur d’instantané de la base de données.

```cpp
    typedef JET_API_PTR JET_OSSNAPID;
```

### <a name="data-types"></a>Types de données

JET_OSSNAPID

Handle d’un instantané de la base de données. Ce descripteur est utilisé dans les éléments de l’API JET impliqués dans la sauvegarde d’instantané.

La **valeur null** peut être utilisée pour indiquer un handle non valide.

### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 


