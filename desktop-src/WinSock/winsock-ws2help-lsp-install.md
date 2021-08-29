---
description: Événement de modification du catalogue Winsock pour une opération d’installation d’un fournisseur de services en couche (LSP).
ms.assetid: 76A3D175-8CDC-486C-8341-D6314BCEC113
title: Événement WINSOCK_WS2HELP_LSP_INSTALL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_INSTALL
api_type:
- NA
api_location: ''
ms.openlocfilehash: 561dec21f08b5e8ad06ade54427789ece877d79af4c1b5412bb995b1ff25d065
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860599"
---
# <a name="winsock_ws2help_lsp_install-event"></a>Événement d’installation de l' \_ ws2help \_ LSP Winsock \_

> [!Note]  
> Les fournisseurs de services en couche sont déconseillés. à partir de Windows 8 et Windows Server 2012, utilisez la [plateforme de filtrage Windows](../fwp/windows-filtering-platform-start-page.md).

 

L’événement d' **installation de Winsock \_ ws2help \_ LSP \_** est un événement de modification du catalogue Winsock pour une opération d’installation d’un fournisseur de services en couche (LSP).


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_INSTALL = {0x1, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nom LSP* 
</dt> <dd>

Nom du LSP obtenu à partir du membre **szProtocol** de la structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) pour le LSP en cours d’installation.

</dd> <dt>

*Catalogue* 
</dt> <dd>

Le catalogue Winsock (32 bits ou 64 bits) sur lequel est installé le LSP. Il s’agit d’une valeur entière qui est 32 ou 64.

</dd> <dt>

*Programme d’installation* 
</dt> <dd>

Nom de fichier du module de l’application effectuant l’appel d’installation LSP.

</dd> <dt>

*GUID* 
</dt> <dd>

Valeur GUID du fournisseur de transport Winsock sous lequel le LSP est installé.

</dd> <dt>

*Catégorie* 
</dt> <dd>

Le membre **dwCatalogEntryId** de la structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) pour le LSP en cours d’installation.

</dd> </dl>

## <a name="remarks"></a>Remarques

L’événement d' **installation de Winsock \_ ws2help \_ LSP \_** est suivi pour une opération d’installation LSP lorsqu’une entrée de protocole est installée dans le catalogue Winsock.

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

 

 
