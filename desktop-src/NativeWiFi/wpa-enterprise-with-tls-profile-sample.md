---
description: Utilise EAP-TLS (Extensible Authentication Protocol Transport Level Security) avec des certificats pour l’authentification sur le réseau (WPA-Enterprise).
ms.assetid: fceeae22-3761-48ab-a190-1a7b1568ed64
title: Exemple de profil WPA-Enterprise avec TLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d6f236429c94e9602e173c2d6c3eb1e3bc8111f
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395034"
---
# <a name="wpa-enterprise-with-tls-profile-sample"></a><span data-ttu-id="6740d-103">Exemple de profil WPA-Enterprise avec TLS</span><span class="sxs-lookup"><span data-stu-id="6740d-103">WPA-Enterprise with TLS Profile Sample</span></span>

<span data-ttu-id="6740d-104">Cet exemple de profil utilise le protocole EAP-TLS (Extensible Authentication Protocol Transport Level Security) avec des certificats pour s’authentifier sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="6740d-104">This sample profile uses Extensible Authentication Protocol Transport Level Security (EAP-TLS) with certificates to authenticate to the network.</span></span>

<span data-ttu-id="6740d-105">Cet exemple est configuré pour utiliser la sécurité d’accès Wi-Fi protégée s’exécutant en mode entreprise (WPA-Enterprise).</span><span class="sxs-lookup"><span data-stu-id="6740d-105">This sample is configured to use Wi-Fi Protected Access security running in Enterprise mode (WPA-Enterprise).</span></span> <span data-ttu-id="6740d-106">Le type de sécurité WPA-Enterprise utilise 802.1 X pour l’échange d’authentification avec le serveur principal.</span><span class="sxs-lookup"><span data-stu-id="6740d-106">The WPA-Enterprise security type uses 802.1X for the authentication exchange with the backend.</span></span> <span data-ttu-id="6740d-107">Le protocole TKIP (Temporal Key Integrity Protocol) est utilisé pour le chiffrement.</span><span class="sxs-lookup"><span data-stu-id="6740d-107">Temporal Key Integrity Protocol (TKIP) is used for encryption.</span></span>

<span data-ttu-id="6740d-108">Les informations d’identification EAP-TLS sont obtenues à partir du magasin de certificats.</span><span class="sxs-lookup"><span data-stu-id="6740d-108">The EAP-TLS credentials are obtained from the certificate store.</span></span> <span data-ttu-id="6740d-109">Si l’authentification basée sur les informations d’identification dans le magasin de certificats échoue, l’utilisateur est invité à fournir des informations d’identification valides.</span><span class="sxs-lookup"><span data-stu-id="6740d-109">If authentication based on the credentials in the certificate store fails, the user is prompted to provide valid credentials.</span></span> <span data-ttu-id="6740d-110">Aucun autre serveur, autorité de certification racine ou nom d’utilisateur n’est utilisé pour l’authentification en cas d’échec de la première tentative.</span><span class="sxs-lookup"><span data-stu-id="6740d-110">No alternate servers, root certificate authorities, or user names are used for authentication if the first attempt fails.</span></span>

<span data-ttu-id="6740d-111">La configuration EAPHost utilisée dans cet exemple de profil sans fil a été dérivée de l’exemple de [Propriétés de connexion EAP-TLS](../eaphost/eap-tls-connection-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="6740d-111">The EAPHost configuration used in this wireless profile sample was derived from the [EAP-TLS Connection Properties](../eaphost/eap-tls-connection-properties.md) sample.</span></span>

<span data-ttu-id="6740d-112">**Windows 7 et Windows Server 2008 R2 avec le service de réseau local sans fil installé :** Les modifications sont implémentées sur Windows 7 et Windows Server 2008 R2 avec le service de réseau local sans fil installé pour optimiser les performances de mise en réseau sans fil.</span><span class="sxs-lookup"><span data-stu-id="6740d-112">**Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed:** Changes are implemented on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed to optimize wireless networking performance.</span></span> <span data-ttu-id="6740d-113">Le paramètre par défaut pour [**AutoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) lorsque cet élément n’est pas défini dans un profil de réseau local sans fil a changé.</span><span class="sxs-lookup"><span data-stu-id="6740d-113">The default setting for [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) when this element is not set in a wireless LAN profile has changed.</span></span> <span data-ttu-id="6740d-114">La valeur par défaut est remplacée par la valeur « false » sur Windows 7 et Windows Server 2008 R2 avec le service de réseau local sans fil installé.</span><span class="sxs-lookup"><span data-stu-id="6740d-114">The default setting is changed to "false" on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span> <span data-ttu-id="6740d-115">Le paramètre par défaut était « true » sur Windows Server 2008 et Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6740d-115">The default setting was "true" on Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="6740d-116">Pour plus d’informations, reportez-vous à la description de l’élément de schéma [**AutoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="6740d-116">Please refer to the [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) schema element description for more information.</span></span>

<span data-ttu-id="6740d-117">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** EAP-TLS n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="6740d-117">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** EAP-TLS is not supported.</span></span>

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleWPAEnterpriseTLS</name>
    <SSIDConfig>
        <SSID>
            <name>SampleWPAEnterpriseTLS</name>
        </SSID>
        <nonBroadcast>false</nonBroadcast>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
    <autoSwitch>false</autoSwitch>
    <MSM>
        <security>
            <authEncryption>
                <authentication>WPA</authentication>
                <encryption>TKIP</encryption>
                <useOneX>true</useOneX>
            </authEncryption>
            <OneX xmlns="https://www.microsoft.com/networking/OneX/v1">
                <EAPConfig>
                    <EapHostConfig xmlns="https://www.microsoft.com/provisioning/EapHostConfig" 
                                   xmlns:eapCommon="https://www.microsoft.com/provisioning/EapCommon" 
                                   xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapMethodConfig">
 
                        <EapMethod>
                            <eapCommon:Type>13</eapCommon:Type> 
                            <eapCommon:AuthorId>0</eapCommon:AuthorId> 
                        </EapMethod>
                        <Config xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapConnectionPropertiesV1" 
                                xmlns:eapTls="https://www.microsoft.com/provisioning/EapTlsConnectionPropertiesV1">

                            <baseEap:Eap>
                                <baseEap:Type>13</baseEap:Type> 
                                <eapTls:EapType>
                                    <eapTls:CredentialsSource>
                                        <eapTls:CertificateStore />
                                    </eapTls:CredentialsSource>
                                    <eapTls:ServerValidation>
                                        <eapTls:DisableUserPromptForServerValidation>false</eapTls:DisableUserPromptForServerValidation> 
                                        <eapTls:ServerNames /> 
                                    </eapTls:ServerValidation> 
                                   <eapTls:DifferentUsername>false</eapTls:DifferentUsername> 
                               </eapTls:EapType>
                           </baseEap:Eap>
                       </Config>
                   </EapHostConfig>
                </EAPConfig>
            </OneX>
        </security>
    </MSM>
</WLANProfile>
```

## <a name="related-topics"></a><span data-ttu-id="6740d-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6740d-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6740d-119">Exemples de profils sans fil</span><span class="sxs-lookup"><span data-stu-id="6740d-119">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 
