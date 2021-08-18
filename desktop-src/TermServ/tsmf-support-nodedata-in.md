---
title: Structure TSMF_SUPPORT_NODEDATA_IN
description: Utilisé à l’intérieur des \_ données de prise en charge TSMF \_ dans la \_ structure pour contenir des informations sur les formats multimédias pris en charge.
ms.assetid: 9aee9d6d-2182-44ec-ba8b-d2747d3edf71
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_NODEDATA_IN structure Services Bureau à distance
- Pointeur de structure PTSMF_SUPPORT_NODEDATA_IN Services Bureau à distance
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_NODEDATA_IN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5e1920ca627a7da8aef2d49a6930b03f0906cfd912e2a2a584b20d8e8382b706
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755721"
---
# <a name="tsmf_support_nodedata_in-structure"></a>TSMF \_ prend en charge \_ NODEDATA \_ dans la structure

Utilisé à l’intérieur des [**\_ \_ données \_ de prise en charge TSMF dans**](tsmf-support-data-in.md) la structure pour contenir des informations sur les formats multimédias pris en charge.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagTSMF_SUPPORT_NODEDATA_IN {
  UINT32           byteCount;
  INT64            nodeId;
  UINT32           numMediaTypes;
  TS_AM_MEDIA_TYPE ...;
} TSMF_SUPPORT_NODEDATA_IN, *PTSMF_SUPPORT_NODEDATA_IN;
```



## <a name="members"></a>Membres

<dl> <dt>

**byteCount**
</dt> <dd>

Taille de la structure en octets.

</dd> <dt>

**ID**
</dt> <dd>

Nœud.

</dd> <dt>

**numMediaTypes**
</dt> <dd>

Nombre de structures de format de média.

</dd> <dt>

**...**
</dt> <dd>

Nombre variable de structures définissant les formats de média audio ou vidéo. Le **type de fichier** est **\_ WaveFormatEx** pour le format audio ou **\_ MFVideoFormat** pour la vidéo.

Pour plus d’informations sur cette structure, consultez [ \_ structure du \_ \_ type de média TS](/openspecs/windows_protocols/ms-rdpev/22a57950-042e-48bd-8135-3580f3a3f934).

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

[**\_ \_ données de support TSMF \_ dans**](tsmf-support-data-in.md)
</dt> </dl>

 

