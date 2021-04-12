---
title: Paramètres de l’appareil
description: Paramètres de l’appareil
ms.assetid: d8774c85-b5c0-4d9e-8a8e-d60ffdf59549
keywords:
- Windows Media Gestionnaire de périphériques, paramètres de l’appareil
- Gestionnaire de périphériques, paramètres de l’appareil
- Guide de programmation, paramètres de l’appareil
- fournisseurs de services, paramètres de l’appareil
- création de fournisseurs de services, paramètres d’appareil
- paramètres de l’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb3ad1a1bfc6a24736fdad8385e6cc03e0b20be2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309769"
---
# <a name="device-parameters"></a>Paramètres de l’appareil

Windows Media Gestionnaire de périphériques utilise des paramètres d’appareil pour contrôler le comportement d’un appareil. Ces paramètres sont ajoutés au registre comme indiqué dans le fichier d’installation de l’appareil (fichier INF). Le tableau suivant répertorie les paramètres de l’appareil que Windows Media Gestionnaire de périphériques requêtes.



| Nom du paramètre d’appareil | Type de données de Registre | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *WMDMSPCLSID*         | **SZ de REG \_**        | Valeur qui spécifie le CLSID du fournisseur de services contrôlant cet appareil. Ce paramètre est obligatoire pour la prise en charge PnP.<br/> La valeur du paramètre doit être le CLSID, et non le ProgID du fournisseur de services. Ce paramètre est obligatoire pour prendre en charge Plug-and-Play (PnP) sous Windows Media Gestionnaire de périphériques. Pour plus d’informations, consultez [activation de PNP pour les appareils](enabling-pnp-for-devices.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| *OptimalTransferSize* | **\_valeur DWORD reg**     | Valeur facultative qui spécifie la taille de transfert préférée que Windows Media Gestionnaire de périphériques utilise pendant les opérations de lecture et d’écriture. Si elle n’est pas fournie, une taille de transfert par défaut est utilisée.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| *UseMetadataViews*    | **\_valeur DWORD reg**     | Paramètre facultatif qui spécifie si Windows Media Gestionnaire de périphériques organise le contenu par métadonnées tout en présentant le contenu de l’appareil aux applications. En l'absence de spécification, la valeur par défaut est 0.<br/> Lorsque les applications énumèrent le contenu sur les stockages d’un lecteur audio portable, Windows Media Gestionnaire de périphériques peut présenter le contenu organisé par métadonnées. Cela s’avère particulièrement utile pour les appareils avec une capacité de stockage importante.<br/> Les applications et les appareils ont la possibilité de contrôler ce comportement. Les appareils indiquent leur préférence par le biais du paramètre d’appareil *UseMetadataViews*.<br/> Les deux valeurs entières suivantes sont prises en charge :<br/> Demande que le contenu soit présenté aux applications exactement telles qu’elles sont organisées sur le système de fichiers de l’appareil.<br/> Demande que le contenu soit présenté aux applications organisées par métadonnées.<br/> |
| *ShowInShell*         | **\_valeur DWORD reg**     | Paramètre facultatif qui spécifie si l’appareil doit apparaître dans l’Explorateur Windows. La valeur 1 indique que l’appareil doit apparaître dans l’Explorateur Windows. Pour plus d’informations, consultez [Configuration requise pour que les lecteurs audio portables s’affichent dans l’Explorateur Windows](requirements-for-portable-audio-players-to-appear-in-windows-explorer.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| *UseExtendedWmdm*     | **\_valeur DWORD reg**     | Paramètre facultatif qui signale à Windows Media Gestionnaire de périphériques que le fournisseur de services prend en charge **IMDSPDevice3**, **IMDSPObject2** et **IMDSPStorage4**. Sans cet indicateur, Windows Media Gestionnaire de périphériques n’appellera jamais ces interfaces. La valeur 1 indique que ces interfaces sont prises en charge.<br/> Cet indicateur est requis pour les fournisseurs de services qui se synchronisent avec le lecteur Windows Media. (Voir [activation de la synchronisation avec le lecteur Windows Media](enabling-synchronization-with-windows-media-player.md)).<br/>                                                                                                                                                                                                                                                                                                                                                                        |



 

**Codage du fichier INF**

L’exemple de code suivant à partir du fichier INF d’un appareil montre comment définir certains paramètres d’appareil lors de l’installation de l’appareil.


```C++
; Set parameters on Windows 95 and Windows 98 operating systems.
[DriverInstall.hw]
AddReg=DriverHwPropReg

; Set parameters on Windows NT-based operating systems.
[DriverInstall.NT.hw]
AddReg=DriverHwPropReg

; Related section that specifies the device parameters.
[DriverHwPropReg]
; Add your own CLSID here.
HKR,,WMDMSPCLSID,,"{00000000-0000-0000-0000-000000000000}"
HKR,,OptimalTransferSize,0x10001,0x10000
HKR,,UseMetadataViews,0x10001,0x1
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création d’un fournisseur de services**](creating-a-service-provider.md)
</dt> <dt>

[**Interface IMDServiceProvider2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider2)
</dt> <dt>

[**IMDServiceProvider2::CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice)
</dt> <dt>

[**Interface IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> </dl>

 

 





