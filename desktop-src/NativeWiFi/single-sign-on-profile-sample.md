---
description: Utilisé pour les scénarios qui requièrent l’authentification 802.1 X avant l’ouverture de session Windows.
ms.assetid: 76c8d416-3912-41b1-ac9d-3e6e86a76ceb
title: Exemple de profil de Sign-On unique
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 077ed95095150e81ad9a3d7412d1940dcb1b33e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535670"
---
# <a name="single-sign-on-profile-sample"></a><span data-ttu-id="37255-103">Exemple de profil de Sign-On unique</span><span class="sxs-lookup"><span data-stu-id="37255-103">Single Sign-On Profile Sample</span></span>

<span data-ttu-id="37255-104">L’exemple de profil de l’authentification unique (SSO) peut être utilisé pour les scénarios qui requièrent l’authentification 802.1 X avant l’ouverture de session Windows.</span><span class="sxs-lookup"><span data-stu-id="37255-104">The single sign-on (SSO) profile sample can be used for scenarios that require 802.1X authentication before Windows logon.</span></span>

<span data-ttu-id="37255-105">Cet exemple est configuré pour utiliser Wi-Fi la sécurité Access 2 protégée s’exécutant en mode entreprise (WPA2-Entreprise).</span><span class="sxs-lookup"><span data-stu-id="37255-105">This sample is configured to use Wi-Fi Protected Access 2 security running in Enterprise mode (WPA2-Enterprise).</span></span> <span data-ttu-id="37255-106">Le protocole PEAP-MSCHAPv2 (Protected Extensible Authentication Protocol avec PEAP-MSCHAPv2) est utilisé pour l’authentification réseau.</span><span class="sxs-lookup"><span data-stu-id="37255-106">Protected Extensible Authentication Protocol with Microsoft Challenge Handshake Authentication Protocol version 2 (PEAP-MSCHAPv2) is used for network authentication.</span></span> <span data-ttu-id="37255-107">Les informations d’identification d’ouverture de session Windows sont utilisées pour l’authentification PEAP-MSCHAPv2.</span><span class="sxs-lookup"><span data-stu-id="37255-107">The Windows logon credentials are used for PEAP-MSCHAPv2 authentication.</span></span>

<span data-ttu-id="37255-108">Bien que cet exemple soit configuré pour utiliser WPA2-Enterprise et PEAP-MSCHAPv2, les profils SSO peuvent être configurés avec d’autres types de sécurité et d’authentification.</span><span class="sxs-lookup"><span data-stu-id="37255-108">While this sample is configured to use WPA2-Enterprise and PEAP-MSCHAPv2, SSO profiles can be configured with other security and authentication types.</span></span>

