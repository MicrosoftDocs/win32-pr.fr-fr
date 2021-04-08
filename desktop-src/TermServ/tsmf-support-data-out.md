---
title: Structure TSMF_SUPPORT_DATA_OUT
description: Contient des informations sur les formats multimédias. | Structure TSMF_SUPPORT_DATA_OUT
ms.assetid: 987ede31-ad15-489f-90e5-fb707c6b38a9
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_DATA_OUT structure Services Bureau à distance
- Pointeur de structure PTSMF_SUPPORT_DATA_OUT Services Bureau à distance
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_DATA_OUT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9705c4c2c27eaff904e09364b029bd74ebd05d6c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103953570"
---
# <a name="tsmf_support_data_out-structure"></a>TSMF \_ prendre en charge la \_ \_ structure Data Out

Contient des informations sur les formats multimédias. Cette structure est utilisée par la méthode [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty) lors des requêtes de **\_ \_ \_ \_ prise en charge du format de requête MF Wrds** .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagTSMF_SUPPORT_DATA_OUT {
  GUID                      guidMfSession;
  UINT32                    numEntries;
  TSMF_SUPPORT_NODEDATA_OUT ...;
} TSMF_SUPPORT_DATA_OUT, *PTSMF_SUPPORT_DATA_OUT;
```



## <a name="members"></a>Membres

<dl> <dt>

**guidMfSession**
</dt> <dd>

Cela doit correspondre à la propriété **guidMfSession** dans les [**\_ données de prise en charge TSMF correspondantes \_ \_ dans**](tsmf-support-data-in.md) la structure.

</dd> <dt>

**numEntries**
</dt> <dd>

Nombre de structures dans les données de longueur variable.

</dd> <dt>

**...**
</dt> <dd>

Nombre variable de structures contenant des données au format de média.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>         |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty)
</dt> <dt>

[**TSMF \_ support \_ NODEDATA \_ out**](tsmf-support-nodedata-out.md)
</dt> </dl>

 

 





