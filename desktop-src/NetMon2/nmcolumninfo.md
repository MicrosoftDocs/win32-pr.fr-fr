---
description: La structure NMCOLUMNINFO définit une colonne dans le volet supérieur de la observateur d’événements.
ms.assetid: 21e0a129-464b-45b3-9c6b-6594e62fbce9
title: NMCOLUMNINFO, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EVENTCOLUMNINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 2597b486590871f0af28736717d4c2f332aae342
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194624"
---
# <a name="nmcolumninfo-structure"></a>NMCOLUMNINFO, structure

La structure **NMCOLUMNINFO** définit une colonne dans le volet supérieur de la observateur d’événements.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  LPSTR           szColumnName;
  NMCOLUMNVARIANT VariantData;
} EVENTCOLUMNINFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**szColumnName**
</dt> <dd>

Nom affichable d’une colonne spécifique. Si le nom est trop long, il ne sera pas complètement visible dans la configuration de observateur d’événements par défaut.

</dd> <dt>

**VariantData**
</dt> <dd>

Données insérées dans la colonne.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




