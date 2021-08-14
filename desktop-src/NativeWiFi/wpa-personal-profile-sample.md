---
description: Utilise une clé prépartagée pour l’authentification réseau. Cet exemple de profil utilise la sécurité d’accès Wi-Fi protégée s’exécutant en mode personnel (WPA-Personal).
ms.assetid: f04de28b-a98d-40cd-91c8-e446cf669555
title: Exemple de profil de WPA-Personal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d196a327672ae31cb52d275be79193860fd89fff29f169be63018f5b848a4268
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117797419"
---
# <a name="wpa-personal-profile-sample"></a>Exemple de profil de WPA-Personal

Cet exemple de profil utilise une clé prépartagée pour l’authentification réseau. La clé est partagée avec le client et le point d’accès. Cet exemple de profil est configuré pour utiliser Wi-Fi la sécurité d’accès protégé s’exécutant en mode personnel (WPA-Personal). Le protocole TKIP (Temporal Key Integrity Protocol) est utilisé pour le chiffrement.

**Windows 7 et Windows Server 2008 R2 avec le Service de réseau local sans fil installé :** les modifications sont implémentées sur Windows 7 et Windows Server 2008 R2 avec le Service de réseau local sans fil installé pour optimiser les performances de mise en réseau sans fil. Le paramètre par défaut pour [**AutoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) lorsque cet élément n’est pas défini dans un profil de réseau local sans fil a changé. la valeur par défaut est remplacée par la valeur « false » sur Windows 7 et Windows Server 2008 R2 avec le Service de réseau local sans fil installé. le paramètre par défaut était « true » sur Windows Server 2008 et Windows Vista. Pour plus d’informations, reportez-vous à la description de l’élément de schéma [**AutoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) .

**Windows xp avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** L’enfant de [**nom**](wlan-profileschema-name-wlanprofile-element.md) de l’élément [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) est ignoré. Le nom du profil, tel qu’il est stocké dans le magasin de profils, est dérivé de l’enfant de [**nom**](wlan-profileschema-name-ssid-element.md) de l’élément [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleWPAPSK</name>
    <SSIDConfig>
        <SSID>
            <name>SampleWPAPSK</name>
        </SSID>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
    <autoSwitch>false</autoSwitch>
    <MSM>
        <security>
            <authEncryption>
                <authentication>WPAPSK</authentication>
                <encryption>TKIP</encryption>
                <useOneX>false</useOneX>
            </authEncryption>
        </security>
    </MSM>
</WLANProfile>
```

La clé partagée a été omise de cet exemple de profil. Si vous essayez d’utiliser cet exemple de profil pour vous connecter à un réseau, vous serez invité à entrer une clé partagée. Vous pouvez éviter cette invite en ajoutant un élément enfant [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) à l’élément de [**sécurité**](wlan-profileschema-security-msm-element.md) qui suit immédiatement l’élément [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .

L’extrait de code suivant montre un élément [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) qui contient une clé non chiffrée. Vous devez remplacer le commentaire `<!-- insert key here -->` par la clé non chiffrée réelle avant d’utiliser cet extrait de code dans un profil.

``` syntax
<sharedKey>
    <keyType>passPhrase</keyType>
    <protected>false</protected>
    <keyMaterial> <!-- insert key here --> </keyMaterial>
</sharedKey>
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples de profils sans fil](wireless-profile-samples.md)
</dt> </dl>

 

 



