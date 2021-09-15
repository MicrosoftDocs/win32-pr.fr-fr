---
description: 'En savoir plus sur : JET_LS'
title: JET_LS
TOCTitle: JET_LS
ms:assetid: 8e4e7902-84b1-404b-8654-bb430a0952aa
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269336(v=EXCHG.10)
ms:contentKeyID: 32765625
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
ms.openlocfilehash: 82a0df37215122e943955f32aeed4d39dd70b268
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127517824"
---
# <a name="jet_ls"></a>JET_LS


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_ls"></a>JET_LS

Le type de données **JET_LS** contient un descripteur de contexte pour le stockage local (LS). Ce handle peut être associé à un curseur ou à une table et peut faire référence à des ressources allouées dynamiquement.

**Windows xp : JET_LS** est introduite dans Windows xp.

```cpp
    typedef JET_API_PTR JET_LS;
```

### <a name="data-types"></a>Types de données

JET_LS

La valeur JET_LSNil indique un handle de contexte non valide.

### <a name="remarks"></a>Notes

Un descripteur de contexte est initialement associé à l' **JET_LS** type de données, à l’aide de [JetSetLS](./jetsetls-function.md). Le descripteur de contexte peut être récupéré à partir du type de données **JET_LS** à l’aide de [JetGetLS](./jetgetls-function.md).

Le descripteur de contexte peut être explicitement dissocié du type de données **JET_LS** à l’aide de [JetGetLS](./jetgetls-function.md) avec JET_bitLSReset. Le handle de contexte peut également être dissocié implicitement du type de données **JET_LS** lorsque l’objet sous-jacent est libéré par le moteur de base de données à la suite d’une action directe ou indirecte de l’application. Dans le cas implicite, un rappel d’exécution est émis pour l’application afin qu’elle puisse nettoyer le handle de contexte. Pour plus d’informations sur la dissociation implicite du type de données **JET_LS** , consultez [JetSetLS](./jetsetls-function.md).

Les indicateurs suivants sont associés au type de données JET_LS.


| <p>Terme</p> | <p>Description</p> | 
|-------------|--------------------|
| <p>JET_bitLSReset</p> | <p>Le handle de contexte est dissocié de l’objet.</p> | 
| <p>JET_bitLSCursor</p> | <p>Définissez ou récupérez le stockage local associé à un curseur de table.</p> | 
| <p>JET_bitLSTable</p> | <p>Définissez ou récupérez le stockage local associé à une table.</p> | 
| <p>JET_LSNil</p> | <p>Le descripteur de contexte n’est pas valide.</p> | 



### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista ou Windows XP.</p> | 
| <p><strong>Serveur</strong></p> | <p>requiert Windows server 2008 ou Windows server 2003.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[JetSetLS](./jetsetls-function.md)  
[JetGetLS](./jetgetls-function.md)
