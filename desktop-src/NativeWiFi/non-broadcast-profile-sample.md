---
description: Utilisé pour se connecter à des réseaux qui ne diffusent pas leur nom de réseau ou SSID.
ms.assetid: 564324ad-6723-4676-ab5c-0b5d2957d201
title: Exemple de profil de non-diffusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a09bfd9cf9eac724f882a9aa3cf16064f051fdf3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009455"
---
# <a name="non-broadcast-profile-sample"></a>Exemple de profil de non-diffusion

L’exemple de profil de non diffusion peut être utilisé pour se connecter à des réseaux qui ne diffusent pas leur nom de réseau ou SSID.

Cet exemple de profil est configuré pour utiliser Wi-Fi la sécurité d’accès protégé s’exécutant en mode personnel (WPA-Personal). Le protocole TKIP (Temporal Key Integrity Protocol) est utilisé pour le chiffrement. Les profils qui utilisent d’autres types de chiffrement et de sécurité peuvent également être configurés en tant que profils de non diffusion.

**Windows xp avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** L’enfant de [**nom**](wlan-profileschema-name-wlanprofile-element.md) de l’élément [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) est ignoré. Le nom du profil, tel qu’il est stocké dans le magasin de profils, est dérivé de l’enfant de [**nom**](wlan-profileschema-name-ssid-element.md) de l’élément [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleNonBroadcast</name>
    <SSIDConfig>
        <SSID>
            <name>SampleNonBroadcast</name>
        </SSID>
        <nonBroadcast>true</nonBroadcast>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
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

 

 



