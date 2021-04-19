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
ms.openlocfilehash: 219eb85dec0cdda77ca8741ae42df1f63d1a7dbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545841"
---
# <a name="winsock_ws2help_lsp_reset-event"></a>\_Événement de \_ réinitialisation du LSP Winsock ws2help \_

> [!Note]  
> Les fournisseurs de services en couche sont déconseillés. À compter de Windows 8 et de Windows Server 2012, utilisez la [plateforme de filtrage Windows](../fwp/windows-filtering-platform-start-page.md).

 

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

## <a name="remarks"></a>Notes

L’événement de **\_ \_ \_ réinitialisation Winsock ws2help LSP** est suivi pour une opération du fournisseur de services en couche (LSP) Winsock lors de la réinitialisation du catalogue Winsock.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



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

 

 
