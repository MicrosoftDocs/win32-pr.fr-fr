---
title: Paramètres de l’appareil
description: Paramètres de l’appareil
ms.assetid: d8774c85-b5c0-4d9e-8a8e-d60ffdf59549
keywords:
- Windows Gestionnaire de périphériques de média, paramètres de l’appareil
- Gestionnaire de périphériques, paramètres de l’appareil
- Guide de programmation, paramètres de l’appareil
- fournisseurs de services, paramètres de l’appareil
- création de fournisseurs de services, paramètres d’appareil
- paramètres de l’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef097940670148551042c22fd8efc6aa51c641960bf0f821361aaf3c29c731d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585348"
---
# <a name="device-parameters"></a>Paramètres de l’appareil

Windows Media Gestionnaire de périphériques utilise des paramètres d’appareil pour contrôler le comportement d’un appareil. Ces paramètres sont ajoutés au registre comme indiqué dans le fichier d’installation de l’appareil (fichier INF). le tableau suivant répertorie les paramètres de l’appareil qui Windows les requêtes de Gestionnaire de périphériques multimédia.



| Nom du paramètre d’appareil | Type de données de Registre | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *WMDMSPCLSID*         | **SZ de REG \_**        | Valeur qui spécifie le CLSID du fournisseur de services contrôlant cet appareil. Ce paramètre est obligatoire pour la prise en charge PnP.<br/> La valeur du paramètre doit être le CLSID, et non le ProgID du fournisseur de services. ce paramètre est obligatoire pour prendre en charge Plug-and-Play (PnP) sous Windows Gestionnaire de périphériques de média. Pour plus d’informations, consultez [activation de PNP pour les appareils](enabling-pnp-for-devices.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| *OptimalTransferSize* | **\_valeur DWORD reg**     | valeur facultative qui spécifie la taille de transfert préférée que Windows Media Gestionnaire de périphériques utilise pendant les opérations de lecture et d’écriture. Si elle n’est pas fournie, une taille de transfert par défaut est utilisée.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| *UseMetadataViews*    | **\_valeur DWORD reg**     | paramètre facultatif qui spécifie si Windows Media Gestionnaire de périphériques organise le contenu par métadonnées tout en présentant le contenu de l’appareil aux applications. En l'absence de spécification, la valeur par défaut est 0.<br/> lorsque les applications énumèrent le contenu sur les stockages d’un lecteur audio portable, Windows media Gestionnaire de périphériques peut présenter le contenu organisé par métadonnées. Cela s’avère particulièrement utile pour les appareils avec une capacité de stockage importante.<br/> Les applications et les appareils ont la possibilité de contrôler ce comportement. Les appareils indiquent leur préférence par le biais du paramètre d’appareil *UseMetadataViews*.<br/> Les deux valeurs entières suivantes sont prises en charge :<br/> Demande que le contenu soit présenté aux applications exactement telles qu’elles sont organisées sur le système de fichiers de l’appareil.<br/> Demande que le contenu soit présenté aux applications organisées par métadonnées.<br/> |
| *ShowInShell*         | **\_valeur DWORD reg**     | paramètre facultatif qui spécifie si l’appareil doit apparaître dans l’explorateur de Windows. la valeur 1 indique que l’appareil doit apparaître dans l’explorateur de Windows. pour plus d’informations, consultez [configuration requise pour que les lecteurs Audio portables s’affichent dans l’explorateur de Windows](requirements-for-portable-audio-players-to-appear-in-windows-explorer.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| *UseExtendedWmdm*     | **\_valeur DWORD reg**     | paramètre facultatif qui signale Windows Gestionnaire de périphériques multimédia que le fournisseur de services prend en charge **IMDSPDevice3**, **IMDSPObject2** et **IMDSPStorage4**. sans cet indicateur, Windows Media Gestionnaire de périphériques n’appellera jamais ces interfaces. La valeur 1 indique que ces interfaces sont prises en charge.<br/> cet indicateur est requis pour les fournisseurs de services qui se synchronisent avec Lecteur Windows Media. (voir [activation de la synchronisation avec Lecteur Windows Media](enabling-synchronization-with-windows-media-player.md)).<br/>                                                                                                                                                                                                                                                                                                                                                                        |



 

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

 

 





