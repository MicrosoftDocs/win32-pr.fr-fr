---
description: Utilisé pour se connecter à un réseau qui utilise le protocole EAP-MSCHAPv2 (Protected Extensible Authentication Protocol) avec le protocole PEAP-MSCHAPv2 (Microsoft Challenge Handshake Authentication Protocol version 2) avec un nom d’utilisateur/mot de passe pour l’authentification 802.1 X.
ms.assetid: b5dde0d0-940f-40ec-b24d-95a76325ff1b
title: Exemple de profil PEAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a2529efb7db131d03807bc5b09c7599a66a7e49d5938edfdde9b98c07291b3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800679"
---
# <a name="peap-profile-sample"></a>Exemple de profil PEAP

Cet exemple de profil montre un profil de réseau câblé utilisé pour se connecter à un réseau qui utilise le protocole EAP-MSCHAPv2 (Protected Extensible Authentication Protocol) avec le protocole PEAP-MSCHAPv2 (Microsoft Challenge Handshake Authentication Protocol version 2) avec le mot de passe * UserName * **/**  pour l’authentification 802.1 x. L’utilisateur est invité à entrer des informations d’identification.

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
                                           <msChapV2:UseWinLogonCredentials>false</msChapV2:UseWinLogonCredentials> 
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
</LANProfile>
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples de profil câblé](wired-profile-samples.md)
</dt> </dl>

 

 



