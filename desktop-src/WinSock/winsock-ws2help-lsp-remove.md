---
description: Événement de modification du catalogue Winsock pour une opération de suppression du fournisseur de services en couche (LSP).
ms.assetid: 86FF17F7-8CCF-4A03-899F-42BFACDF3F54
title: Événement WINSOCK_WS2HELP_LSP_REMOVE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_REMOVE
api_type:
- NA
api_location: ''
ms.openlocfilehash: b0ac13a5404dcbbfe5fb5f5d8c2a5f17d43edeb72ba135abfc7e85ad9e5227a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118321591"
---
# <a name="winsock_ws2help_lsp_remove-event"></a>\_Événement de \_ suppression LSP Winsock ws2help \_

> [!Note]  
> Les fournisseurs de services en couche sont déconseillés. à partir de Windows 8 et Windows Server 2012, utilisez la [plateforme de filtrage Windows](../fwp/windows-filtering-platform-start-page.md).

 

L’événement **Winsock \_ ws2help \_ LSP \_ Remove** est un événement de modification du catalogue Winsock pour une opération de suppression du fournisseur de services en couche (LSP).


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_REMOVE = {0x2, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nom LSP* 
</dt> <dd>

Nom du LSP obtenu à partir du membre **szProtocol** de la structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) pour le LSP en cours de suppression.

</dd> <dt>

*Catalogue* 
</dt> <dd>

Le catalogue Winsock (32 bits ou 64 bits) dans lequel le LSP est supprimé. Il s’agit d’une valeur entière qui est 32 ou 64.

</dd> <dt>

*Programme d’installation* 
</dt> <dd>

Nom du fichier de module de l’application qui effectue l’appel de l’LSP de suppression.

</dd> <dt>

*GUID* 
</dt> <dd>

Valeur GUID du fournisseur de transport Winsock duquel le LSP est supprimé.

</dd> <dt>

*Catégorie* 
</dt> <dd>

Membre **dwCatalogEntryId** de la structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) pour le LSP en cours de suppression.

</dd> </dl>

## <a name="remarks"></a>Remarques

L’événement **Winsock \_ ws2help \_ LSP \_ Remove** est suivi pour une opération de suppression LSP lorsqu’une entrée de protocole est supprimée du catalogue Winsock.

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

 

 
