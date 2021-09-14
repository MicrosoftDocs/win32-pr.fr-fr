---
description: Utilise le protocole EAP-TLS (Extensible Authentication Protocol Transport Level Security) avec des certificats pour l’authentification sur le réseau (WPA2-Enterprise).
ms.assetid: ded07fda-ea7f-4c5a-9433-60196c3f14af
title: Exemple de profil WPA2-Enterprise avec TLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba561f552614896ca5da1522180a53146dc5ce54
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119354"
---
# <a name="wpa2-enterprise-with-tls-profile-sample"></a>Exemple de profil WPA2-Enterprise avec TLS

Cet exemple de profil utilise le protocole EAP-TLS (Extensible Authentication Protocol Transport Level Security) avec des certificats pour s’authentifier sur le réseau.

cet exemple est configuré pour utiliser Wi-Fi la sécurité Access 2 protégée s’exécutant en mode Enterprise (WPA2-Enterprise). Le type de sécurité WPA2-Enterprise utilise 802.1 X pour l’échange d’authentification avec le serveur principal. Le type de chiffrement Advanced Encryption Standard (AES) est utilisé pour le chiffrement.

Les informations d’identification EAP-TLS sont obtenues à partir du magasin de certificats. Si l’authentification basée sur les informations d’identification dans le magasin de certificats échoue, l’utilisateur est invité à fournir des informations d’identification valides. Aucun autre serveur, autorité de certification racine ou nom d’utilisateur n’est utilisé pour l’authentification en cas d’échec de la première tentative.

La configuration EAPHost utilisée dans cet exemple de profil sans fil a été dérivée de l’exemple de [Propriétés de connexion EAP-TLS](../eaphost/eap-tls-connection-properties.md) .

**Windows 7 et Windows Server 2008 R2 avec le Service de réseau local sans fil installé :** les modifications sont implémentées sur Windows 7 et Windows Server 2008 R2 avec le Service de réseau local sans fil installé pour optimiser les performances de mise en réseau sans fil. Le paramètre par défaut pour [**AutoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) lorsque cet élément n’est pas défini dans un profil de réseau local sans fil a changé. la valeur par défaut est remplacée par la valeur « false » sur Windows 7 et Windows Server 2008 R2 avec le Service de réseau local sans fil installé. le paramètre par défaut était « true » sur Windows Server 2008 et Windows Vista. Pour plus d’informations, reportez-vous à la description de l’élément de schéma [**AutoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) .

**Windows xp avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** EAP-TLS n’est pas pris en charge.

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleWPA2EnterpriseTLS</name>
    <SSIDConfig>
        <SSID>
            <name>SampleWPA2EnterpriseTLS</name>
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

 

 
