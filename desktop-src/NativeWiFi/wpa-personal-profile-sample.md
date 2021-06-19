---
description: Utilise une clé prépartagée pour l’authentification réseau. Cet exemple de profil utilise la sécurité d’accès Wi-Fi protégée s’exécutant en mode personnel (WPA-Personal).
ms.assetid: f04de28b-a98d-40cd-91c8-e446cf669555
title: Exemple de profil de WPA-Personal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 334076d4b0cf10372ed845265a1fff652f0879b9
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395024"
---
# <a name="wpa-personal-profile-sample"></a><span data-ttu-id="582d2-104">Exemple de profil de WPA-Personal</span><span class="sxs-lookup"><span data-stu-id="582d2-104">WPA-Personal Profile Sample</span></span>

<span data-ttu-id="582d2-105">Cet exemple de profil utilise une clé prépartagée pour l’authentification réseau.</span><span class="sxs-lookup"><span data-stu-id="582d2-105">This sample profile uses a pre-shared key for network authentication.</span></span> <span data-ttu-id="582d2-106">La clé est partagée avec le client et le point d’accès.</span><span class="sxs-lookup"><span data-stu-id="582d2-106">The key is shared with the client and the access point.</span></span> <span data-ttu-id="582d2-107">Cet exemple de profil est configuré pour utiliser Wi-Fi la sécurité d’accès protégé s’exécutant en mode personnel (WPA-Personal).</span><span class="sxs-lookup"><span data-stu-id="582d2-107">This sample profile is configured to use Wi-Fi Protected Access security running in Personal mode (WPA-Personal).</span></span> <span data-ttu-id="582d2-108">Le protocole TKIP (Temporal Key Integrity Protocol) est utilisé pour le chiffrement.</span><span class="sxs-lookup"><span data-stu-id="582d2-108">Temporal Key Integrity Protocol (TKIP) is used for encryption.</span></span>

<span data-ttu-id="582d2-109">**Windows 7 et Windows Server 2008 R2 avec le service de réseau local sans fil installé :** Les modifications sont implémentées sur Windows 7 et Windows Server 2008 R2 avec le service de réseau local sans fil installé pour optimiser les performances de mise en réseau sans fil.</span><span class="sxs-lookup"><span data-stu-id="582d2-109">**Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed:** Changes are implemented on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed to optimize wireless networking performance.</span></span> <span data-ttu-id="582d2-110">Le paramètre par défaut pour [**AutoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) lorsque cet élément n’est pas défini dans un profil de réseau local sans fil a changé.</span><span class="sxs-lookup"><span data-stu-id="582d2-110">The default setting for [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) when this element is not set in a wireless LAN profile has changed.</span></span> <span data-ttu-id="582d2-111">La valeur par défaut est remplacée par la valeur « false » sur Windows 7 et Windows Server 2008 R2 avec le service de réseau local sans fil installé.</span><span class="sxs-lookup"><span data-stu-id="582d2-111">The default setting is changed to "false" on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span> <span data-ttu-id="582d2-112">Le paramètre par défaut était « true » sur Windows Server 2008 et Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="582d2-112">The default setting was "true" on Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="582d2-113">Pour plus d’informations, reportez-vous à la description de l’élément de schéma [**AutoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="582d2-113">Please refer to the [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) schema element description for more information.</span></span>

<span data-ttu-id="582d2-114">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** L’enfant de [**nom**](wlan-profileschema-name-wlanprofile-element.md) de l’élément [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) est ignoré.</span><span class="sxs-lookup"><span data-stu-id="582d2-114">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** The [**name**](wlan-profileschema-name-wlanprofile-element.md) child of the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element is ignored.</span></span> <span data-ttu-id="582d2-115">Le nom du profil, tel qu’il est stocké dans le magasin de profils, est dérivé de l’enfant de [**nom**](wlan-profileschema-name-ssid-element.md) de l’élément [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="582d2-115">The name of the profile, as stored in the profile store, is derived from the [**name**](wlan-profileschema-name-ssid-element.md) child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

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

<span data-ttu-id="582d2-116">La clé partagée a été omise de cet exemple de profil.</span><span class="sxs-lookup"><span data-stu-id="582d2-116">The shared key has been omitted from this sample profile.</span></span> <span data-ttu-id="582d2-117">Si vous essayez d’utiliser cet exemple de profil pour vous connecter à un réseau, vous serez invité à entrer une clé partagée.</span><span class="sxs-lookup"><span data-stu-id="582d2-117">If you try to use this sample profile to connect to a network, you will be prompted to enter a shared key.</span></span> <span data-ttu-id="582d2-118">Vous pouvez éviter cette invite en ajoutant un élément enfant [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) à l’élément de [**sécurité**](wlan-profileschema-security-msm-element.md) qui suit immédiatement l’élément [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="582d2-118">You can avoid this prompt by adding a [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) child element to the [**security**](wlan-profileschema-security-msm-element.md) element immediately following the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span>

<span data-ttu-id="582d2-119">L’extrait de code suivant montre un élément [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) qui contient une clé non chiffrée.</span><span class="sxs-lookup"><span data-stu-id="582d2-119">The following snippet shows a [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) element that contains an unencrypted key.</span></span> <span data-ttu-id="582d2-120">Vous devez remplacer le commentaire `<!-- insert key here -->` par la clé non chiffrée réelle avant d’utiliser cet extrait de code dans un profil.</span><span class="sxs-lookup"><span data-stu-id="582d2-120">You must replace the comment `<!-- insert key here -->` with the actual unencrypted key before using this snippet in a profile.</span></span>

``` syntax
<sharedKey>
    <keyType>passPhrase</keyType>
    <protected>false</protected>
    <keyMaterial> <!-- insert key here --> </keyMaterial>
</sharedKey>
```

## <a name="related-topics"></a><span data-ttu-id="582d2-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="582d2-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="582d2-122">Exemples de profils sans fil</span><span class="sxs-lookup"><span data-stu-id="582d2-122">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 



