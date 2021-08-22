---
description: Événement de modification du catalogue Winsock pour une opération de réinitialisation du catalogue Winsock.
ms.assetid: BE8DC0DB-0F96-4015-87F5-ECF25AE164AA
title: Événement WINSOCK_WS2HELP_LSP_RESET
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_RESET
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3c9a638d962db908b24387d7baeb2f34d4e09ece561fdd1796a8a44930a5dfb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051287"
---
# <a name="winsock_ws2help_lsp_reset-event"></a>\_Événement de \_ réinitialisation du LSP Winsock ws2help \_

> [!Note]  
> Les fournisseurs de services en couche sont déconseillés. à partir de Windows 8 et Windows Server 2012, utilisez la [plateforme de filtrage Windows](../fwp/windows-filtering-platform-start-page.md).

 

L’événement de **\_ \_ \_ réinitialisation de Winsock ws2help LSP** est un événement de modification de catalogue Winsock pour une opération de réinitialisation de catalogue Winsock.


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_RESET = {0x4, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Catalogue* 
</dt> <dd>

Le catalogue Winsock (32 bits ou 64 bits) en cours de réinitialisation. Il s’agit d’une valeur entière qui est 32 ou 64.

</dd> </dl>

## <a name="remarks"></a>Remarques

L’événement de **\_ \_ \_ réinitialisation Winsock ws2help LSP** est suivi pour une opération du fournisseur de services en couche (LSP) Winsock lors de la réinitialisation du catalogue Winsock.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Contrôle du suivi Winsock](control-of-winsock-tracing.md)
</dt> <dt>

[Suivi Winsock](winsock-tracing.md)
</dt> <dt>

[Niveaux de suivi Winsock](winsock-tracing-levels.md)
</dt> <dt>

[Détails du suivi de modification du catalogue Winsock](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