<span data-ttu-id="37255-109">**Windows 7 et Windows Server 2008 R2 avec le service de réseau local sans fil installé :** Les modifications sont implémentées sur Windows 7 et Windows Server 2008 R2 avec le service de réseau local sans fil installé pour optimiser les performances de mise en réseau sans fil.</span><span class="sxs-lookup"><span data-stu-id="37255-109">**Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed:** Changes are implemented on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed to optimize wireless networking performance.</span></span> <span data-ttu-id="37255-110">Le paramètre par défaut pour [**AutoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) lorsque cet élément n’est pas défini dans un profil de réseau local sans fil a changé.</span><span class="sxs-lookup"><span data-stu-id="37255-110">The default setting for [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) when this element is not set in a wireless LAN profile has changed.</span></span> <span data-ttu-id="37255-111">La valeur par défaut est remplacée par la valeur « false » sur Windows 7 et Windows Server 2008 R2 avec le service de réseau local sans fil installé.</span><span class="sxs-lookup"><span data-stu-id="37255-111">The default setting is changed to "false" on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span> <span data-ttu-id="37255-112">Le paramètre par défaut était « true » sur Windows Server 2008 et Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="37255-112">The default setting was "true" on Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="37255-113">Pour plus d’informations, reportez-vous à la description de l’élément de schéma [**AutoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="37255-113">Please refer to the [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) schema element description for more information.</span></span>

<span data-ttu-id="37255-114">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** L’enfant de [**nom**](wlan-profileschema-name-wlanprofile-element.md) de l’élément [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) est ignoré.</span><span class="sxs-lookup"><span data-stu-id="37255-114">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** The [**name**](wlan-profileschema-name-wlanprofile-element.md) child of the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element is ignored.</span></span> <span data-ttu-id="37255-115">Le nom du profil, tel qu’il est stocké dans le magasin de profils, est dérivé de l’enfant de [**nom**](wlan-profileschema-name-ssid-element.md) de l’élément [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="37255-115">The name of the profile, as stored in the profile store, is derived from the [**name**](wlan-profileschema-name-ssid-element.md) child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span> <span data-ttu-id="37255-116">Les enfants [**cacheUserData**](onexschema-cacheuserdata-onex-element.md), [**maxAuthFailures**](onexschema-maxauthfailures-onex-element.md), [**authmode**](onexschema-authmode-onex-element.md)et [**singleSignOn**](onexschema-singlesignon-onex-element.md) de l’élément [**Onex**](onexschema-onex-element.md) ne sont pas pris en charge et doivent être supprimés du profil avant l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="37255-116">The [**cacheUserData**](onexschema-cacheuserdata-onex-element.md), [**maxAuthFailures**](onexschema-maxauthfailures-onex-element.md), [**authMode**](onexschema-authmode-onex-element.md), and [**singleSignOn**](onexschema-singlesignon-onex-element.md) children of the [**OneX**](onexschema-onex-element.md) element are not supported, and should be removed from the profile before use.</span></span>

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleSingleSignOn</name>
    <SSIDConfig>
        <SSID>
            <name>SampleSingleSignOn</name>
        </SSID>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
    <autoSwitch>false</autoSwitch>
    <MSM>
        <security>
            <authEncryption>
                <authentication>WPA2</authentication>
                <encryption>AES</encryption>
                <useOneX>true</useOneX>
            </authEncryption>
            <OneX xmlns="https://www.microsoft.com/networking/OneX/v1">
                <cacheUserData>true</cacheUserData>
                <maxAuthFailures>3</maxAuthFailures>
                <authMode>user</authMode>
                <singleSignOn>
                    <type>preLogon</type>
                    <maxDelay>10</maxDelay>
                </singleSignOn>
                <EAPConfig>
                    <EapHostConfig xmlns="https://www.microsoft.com/provisioning/EapHostConfig" 
                                   xmlns:eapCommon="https://www.microsoft.com/provisioning/EapCommon" 
                                   xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapMethodConfig">
                        <EapMethod>
                            <eapCommon:Type>25</eapCommon:Type> 
                            <eapCommon:AuthorId>0</eapCommon:AuthorId> 
                       </EapMethod>
                       <Config xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapConnectionPropertiesV1" 
                               xmlns:msPeap="https://www.microsoft.com/provisioning/MsPeapConnectionPropertiesV1" 
                               xmlns:msChapV2="https://www.microsoft.com/provisioning/MsChapV2ConnectionPropertiesV1">
                           <baseEap:Eap>
                               <baseEap:Type>25</baseEap:Type> 
                               <msPeap:EapType>
                                   <msPeap:ServerValidation>
                                       <msPeap:DisableUserPromptForServerValidation>false</msPeap:DisableUserPromptForServerValidation> 
                                       <msPeap:TrustedRootCA /> 
                                   </msPeap:ServerValidation>
                                   <msPeap:FastReconnect>true</msPeap:FastReconnect> 
                                   <msPeap:InnerEapOptional>0</msPeap:InnerEapOptional> 
                                   <baseEap:Eap>
                                       <baseEap:Type>26</baseEap:Type> 
                                       <msChapV2:EapType>
                                           <msChapV2:UseWinLogonCredentials>true</msChapV2:UseWinLogonCredentials> 
                                       </msChapV2:EapType>
                                   </baseEap:Eap>
                                   <msPeap:EnableQuarantineChecks>false</msPeap:EnableQuarantineChecks> 
                                   <msPeap:RequireCryptoBinding>false</msPeap:RequireCryptoBinding> 
                                   <msPeap:PeapExtensions /> 
                               </msPeap:EapType>
                           </baseEap:Eap>
                       </Config>
                   </EapHostConfig>
                </EAPConfig>
            </OneX>
        </security>
    </MSM>
</WLANProfile>
```

## <a name="related-topics"></a><span data-ttu-id="37255-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="37255-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37255-118">Exemples de profils sans fil</span><span class="sxs-lookup"><span data-stu-id="37255-118">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 



