---
description: Modèle d’appareil
ms.assetid: d56021be-616b-41cd-8cf0-9e0d314f62cd
title: Modèle d’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4657fbb49e2619d75911c18185109805116b9647
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482704"
---
# <a name="device-mode"></a>Modèle d’appareil

Les caméscopes IEEE 1394 et USB peuvent basculer entre le mode caméra et le mode magnétoscope (magnétoscope). Quand un caméscope IEEE 1394 change de mode, le périphérique est redéfini et l’application doit l’énumérer à nouveau. Il n’existe aucun moyen pour une application de basculer le mode par programme. Les caméscopes USB, quant à eux, peuvent basculer entre les modes caméra et magnétoscope sans réinitialiser, et l’application peut modifier le mode.

**Pilote MSDV**

Pour récupérer le mode actuel sur un appareil IEEE 1394, appelez la méthode [**IAMExtDevice :: GetCapability**](/windows/desktop/api/Strmif/nf-strmif-iamextdevice-getcapability) avec la valeur Ed \_ DEVCAP \_ Device \_ type. Si la méthode retourne le \_ magnétoscope devtype de valeur Ed \_ , l’appareil est en mode VTR et possède des fonctions telles que pause, arrêt, avance rapide et rembobiner. Sinon, si la méthode retourne ED \_ devtype \_ Camera, l’appareil est en mode caméra. L’exemple de code suivant montre comment interroger le type d’appareil :


```C++
if (MyDevCap.bHasDevice) 
{
    LONG lDeviceType = 0;
    MyDevCap.pDevice->GetCapability(ED_DEVCAP_DEVICE_TYPE, &lDeviceType, 0);

    if (lDeviceType == ED_DEVTYPE_VCR) 
    {
        // Device is a VTR. Enable all VTR functions.
    }
    else 
    {
        // Device is a camera. 
        // Enable record and record-pause; disable other functions.
    }
}
```



Si le caméscope passe en mode hors connexion, vous devez le demander une nouvelle fois dès qu’il sera disponible. Le gestionnaire de graphique de filtre publie un événement de [**\_ \_ perte d’appareil ce**](ec-device-lost.md) lorsque l’appareil est supprimé.

**Pilote UVC**

Étant donné que les périphériques vidéo USB peuvent changer de mode sans réinitialiser, le code présenté dans les exemples précédents n’est pas fiable pour les périphériques USB. Utilisez plutôt l’interface [**ISelector**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector) pour accéder au mode actuel. Vous pouvez également utiliser cette interface pour changer de mode par programme si l’appareil la prend en charge.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Contrôle d’un caméscope DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



