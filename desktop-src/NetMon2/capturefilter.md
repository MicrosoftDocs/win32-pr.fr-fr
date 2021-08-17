---
description: La structure CAPTUREFILTER contient des données de filtre de capture.
ms.assetid: 773187c6-31c7-4439-850d-1dd43d42f701
title: CAPTUREFILTER, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPTUREFILTER
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: de5ab95ab395d50afb41223a458342706da1df7434d524f21c230436b3b9c7b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796359"
---
# <a name="capturefilter-structure"></a>CAPTUREFILTER, structure

La structure **capturefilter** contient des données de filtre de capture.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _CAPTUREFILTER {
  DWORD          FilterFlags;
  LPBYTE         lpSapTable;
  LPWORD         lpEtypeTable;
  WORD           nSaps;
  WORD           nEtypes;
  LPADDRESSTABLE AddressTable;
  EXPRESSION     FilterExpression;
  TRIGGER        Trigger;
  DWORD          nFrameBytesToCopy;
  RESERVED       Reserved;
} CAPTUREFILTER, *LPCAPTUREFILTER;
```



## <a name="members"></a>Membres

<dl> <dt>

**FilterFlags**
</dt> <dd>

Indicateurs qui décrivent le contenu du filtre de capture.



| Valeur                                                                                                                                                                                                                                                                                                   | Signification                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="CAPTUREFILTER_FLAGS_INCLUDE_ALL_SAPS"></span><span id="capturefilter_flags_include_all_saps"></span><dl> <dt>**Capturefilter \_ \_Les indicateurs incluent \_ tous les \_ SAP**</dt> <dt>0x0001</dt> </dl>       | Comprend tous les SAP comme des trames acceptables.<br/>  |
| <span id="CAPTUREFILTER_FLAGS_INCLUDE_ALL_ETYPES"></span><span id="capturefilter_flags_include_all_etypes"></span><dl> <dt>**Capturefilter \_ \_Les indicateurs incluent \_ tous les \_ ETYPE**</dt> <dt>0x0002</dt> </dl> | Inclure tous les ETYPE comme trames acceptables.<br/> |
| <span id="CAPTUREFILTER_FLAGS_LOCAL_ONLY"></span><span id="capturefilter_flags_local_only"></span><dl> <dt>**Capturefilter \_ INDICATEURS \_ locaux \_ uniquement**</dt> <dt>0x0008</dt> </dl>                          | Aucun mode P<br/>                                |
| <span id="CAPTUREFILTER_FLAGS_KEEP_RAW"></span><span id="capturefilter_flags_keep_raw"></span><dl> <dt>**Capturefilter \_ INDICATEURS \_ Keep \_ RAW**</dt> <dt>0x0020</dt> </dl>                                | Conservez les trames SMT et Token Ring MAC.<br/>      |



 

</dd> <dt>

**lpSapTable**
</dt> <dd>

Pointeur vers un tableau de valeurs SAP. Ce membre indique les valeurs SAP qui sont valides pour passer au pilote. Si \_ les indicateurs capturefilter \_ incluent \_ tous les \_ SAP sont définis, cela devient une liste d’exceptions (y compris tous les SAP sauf ceux-ci).

</dd> <dt>

**lpEtypeTable**
</dt> <dd>

Pointeur vers un tableau de valeurs ETYPE. Cela indique les valeurs ETYPE qui sont valides pour passer au pilote. Si \_ les indicateurs capturefilter \_ incluent \_ tous les \_ ETYPE sont définis, cela devient une liste d’exceptions (y compris tous les ETYPE, sauf celles-ci).

</dd> <dt>

**nSaps**
</dt> <dd>

Nombre de SAP dans la table SAP.

</dd> <dt>

**nEtypes**
</dt> <dd>

Nombre de ETYPE dans la table ETYPE.

</dd> <dt>

**AddressTable**
</dt> <dd>

Nom de la table d’adresses.

</dd> <dt>

**FilterExpression**
</dt> <dd>

Structure d’EXPRESSION. Contient la partie de correspondance de modèle du filtre de capture.

</dd> <dt>

**Déclencheur**
</dt> <dd>

Réservé.

</dd> <dt>

**nFrameBytesToCopy**
</dt> <dd>

Si ce membre n’est pas égal à 0, il spécifie le nombre d’octets à conserver pour chaque trame reçue. Si la valeur est 0, conservez la totalité du frame.

</dd> <dt>

**Reserved**
</dt> <dd>

Réservé.

</dd> </dl>

## <a name="remarks"></a>Remarques

La combinaison d’indicateurs, de valeurs et d’expressions détermine les frames qui seront transmis par le pilote qui utilise ces données de structure. Pour plus d’informations sur l’implémentation d’une structure **capturefilter** , consultez [filtres de capture](capture-filters.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ADDRESSTABLE](addresstable.md)
</dt> <dt>

[ADDRESSPAIR](addresspair.md)
</dt> <dt>

[FORMULE](expression.md)
</dt> <dt>

[ANDEXP](andexp.md)
</dt> <dt>

[PATTERNMATCH](patternmatch.md)
</dt> </dl>

 

 




