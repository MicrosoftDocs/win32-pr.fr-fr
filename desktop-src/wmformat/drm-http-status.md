---
title: Énumération DRM_HTTP_STATUS (Drmexternals. h)
description: Le \_ \_ type d’énumération de l’État http DRM définit une plage d’États pour une requête DRM.
ms.assetid: 9e0fb060-3fbf-45d0-872b-4d666ea9a88d
keywords:
- Format Windows Media d’énumération DRM_HTTP_STATUS
- Format Windows Media d’énumération
topic_type:
- apiref
api_name:
- DRM_HTTP_STATUS
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e222cbf24e6333c7105e8564a5ad255693340749aeea32d98bd013bcb40995d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586299"
---
# <a name="drm_http_status-enumeration-drmexternalsh"></a>Énumération DRM_HTTP_STATUS (Drmexternals. h)

Le type d’énumération de l' **\_ \_ État http DRM** définit une plage d’États pour une requête [*DRM*](wmformat-glossary.md) .

## <a name="syntax"></a>Syntaxe


```C++
typedef enum DRM_HTTP_STATUS { 
  HTTP_NOTINITIATED  = 0,
  HTTP_CONNECTING    = 1,
  HTTP_REQUESTING    = 2,
  HTTP_RECEIVING     = 3,
  HTTP_COMPLETED     = 4
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="HTTP_NOTINITIATED"></span><span id="http_notinitiated"></span>**\_NOTINITIATED http**
</dt> <dd>

Les opérations HTTP n’ont pas été initiées.

</dd> <dt>

<span id="HTTP_CONNECTING"></span><span id="http_connecting"></span>**\_connexion http**
</dt> <dd>

La connexion est en cours d’établissement.

</dd> <dt>

<span id="HTTP_REQUESTING"></span><span id="http_requesting"></span>**\_demande http**
</dt> <dd>

Les données sont demandées.

</dd> <dt>

<span id="HTTP_RECEIVING"></span><span id="http_receiving"></span>**\_réception http**
</dt> <dd>

Les données sont reçues.

</dd> <dt>

<span id="HTTP_COMPLETED"></span><span id="http_completed"></span>**HTTP \_ terminé**
</dt> <dd>

Les opérations HTTP sont terminées.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette énumération est utilisée par la structure d' [**\_ \_ État**](wm-individualize-status.md) de l’énumération WM.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                      |
| Version<br/>                  | Windows Media Format 7 SDK ou les versions ultérieures du kit de développement logiciel (SDK)<br/>                       |
| En-tête<br/>                   | <dl> <dt>Drmexternals. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**État de l' \_ individualisation DRM \_**](drm-individualization-status.md)
</dt> <dt>

[**Types énumération**](enumeration-types.md)
</dt> </dl>

 

 





