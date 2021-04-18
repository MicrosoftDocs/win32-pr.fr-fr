---
description: L’interface IWiaVideo permet à une application d’afficher la vidéo et de capturer des images fixes à partir de celle-ci.
ms.assetid: 59eddbdc-4957-44be-a602-0763f3385e89
title: Aperçu de la vidéo (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 935625c1c16ceea66326963185dd75d96d98ed02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526428"
---
# <a name="previewing-video-wia"></a>Aperçu de la vidéo (WIA)

L’interface [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) permet à une application d’afficher la vidéo et de capturer des images fixes à partir de celle-ci. Procédez comme suit pour sélectionner le périphérique vidéo en continu et afficher un flux vidéo dans une fenêtre.

-   Appelez [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour récupérer un pointeur vers l’interface [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) .
-   Utilisez la méthode [**IWiaDevMgr :: EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) de l’interface [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) pour obtenir un pointeur vers l’interface d' [**\_ \_ informations de développement IEnumWIA**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) . Pour obtenir des instructions sur l’énumération des appareils, consultez énumération des périphériques système.
-   Utilisez l’interface [**IEnumWIA \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) pour obtenir un pointeur d’interface [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) pour chaque périphérique WIA (Windows Image Acquisition) trouvé.
-   Utilisez l’interface [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) pour récupérer la propriété DeviceID du périphérique souhaité. Un périphérique vidéo en streaming a l’indicateur StiDeviceTypeStreamingVideo du \_ jeu de \_ Propriétés de type de développement DIP WIA \_ .
-   Utilisez l’interface [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) pour récupérer la valeur de la propriété du répertoire des images de la \_ DPV WIA \_ \_ .
-   Appelez [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour récupérer un pointeur vers l’interface [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) .
-   Affectez à la propriété [**IWiaVideo :: ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) de l’interface [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) la valeur reçue à partir de la valeur de la propriété du répertoire d’images de la \_ DPV WIA \_ \_ .
-   Appelez [**IWiaVideo :: CreateVideoByWiaDevID**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-createvideobywiadevid) sur l’interface [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) , en passant l’ID d’appareil de l’appareil d’images en continu et le handle de la fenêtre dans laquelle la vidéo doit être affichée.

> [!Note]  
> WIA ne prend pas en charge les périphériques vidéo dans Windows Server 2003, Windows Vista ou version ultérieure. Pour ces versions de Windows, utilisez [DirectShow](/previous-versions//ms783323(v=vs.85)) pour acquérir des images à partir d’une vidéo.

 

 

 
