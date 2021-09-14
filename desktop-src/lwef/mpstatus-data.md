---
title: Structure MPSTATUS_DATA (MpClient. h)
description: Contient des données sur l’état actuel d’un composant du produit.
ms.assetid: 6AEF485C-30D1-47DB-92B6-048B8CAA7833
keywords:
- fonctionnalités d’environnement Windows héritées de la structure MPSTATUS_DATA
- PMPSTATUS_DATA des fonctionnalités d’environnement du pointeur de structure Windows hérité
topic_type:
- apiref
api_name:
- MPSTATUS_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5da4ea9c8c51d8ee74d3242e5020df23f758228
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127236417"
---
# <a name="mpstatus_data-structure"></a>\_Structure de données MPSTATUS

Contient des données sur l’état actuel d’un composant du produit.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMPSTATUS_DATA {
  MPCOMPONENT_ID ComponentID;
  BOOL           fEnable;
  union {
    PMPSTATUS_DATAEX_UNUSED p1;
    PMPSTATUS_DATAEX_UNUSED p2;
    PMPSTATUS_DATAEX_UNUSED p3;
    PMPSTATUS_DATAEX_UNUSED p4;
    PMPSTATUS_DATAEX_UNUSED p5;
    PMPSTATUS_DATAEX_UNUSED p6;
    PMPSTATUS_DATAEX_UNUSED p7;
    PMPSTATUS_DATAEX_UNUSED p8;
    PMPSTATUS_DATAEX_UNUSED p9;
    PMPSTATUS_DATAEX_UNUSED pa;
    PMPSTATUS_DATAEX_UNUSED pb;
  } ComponentStatus;
} MPSTATUS_DATA, *PMPSTATUS_DATA;
```



## <a name="members"></a>Membres

<dl> <dt>

**ComponentID**
</dt> <dd>

Type : **[ **\_ ID MPCOMPONENT**](mpcomponent-id.md)**

</dd> <dd>

ID de composant spécifique pour lequel l’État est signalé.

</dd> <dt>

**fEnable**
</dt> <dd>

Type : **bool**

</dd> <dd>

État demandé pour le composant. **HRESULT** dans les données de rappel indique la réussite ou l’échec de la requête.

</dd> <dt>

**ComponentStatus**
</dt> <dd>

Données d’État supplémentaires en fonction de la valeur de **ComponentID**.

> [!Note]  
> Génère actuellement un pointeur vers une structure factice pour toutes les valeurs possibles de **ComponentID**.

 

<dl> <dt>

**P1**
</dt> <dd>

Type : **PMPSTATUS \_ DATAEX \_ inutilisé**

</dd> <dd>

Quand **ComponentID**  ==  **MPCOMPONENT \_ comme \_ signature**. Consultez [**MPSTATUS \_ DATAEX \_ inutilisé**](mpstatus-dataex-unused.md).

</dd> <dt>

**S2**
</dt> <dd>

Type : **PMPSTATUS \_ DATAEX \_ inutilisé**

</dd> <dd>

Lorsque l' **ID** de la  ==  **\_ \_ signature AV MPCOMPONENT**. Consultez [**MPSTATUS \_ DATAEX \_ inutilisé**](mpstatus-dataex-unused.md).

</dd> <dt>

**P3**
</dt> <dd>

Type : **PMPSTATUS \_ DATAEX \_ inutilisé**

</dd> <dd>

Quand l'  ==  **\_ \_ analyse en temps réel** de l’ID d’MPCOMPONENT. Consultez [**MPSTATUS \_ DATAEX \_ inutilisé**](mpstatus-dataex-unused.md).

</dd> <dt>

**P4**
</dt> <dd>

Type : **PMPSTATUS \_ DATAEX \_ inutilisé**

</dd> <dd>

Quand **ComponentID**  ==  **MPCOMPONENT \_ onaccess \_ protection**. Consultez [**MPSTATUS \_ DATAEX \_ inutilisé**](mpstatus-dataex-unused.md).

</dd> <dt>

**P5**
</dt> <dd>

Type : **PMPSTATUS \_ DATAEX \_ inutilisé**

</dd> <dd>

Quand **ComponentID**  ==  **MPCOMPONENT \_ IOAV \_ protection**. Consultez [**MPSTATUS \_ DATAEX \_ inutilisé**](mpstatus-dataex-unused.md).

</dd> <dt>

**P6**
</dt> <dd>

Type : **PMPSTATUS \_ DATAEX \_ inutilisé**

</dd> <dd>

Quand l'  ==  **\_ \_ analyse du comportement MPCOMPONENT** de l’ID de la. Consultez [**MPSTATUS \_ DATAEX \_ inutilisé**](mpstatus-dataex-unused.md).

</dd> <dt>

**P7**
</dt> <dd>

Type : **PMPSTATUS \_ DATAEX \_ inutilisé**

</dd> <dd>

Lors de l'  ==  **\_ \_ analyse automatique** de l’ID d’MPCOMPONENT. Consultez [**MPSTATUS \_ DATAEX \_ inutilisé**](mpstatus-dataex-unused.md).

</dd> <dt>

**P8**
</dt> <dd>

Type : **PMPSTATUS \_ DATAEX \_ inutilisé**

</dd> <dd>

Quand **ComponentID**  ==  **MPCOMPONENT \_ auto \_ SIGUPDATE**. Consultez [**MPSTATUS \_ DATAEX \_ inutilisé**](mpstatus-dataex-unused.md).

</dd> <dt>

**P9**
</dt> <dd>

Type : **PMPSTATUS \_ DATAEX \_ inutilisé**

</dd> <dd>

Quand **ComponentID**  ==  **MPCOMPONENT \_ IPC**. Consultez [**MPSTATUS \_ DATAEX \_ inutilisé**](mpstatus-dataex-unused.md).

</dd> <dt>

**activation**
</dt> <dd>

Type : **PMPSTATUS \_ DATAEX \_ inutilisé**

</dd> <dd>

Quand **ComponentID**  ==  **MPCOMPONENT \_ NIS**. Consultez [**MPSTATUS \_ DATAEX \_ inutilisé**](mpstatus-dataex-unused.md).

</dd> <dt>

**po**
</dt> <dd>

Type : **PMPSTATUS \_ DATAEX \_ inutilisé**

</dd> <dd>

Quand **ComponentID**  ==  **MPCOMPONENT \_ Elam**. Consultez [**MPSTATUS \_ DATAEX \_ inutilisé**](mpstatus-dataex-unused.md).

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_ID MPCOMPONENT**](mpcomponent-id.md)
</dt> <dt>

[**MPSTATUS \_ DATAEX \_ inutilisé**](mpstatus-dataex-unused.md)
</dt> </dl>

 

 





