---
description: Utilisé pour se connecter à des réseaux qui ne diffusent pas leur nom de réseau ou SSID.
ms.assetid: 564324ad-6723-4676-ab5c-0b5d2957d201
title: Exemple de profil de non-diffusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a09bfd9cf9eac724f882a9aa3cf16064f051fdf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518235"
---
# <a name="non-broadcast-profile-sample"></a><span data-ttu-id="1041f-103">Exemple de profil de non-diffusion</span><span class="sxs-lookup"><span data-stu-id="1041f-103">Non-Broadcast Profile Sample</span></span>

<span data-ttu-id="1041f-104">L’exemple de profil de non diffusion peut être utilisé pour se connecter à des réseaux qui ne diffusent pas leur nom de réseau ou SSID.</span><span class="sxs-lookup"><span data-stu-id="1041f-104">The non-broadcast profile sample can be used to connect to networks which do not broadcast their network name or SSID.</span></span>

<span data-ttu-id="1041f-105">Cet exemple de profil est configuré pour utiliser Wi-Fi la sécurité d’accès protégé s’exécutant en mode personnel (WPA-Personal).</span><span class="sxs-lookup"><span data-stu-id="1041f-105">This sample profile is configured to use Wi-Fi Protected Access security running in Personal mode (WPA-Personal).</span></span> <span data-ttu-id="1041f-106">Le protocole TKIP (Temporal Key Integrity Protocol) est utilisé pour le chiffrement.</span><span class="sxs-lookup"><span data-stu-id="1041f-106">Temporal Key Integrity Protocol (TKIP) is used for encryption.</span></span> <span data-ttu-id="1041f-107">Les profils qui utilisent d’autres types de chiffrement et de sécurité peuvent également être configurés en tant que profils de non diffusion.</span><span class="sxs-lookup"><span data-stu-id="1041f-107">Profiles that use other security and cipher types can also be configured as non-broadcast profiles.</span></span>

<span data-ttu-id="1041f-108">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** L’enfant de [**nom**](wlan-profileschema-name-wlanprofile-element.md) de l’élément [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) est ignoré.</span><span class="sxs-lookup"><span data-stu-id="1041f-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** The [**name**](wlan-profileschema-name-wlanprofile-element.md) child of the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element is ignored.</span></span> <span data-ttu-id="1041f-109">Le nom du profil, tel qu’il est stocké dans le magasin de profils, est dérivé de l’enfant de [**nom**](wlan-profileschema-name-ssid-element.md) de l’élément [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="1041f-109">The name of the profile, as stored in the profile store, is derived from the [**name**](wlan-profileschema-name-ssid-element.md) child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

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

<span data-ttu-id="1041f-110">La clé partagée a été omise de cet exemple de profil.</span><span class="sxs-lookup"><span data-stu-id="1041f-110">The shared key has been omitted from this sample profile.</span></span> <span data-ttu-id="1041f-111">Si vous essayez d’utiliser cet exemple de profil pour vous connecter à un réseau, vous serez invité à entrer une clé partagée.</span><span class="sxs-lookup"><span data-stu-id="1041f-111">If you try to use this sample profile to connect to a network, you will be prompted to enter a shared key.</span></span> <span data-ttu-id="1041f-112">Vous pouvez éviter cette invite en ajoutant un élément enfant [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) à l’élément de [**sécurité**](wlan-profileschema-security-msm-element.md) qui suit immédiatement l’élément [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="1041f-112">You can avoid this prompt by adding a [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) child element to the [**security**](wlan-profileschema-security-msm-element.md) element immediately following the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span>

<span data-ttu-id="1041f-113">L’extrait de code suivant montre un élément [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) qui contient une clé non chiffrée.</span><span class="sxs-lookup"><span data-stu-id="1041f-113">The following snippet shows a [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) element that contains an unencrypted key.</span></span> <span data-ttu-id="1041f-114">Vous devez remplacer le commentaire `<!-- insert key here -->` par la clé non chiffrée réelle avant d’utiliser cet extrait de code dans un profil.</span><span class="sxs-lookup"><span data-stu-id="1041f-114">You must replace the comment `<!-- insert key here -->` with the actual unencrypted key before using this snippet in a profile.</span></span>

``` syntax
<sharedKey>
    <keyType>passPhrase</keyType>
    <protected>false</protected>
    <keyMaterial> <!-- insert key here --> </keyMaterial>
</sharedKey>
```

## <a name="related-topics"></a><span data-ttu-id="1041f-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1041f-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1041f-116">Exemples de profils sans fil</span><span class="sxs-lookup"><span data-stu-id="1041f-116">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 



