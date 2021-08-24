---
description: WIA fournit plusieurs interfaces pour énumérer diverses fonctionnalités, propriétés et informations.
ms.assetid: d46d4c18-79cc-4f3c-9745-522ab2635068
title: Utilisation d’énumérateurs WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47b6e822d38c73171767d43afd416d09648bd6b82095b9408e2f17827751b0cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813469"
---
# <a name="using-wia-enumerators"></a>Utilisation d’énumérateurs WIA

WIA fournit plusieurs interfaces pour énumérer diverses fonctionnalités, propriétés et informations. les interfaces d’énumération WIA (Windows Image Acquisition) sont toutes des implémentations spécifiques de l’interface d’énumération COM (component Object Model) standard. Pour plus d’informations, consultez [IEnumXXXX](/previous-versions//ms680089(v=vs.85)).

Le tableau suivant fournit des informations sur les interfaces d’énumération WIA. 

| Interface                                                   | Obtention d’un pointeur                                                                                                                                                                                    | Utilisation                                                                                                                             |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumWIA \_ dev \_ majuscules**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)       | Appelez une méthode [**IWiaItem :: EnumDeviceCapabilities**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumdevicecapabilities) ou [**IWiaItem2 :: EnumDeviceCapabilities**](-wia-iwiaitem2-enumdevicecapabilities.md) du d’un élément racine WIA. | Énumère les fonctionnalités d’un périphérique matériel WIA, telles que les commandes d’appareil et les événements.                                            |
| [**\_Informations de développement IEnumWIA \_**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)       | Appelez la méthode [**IWiaDevMgr :: EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) ou [**IWiaDevMgr2 :: EnumDeviceInfo**](-wia-iwiadevmgr2-enumdeviceinfo.md) .                                            | Énumère les appareils WIA disponibles et fournit des pointeurs vers leurs interfaces [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) . |
| [**\_Informations de format IEnumWIA \_**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info) | Appeler une méthode d' [**informations de \_ format \_ IWiaDataTransfer :: idtEnumWIA**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtenumwia_format_info) d’un élément.                                                                              | Énumère toutes les informations de format d’image fournies par un élément WIA.                                                                    |
| [**IEnumWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem)                   | Appelez une méthode [**IWiaItem :: EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) ou [**IWiaItem2 :: EnumChildItems**](-wia-iwiaitem2-enumchilditems.md) de l’élément WIA.                                          | Énumère les éléments enfants d’un élément WIA qui représente soit un appareil, soit un dossier.                                                |



 

 

 
