---
description: Détails du suivi de modification du catalogue Winsock
ms.assetid: 4C86618D-4E79-486E-997F-9E2509FBF6B6
title: Détails du suivi de modification du catalogue Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6258ca87d5d1fba2de9364e5524110bb43c76513
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114287"
---
# <a name="winsock-catalog-change-tracing-details"></a>Détails du suivi de modification du catalogue Winsock

> [!Note]  
> Les fournisseurs de services en couche sont déconseillés. À compter de Windows 8 et de Windows Server 2012, utilisez la [plateforme de filtrage Windows](../fwp/windows-filtering-platform-start-page.md).

 

Le suivi des événements de modification du catalogue Winsock pour les fournisseurs de services en couche (LSP) est lié à l’installation du LSP, à la suppression du LSP, à la désactivation LSP et aux opérations de réinitialisation du catalogue Winsock. Tous les événements suivants sont écrits sur le canal *opérationnel Microsoft-Windows-Winsock-ws2help/Operational* , qui est différent de l’autre suivi d’événements réseau Winsock enregistré sur Windows Vista et versions ultérieures.

Les éléments suivants décrivent chacun des événements Winsock LSP qui peuvent être suivis et détaillent les paramètres et les informations qui sont journalisés.

## <a name="lsp-install"></a>Installation du LSP

ID d’événement = 1

Niveau = 4 (informations)

Les événements LSP Winsock suivants sont suivis pour une opération d’installation LSP :

-   Une entrée de protocole est installée dans le catalogue Winsock.

Les paramètres suivants sont consignés pour un événement d’installation LSP :



| Paramètre                                                                                                | Description                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>Nom LSP<br/>     | Nom du LSP obtenu à partir du membre **szProtocol** de la structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) pour le LSP en cours d’installation.<br/> |
| <span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalogue<br/>         | Le catalogue Winsock (32 bits ou 64 bits) sur lequel est installé le LSP. Il s’agit d’une valeur entière qui est 32 ou 64.<br/>                                   |
| <span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>D'<br/> | Nom de fichier du module de l’application effectuant l’appel d’installation LSP.<br/>                                                                                          |
| <span id="GUID"></span><span id="guid"></span>UNIQUES<br/>                                            | Valeur GUID du fournisseur de transport Winsock sous lequel le LSP est installé.<br/>                                                                      |
| <span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Catégorie<br/>     | Le membre **dwCatalogEntryId** de la structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) pour le LSP en cours d’installation.<br/>                                |



 

## <a name="lsp-uninstall"></a>Désinstallation de LSP

ID d’événement = 2

Niveau = 4 (informations)

Les événements LSP Winsock suivants sont suivis pour une opération de désinstallation LSP :

-   Une entrée de protocole est supprimée du catalogue Winsock.

Les paramètres suivants sont consignés pour un événement de désinstallation LSP :



| Paramètre                                                                                                | Description                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>Nom LSP<br/>     | Nom du LSP obtenu à partir du membre **szProtocol** de la structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) pour le LSP en cours de suppression.<br/> |
| <span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalogue<br/>         | Le catalogue Winsock (32 bits ou 64 bits) dans lequel le LSP est supprimé. Il s’agit d’une valeur entière qui est 32 ou 64.<br/>                                   |
| <span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>D'<br/> | Nom du fichier de module de l’application qui effectue l’appel de l’LSP de suppression.<br/>                                                                                         |
| <span id="GUID"></span><span id="guid"></span>UNIQUES<br/>                                            | Valeur GUID du fournisseur de transport Winsock duquel le LSP est supprimé.<br/>                                                                             |
| <span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Catégorie<br/>     | Membre **dwCatalogEntryId** de la structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) pour le LSP en cours de suppression.<br/>                                |



 

## <a name="lsp-disable"></a>Désactivation LSP

ID d’événement = 3

Niveau = 4 (informations)

Les événements LSP Winsock suivants sont suivis pour une opération de désactivation LSP :

-   Une entrée de protocole est désactivée dans le catalogue Winsock.

Les paramètres suivants sont consignés pour un événement de désactivation LSP :



| Paramètre                                                                                                | Description                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>Nom LSP<br/>     | Nom du LSP obtenu à partir du membre **szProtocol** de la structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) pour le LSP en cours de désactivation.<br/> |
| <span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalogue<br/>         | Le catalogue Winsock (32 bits ou 64 bits) sur lequel est désactivé le LSP. Il s’agit d’une valeur entière qui est 32 ou 64.<br/>                                   |
| <span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>D'<br/> | Nom du fichier de module de l’application qui effectue l’appel de désactivation du LSP.<br/>                                                                                         |
| <span id="GUID"></span><span id="guid"></span>UNIQUES<br/>                                            | Valeur GUID du fournisseur de transport Winsock sur lequel le LSP est désactivé.<br/>                                                                           |
| <span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Catégorie<br/>     | Le membre **dwCatalogEntryId** de la structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) pour le LSP en cours de désactivation.<br/>                                |



 

## <a name="winsock-catalog-reset"></a>Réinitialisation du catalogue Winsock

ID d’événement = 4

Niveau = 4 (informations)

Les événements LSP Winsock suivants sont suivis pour une opération de réinitialisation du catalogue Winsock :

-   Le catalogue Winsock est réinitialisé.

Les paramètres suivants sont enregistrés pour un événement de réinitialisation du catalogue Winsock :



| Paramètre                                                                                        | Description                                                                                                              |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalogue<br/> | Le catalogue Winsock (32 bits ou 64 bits) en cours de réinitialisation. Il s’agit d’une valeur entière qui est 32 ou 64.<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Contrôle du suivi Winsock](control-of-winsock-tracing.md)
</dt> <dt>

[Suivi Winsock](winsock-tracing.md)
</dt> <dt>

[Niveaux de suivi Winsock](winsock-tracing-levels.md)
</dt> <dt>

[Détails du suivi d’événements réseau Winsock](winsock-tracing-event-details.md)
</dt> </dl>

 

 
