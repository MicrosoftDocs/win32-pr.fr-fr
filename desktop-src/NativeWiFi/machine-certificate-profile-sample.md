---
description: Utilisé pour se connecter à un réseau qui utilise des certificats EAP-TLS (Extensible Authentication Protocol Transport Level Security) stockés sur l’ordinateur local pour l’authentification 802.1 X.
ms.assetid: 4cc4cbb7-963f-4771-8a3d-2a37058c9011
title: Exemple de profil de certificat d’ordinateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afb76f0916f2a0d8287a5bf098983e0229c6682decbd3a72386e7b15809c27ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801099"
---
# <a name="machine-certificate-profile-sample"></a>Exemple de profil de certificat d’ordinateur

Cet exemple de profil montre un profil de réseau câblé utilisé pour se connecter à un réseau qui utilise des certificats EAP-TLS (Extensible Authentication Protocol Transport Level Security) stockés sur l’ordinateur local pour l’authentification 802.1 X. Pour afficher un profil qui utilise des certificats EAP-TLS stockés sur une carte à puce, consultez [exemple de certificat de carte à puce](smart-card-certificate-profile-sample.md).

La configuration EAPHost utilisée dans cet exemple de profil sans fil a été dérivée de l’exemple de [Propriétés de connexion EAP-TLS](../eaphost/eap-tls-connection-properties.md) .

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<LANProfile xmlns="https://www.microsoft.com/networking/LAN/profile/v1">
    <MSM>
        <security>
            <OneXEnforced>false</OneXEnforced>
            <OneXEnabled>true</OneXEnabled>
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
</LANProfile>
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples de profil câblé](wired-profile-samples.md)
</dt> </dl>

 

 
