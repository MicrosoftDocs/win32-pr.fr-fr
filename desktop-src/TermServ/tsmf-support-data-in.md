---
title: Structure TSMF_SUPPORT_DATA_IN
description: Contient des informations sur les formats multimédias. | Structure TSMF_SUPPORT_DATA_IN
ms.assetid: cd1a8295-22b7-4d75-8325-94da4d7380d0
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_DATA_IN structure Services Bureau à distance
- Pointeur de structure PTSMF_SUPPORT_DATA_IN Services Bureau à distance
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_DATA_IN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2072363978cb0e70d64a09d855ed2861341e9cf0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324373"
---
# <a name="tsmf_support_data_in-structure"></a>\_Données de prise en charge TSMF \_ \_ dans la structure

Contient des informations sur les formats multimédias. Cette structure est utilisée par la méthode [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty) lors des requêtes de **\_ \_ \_ \_ prise en charge du format de requête MF Wrds** .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagTSMF_SUPPORT_DATA_IN {
  GUID                     guidMfSession;
  UINT32                   numEntries;
  TSMF_SUPPORT_NODEDATA_IN ...;
} TSMF_SUPPORT_DATA_IN, *PTSMF_SUPPORT_DATA_IN;
```



## <a name="members"></a>Membres

<dl> <dt>

**guidMfSession**
</dt> <dd>

Session.

</dd> <dt>

**numEntries**
</dt> <dd>

Nombre de structures dans les données de longueur variable.

</dd> <dt>

**...**
</dt> <dd>

Nombre variable de structures contenant des données au format de média.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>         |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty)
</dt> <dt>

[**TSMF \_ prend en charge \_ NODEDATA \_ dans**](tsmf-support-nodedata-in.md)
</dt> </dl>

 

 





