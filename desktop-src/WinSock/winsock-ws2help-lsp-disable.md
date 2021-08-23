---
description: Événement de modification du catalogue Winsock pour une opération de désactivation du fournisseur de services en couche (LSP).
ms.assetid: 6BCEECB1-92AD-47D8-952B-D0FD2A78EB45
title: Événement WINSOCK_WS2HELP_LSP_DISABLE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_DISABLE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 578479710856e149760202699be13d4b30b50709f6ea9b389e055793a8b0ca94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733129"
---
# <a name="winsock_ws2help_lsp_disable-event"></a>\_Événement de \_ \_ désactivation de l’LSP Winsock ws2help

> [!Note]  
> Les fournisseurs de services en couche sont déconseillés. à partir de Windows 8 et Windows Server 2012, utilisez la [plateforme de filtrage Windows](../fwp/windows-filtering-platform-start-page.md).

 

L’événement **Winsock \_ ws2help \_ LSP \_ Disable** est un événement de modification du catalogue Winsock pour une opération de désactivation du fournisseur de services en couche (LSP).


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_DISABLE = {0x3, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nom LSP* 
</dt> <dd>

Nom du LSP obtenu à partir du membre **szProtocol** de la structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) pour le LSP en cours de désactivation.

</dd> <dt>

*Catalogue* 
</dt> <dd>

Le catalogue Winsock (32 bits ou 64 bits) sur lequel est désactivé le LSP. Il s’agit d’une valeur entière qui est 32 ou 64.

</dd> <dt>

*Programme d’installation* 
</dt> <dd>

Nom du fichier de module de l’application qui effectue l’appel de désactivation du LSP.

</dd> <dt>

*GUID* 
</dt> <dd>

Valeur GUID du fournisseur de transport Winsock que le LSP est en cours de désactivation.

</dd> <dt>

*Catégorie* 
</dt> <dd>

Le membre **dwCatalogEntryId** de la structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) pour le LSP en cours de désactivation.

</dd> </dl>

Cet événement n’a pas de paramètres.

## <a name="remarks"></a>Remarques

L’événement de **\_ \_ \_ désactivation de l’LSP Winsock ws2help** est suivi pour une opération de désactivation LSP lorsqu’une entrée de protocole est désactivée dans le catalogue Winsock.

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

 

 
