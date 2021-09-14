---
title: Structure MPTHREAT_LOCALIZED_INFO (MpClient. h)
description: Informations localisées pour une menace.
ms.assetid: 99DC9737-9A61-4407-B544-A7A979C5B556
keywords:
- fonctionnalités d’environnement Windows héritées de la structure MPTHREAT_LOCALIZED_INFO
- PMPTHREAT_LOCALIZED_INFO des fonctionnalités d’environnement du pointeur de structure Windows hérité
topic_type:
- apiref
api_name:
- MPTHREAT_LOCALIZED_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87ea0bee7c8cae15389b40b64038aad92a56dd5f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127227820"
---
# <a name="mpthreat_localized_info-structure"></a>MPTHREAT \_ structure des \_ informations localisées

Informations localisées pour une menace.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMPTHREAT_LOCALIZED_INFO {
  MPTHREAT_ID           ThreatID;
  MP_MIDL_STRING LPWSTR CategoryName;
  MP_MIDL_STRING LPWSTR CategoryDescription;
  MP_MIDL_STRING LPWSTR SeverityName;
  MP_MIDL_STRING LPWSTR SeverityDescription;
  MP_MIDL_STRING LPWSTR ShortDescription;
  MP_MIDL_STRING LPWSTR DefaultActionName;;
  MP_MIDL_STRING LPWSTR Advice;
  MP_MIDL_STRING LPWSTR ThreatUrl;
} MPTHREAT_LOCALIZED_INFO, *PMPTHREAT_LOCALIZED_INFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**ThreatID**
</dt> <dd>

Type : **\_ ID MPTHREAT**

</dd> <dd>

Identificateur de la menace. Le bit supérieur est défini pour identifier les menaces liées à l’antivirus.

</dd> <dt>

**NomCatégorie**
</dt> <dd>

Type : **MP \_ MIDL \_ String** de type LPWStr

</dd> <dd>

Classification des menaces, comme un cheval de Troie ou un enregistreur d’enregistreur.

</dd> <dt>

**CategoryDescription**
</dt> <dd>

Type : **MP \_ MIDL \_ String** de type LPWStr

</dd> <dd>

Description de la catégorie de menace.

</dd> <dt>

**SeverityName**
</dt> <dd>

Type : **MP \_ MIDL \_ String** de type LPWStr

</dd> <dd>

Niveau de gravité de la menace, par exemple grave ou modéré.

</dd> <dt>

**SeverityDescription**
</dt> <dd>

Type : **MP \_ MIDL \_ String** de type LPWStr

</dd> <dd>

Description du niveau de gravité de la menace.

</dd> <dt>

**ShortDescription**
</dt> <dd>

Type : **MP \_ MIDL \_ String** de type LPWStr

</dd> <dd>

Description sommaire de la menace.

</dd> <dt>

**DefaultActionName;**
</dt> <dd>

Type : **MP \_ MIDL \_ String** de type LPWStr

</dd> <dd>

Nom de l’action par défaut, par exemple supprimer ou mettre en quarantaine, suggéré par le moteur.

</dd> <dt>

**Conseils**
</dt> <dd>

Type : **MP \_ MIDL \_ String** de type LPWStr

</dd> <dd>

Conseils pour une menace particulière.

</dd> <dt>

**ThreatUrl**
</dt> <dd>

Type : **MP \_ MIDL \_ String** de type LPWStr

</dd> <dd>

URL d’une page Web contenant des informations sur la menace.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





