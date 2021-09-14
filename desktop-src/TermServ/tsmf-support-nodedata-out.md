---
title: Structure TSMF_SUPPORT_NODEDATA_OUT
description: Utilisé dans la \_ \_ structure de données de prise en charge \_ de TSMF pour contenir des informations sur les formats multimédias pris en charge.
ms.assetid: cac0af9e-6750-4735-b075-46c77aea7d41
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_NODEDATA_OUT structure Services Bureau à distance
- Pointeur de structure PTSMF_SUPPORT_NODEDATA_OUT Services Bureau à distance
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_NODEDATA_OUT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 517170e9d6580f69b59f71e0994351ebe0484ddc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008591"
---
# <a name="tsmf_support_nodedata_out-structure"></a>TSMF \_ prise en charge de la \_ \_ structure NODEDATA out

Utilisé dans la structure de [**données de prise en charge de TSMF pour contenir des informations sur \_ \_ \_ les**](tsmf-support-data-out.md) formats multimédias pris en charge.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagTSMF_SUPPORT_NODEDATA_OUT {
  INT64   nodeId;
  HRESULT hrSupportStatus;
  CLSID   clsidNewSink;
  UINT32  supportedMediaTypeIndex;
} TSMF_SUPPORT_NODEDATA_OUT, *PTSMF_SUPPORT_NODEDATA_OUT;
```



## <a name="members"></a>Membres

<dl> <dt>

**ID**
</dt> <dd>

Nœud.

</dd> <dt>

**hrSupportStatus**
</dt> <dd>

Indique si le récepteur identifié par le paramètre *clsidNewSink* est pris en charge.

Les valeurs possibles sont.

<dt>

0
</dt> <dd>

Non pris en charge

</dd> <dt>

1
</dt> <dd>

Prise en charge

</dd> </dl>

Les autres valeurs ne sont pas définies.

</dd> <dt>

**clsidNewSink**
</dt> <dd>

Récepteur associé au type de média.

</dd> <dt>

**supportedMediaTypeIndex**
</dt> <dd>

Index de base zéro du type de média pris en charge par le récepteur.

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

[**TSMF \_ prennent en charge \_ \_ les données sortantes**](tsmf-support-data-out.md)
</dt> </dl>

 

 





