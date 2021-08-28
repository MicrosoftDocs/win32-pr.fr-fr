---
description: quand une application se connecte à un périphérique matériel wia (Windows Image Acquisition), WIA crée une arborescence d’éléments (une arborescence hiérarchique d’interfaces IWiaItem ou IWiaItem2) qui représente l’appareil et ses images, dossiers et lits d’analyse.
ms.assetid: 2a7bcfd4-4075-48a4-9eff-5210b9a635e3
title: Sélection d’un appareil (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d068dc2501419b5748f199114fab15d72dc5fecc6c7e6881f63b8e47114b7d2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813658"
---
# <a name="selecting-a-device-wia"></a>Sélection d’un appareil (WIA)

quand une application se connecte à un périphérique matériel wia (Windows Image Acquisition), WIA crée une arborescence d’éléments (une arborescence hiérarchique d’interfaces [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ou [**IWiaItem2**](-wia-iwiaitem2.md) ) qui représente l’appareil et ses images, dossiers et lits d’analyse. Une application peut sélectionner et se connecter à un appareil sans entrée d’utilisateur, ou elle peut afficher une boîte de dialogue qui permet à un utilisateur de sélectionner un appareil.

-   [Sélection d’un appareil sans interface utilisateur](#selecting-a-device-without-the-ui)
-   [Sélection d’un appareil avec l’interface utilisateur](#selecting-a-device-with-the-ui)

## <a name="selecting-a-device-without-the-ui"></a>Sélection d’un appareil sans interface utilisateur

Procédez comme suit pour sélectionner un périphérique matériel WIA et s’y connecter.

-   Appelez [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour récupérer un pointeur vers l’interface [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) ou [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) .
-   Utilisez la méthode [**IWiaDevMgr :: EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) de l’interface [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) ou [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) pour obtenir un pointeur vers l’interface [**IEnumWIA \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) . Pour obtenir des instructions sur l’énumération des appareils, consultez [énumération des périphériques système](-wia-enumerating-system-devices.md).
-   Utilisez l’interface [**IEnumWIA \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) pour obtenir les pointeurs d’interface [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) pour chaque appareil WIA énuméré.
-   Utilisez l’interface [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) pour inspecter les propriétés d’informations sur l’appareil de chaque appareil et enregistrer la propriété de l' \_ ID de développement DIP WIA \_ \_ à partir de l’appareil souhaité.
-   Utilisez la propriété DeviceID avec la méthode [**IWiaDevMgr :: CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) dans l’interface [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) ou [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) pour créer un objet appareil WIA. La méthode **IWiaDevMgr :: CreateDevice** fournit l’application avec le pointeur vers l’interface [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ou [**IWiaItem2**](-wia-iwiaitem2.md) de l’élément racine de l’appareil spécifié.

Pour obtenir un exemple de la procédure à suivre dans une application, consultez la section [création d’un appareil](-wia-creating-a-device.md) dans le didacticiel de ce guide.

## <a name="selecting-a-device-with-the-ui"></a>Sélection d’un appareil avec l’interface utilisateur

Après avoir récupéré un pointeur vers [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr), une application peut permettre à un utilisateur de sélectionner un appareil en ignorant le reste des étapes ci-dessus et en appelant [**IWiaDevMgr :: SelectDeviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-selectdevicedlg). **IWiaDevMgr :: SelectDeviceDlg** affiche une boîte de dialogue dans laquelle l’utilisateur peut sélectionner un appareil WIA.

Il est recommandé que les applications rendent la sélection de l’appareil et de l’image disponible via un élément de menu nommé **à partir de scanner** dans le menu **fichier** .

 

 
