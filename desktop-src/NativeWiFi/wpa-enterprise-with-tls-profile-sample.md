---
description: Utilise le protocole EAP-TLS (Extensible Authentication Protocol Transport Level Security) avec des certificats pour l’authentification sur le réseau (WPA-Enterprise).
ms.assetid: fceeae22-3761-48ab-a190-1a7b1568ed64
title: Exemple de profil WPA-Enterprise avec TLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d6f236429c94e9602e173c2d6c3eb1e3bc8111f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119362"
---
# <a name="wpa-enterprise-with-tls-profile-sample"></a>Exemple de profil WPA-Enterprise avec TLS

Cet exemple de profil utilise le protocole EAP-TLS (Extensible Authentication Protocol Transport Level Security) avec des certificats pour s’authentifier sur le réseau.

cet exemple est configuré pour utiliser la sécurité d’accès Wi-Fi protégée s’exécutant en mode Enterprise (WPA-Enterprise). Le type de sécurité WPA-Enterprise utilise 802.1 X pour l’échange d’authentification avec le serveur principal. Le protocole TKIP (Temporal Key Integrity Protocol) est utilisé pour le chiffrement.

Les informations d’identification EAP-TLS sont obtenues à partir du magasin de certificats. Si l’authentification basée sur les informations d’identification dans le magasin de certificats échoue, l’utilisateur est invité à fournir des informations d’identification valides. Aucun autre serveur, autorité de certification racine ou nom d’utilisateur n’est utilisé pour l’authentification en cas d’échec de la première tentative.

La configuration EAPHost utilisée dans cet exemple de profil sans fil a été dérivée de l’exemple de [Propriétés de connexion EAP-TLS](../eaphost/eap-tls-connection-properties.md) .

**Windows 7 et Windows Server 2008 R2 avec le Service de réseau local sans fil installé :** les modifications sont implémentées sur Windows 7 et Windows Server 2008 R2 avec le Service de réseau local sans fil installé pour optimiser les performances de mise en réseau sans fil. Le paramètre par défaut pour [**AutoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) lorsque cet élément n’est pas défini dans un profil de réseau local sans fil a changé. la valeur par défaut est remplacée par la valeur « false » sur Windows 7 et Windows Server 2008 R2 avec le Service de réseau local sans fil installé. le paramètre par défaut était « true » sur Windows Server 2008 et Windows Vista. Pour plus d’informations, reportez-vous à la description de l’élément de schéma [**AutoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) .

**Windows xp avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** EAP-TLS n’est pas pris en charge.

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

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples de profils sans fil](wireless-profile-samples.md)
</dt> </dl>

 

 
