---
description: Utilisé pour se connecter à un réseau qui utilise des certificats EAP-TLS (Extensible Authentication Protocol Transport Level Security) stockés sur une carte à puce pour l’authentification 802.1 X.
ms.assetid: cb6758fc-1cce-4e62-adf7-0976957a49b0
title: Exemple de profil de certificat de carte à puce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13373ea66a7ed93ad527715de9f32d4f72705be5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530274"
---
# <a name="smart-card-certificate-profile-sample"></a><span data-ttu-id="67feb-103">Exemple de profil de certificat de carte à puce</span><span class="sxs-lookup"><span data-stu-id="67feb-103">Smart Card Certificate Profile Sample</span></span>

<span data-ttu-id="67feb-104">Cet exemple de profil montre un profil de réseau câblé utilisé pour se connecter à un réseau qui utilise des certificats EAP-TLS (Extensible Authentication Protocol Transport Level Security) stockés sur une carte à puce pour l’authentification 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="67feb-104">This profile sample shows a wired network profile used to connect to a network that uses Extensible Authentication Protocol Transport Level Security (EAP-TLS) certificates stored on a smart card for 802.1X authentication.</span></span> <span data-ttu-id="67feb-105">Pour afficher un profil qui utilise des certificats EAP-TLS stockés sur l’ordinateur local, consultez [exemple de profil de certificat d’ordinateur](machine-certificate-profile-sample.md).</span><span class="sxs-lookup"><span data-stu-id="67feb-105">To see a profile that uses EAP-TLS certificates stored on the local machine, see [Machine Certificate Profile Sample](machine-certificate-profile-sample.md).</span></span>

<span data-ttu-id="67feb-106">La configuration EAPHost utilisée dans cet exemple de profil sans fil a été dérivée de l’exemple de [Propriétés de connexion EAP-TLS](../eaphost/eap-tls-connection-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="67feb-106">The EAPHost configuration used in this wireless profile sample was derived from the [EAP-TLS Connection Properties](../eaphost/eap-tls-connection-properties.md) sample.</span></span>

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
                                        <eapTls:SmartCard />
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

## <a name="related-topics"></a><span data-ttu-id="67feb-107">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="67feb-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67feb-108">Exemples de profil câblé</span><span class="sxs-lookup"><span data-stu-id="67feb-108">Wired Profile Samples</span></span>](wired-profile-samples.md)
</dt> </dl>

 

 
