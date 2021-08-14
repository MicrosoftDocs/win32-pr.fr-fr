---
description: cette rubrique s’applique à Windows XP Service Pack 2 ou version ultérieure. La \_ structure de connexion KSTOPOLOGY décrit une connexion de nœud dans un filtre de diffusion en continu de noyau (KS). Un nœud peut être connecté à un autre nœud dans le filtre ou à un code confidentiel sur le filtre.
ms.assetid: 8fca47b7-4c52-46db-809c-77a0e3414276
title: KSTOPOLOGY_CONNECTION, structure (KS. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KSTOPOLOGY_CONNECTION
api_type:
- HeaderDef
api_location:
- Ks.h
ms.openlocfilehash: 80a7b6f046edd1cd7f602487a11d6a79c375276814f9374f4142d148699bb8b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118397243"
---
# <a name="kstopology_connection-structure"></a>\_Structure de connexion KSTOPOLOGY

cette rubrique s’applique à Windows XP Service Pack 2 ou version ultérieure.

La structure de **\_ connexion KSTOPOLOGY** décrit une connexion de nœud dans un filtre de diffusion en continu de noyau (KS). Un nœud peut être connecté à un autre nœud dans le filtre ou à un code confidentiel sur le filtre.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  ULONG FromNode;
  ULONG FromNodePin;
  ULONG ToNode;
  ULONG ToNodePin;
} KSTOPOLOGY_CONNECTION, *PKSTOPOLOGY_CONNECTION;
```



## <a name="members"></a>Membres

<dl> <dt>

**FromNode**
</dt> <dd>

Index du nœud amont dans la connexion. Si la connexion amont est un code confidentiel, et non un nœud, la valeur est KSFILTER \_ node.

</dd> <dt>

**FromNodePin**
</dt> <dd>

Si la valeur du champ **FromNode** est KSFILTER \_ nœud, ce champ spécifie l’index de la broche amont. Dans le cas contraire, ce champ est ignoré.

</dd> <dt>

**ToNode**
</dt> <dd>

Index du nœud en aval dans la connexion. Si la connexion en aval est un code confidentiel, et non un nœud, la valeur est KSFILTER \_ node.

</dd> <dt>

**ToNodePin**
</dt> <dd>

Si la valeur du champ **ToNode** est KSFILTER \_ nœud, ce champ spécifie l’index du code confidentiel en aval. Dans le cas contraire, ce champ est ignoré.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>KS. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[DirectShow Celles](directshow-structures.md)
</dt> <dt>

[**IKsTopologyInfo :: obtient \_ ConnectionInfo**](/previous-versions/windows/desktop/api/Vidcap/nf-vidcap-ikstopologyinfo-get_connectioninfo)
</dt> </dl>

 

 




