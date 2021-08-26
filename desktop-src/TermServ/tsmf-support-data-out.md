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
ms.openlocfilehash: 8577266c2e259e7a7e4bb70310837eee1d743905e0e0d166e5797bc51a1f1b45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869019"
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

 

 





