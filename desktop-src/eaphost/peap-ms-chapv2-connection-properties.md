---
title: Propriétés de connexion PEAP MS-CHAPv2
description: En savoir plus sur les propriétés de connexion PEAP MS-CHAPv2. Consultez un exemple qui est une instance du schéma hérité mschapv2connectionpropertiesv1.
ms.assetid: a289343a-b702-4be2-baf5-2d004a8a8fea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcac1210eb0fb1606600366618b28c0a4276fa80
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104463854"
---
# <a name="peap-ms-chapv2-connection-properties"></a><span data-ttu-id="2a5a2-104">Propriétés de connexion PEAP MS-CHAPv2</span><span class="sxs-lookup"><span data-stu-id="2a5a2-104">PEAP MS-CHAPv2 Connection Properties</span></span>

<span data-ttu-id="2a5a2-105">Cet exemple est une instance du schéma hérité [mschapv2connectionpropertiesv1](mschapv2connectionpropertiesv1schema-schema.md) ..</span><span class="sxs-lookup"><span data-stu-id="2a5a2-105">This sample is an instance of the [mschapv2connectionpropertiesv1](mschapv2connectionpropertiesv1schema-schema.md) legacy schema..</span></span>

``` syntax
  <?xml version="1.0" ?> 
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
```

## <a name="related-topics"></a><span data-ttu-id="2a5a2-106">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2a5a2-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a5a2-107">Propriétés de connexion</span><span class="sxs-lookup"><span data-stu-id="2a5a2-107">Connection Properties</span></span>](connection-profiles.md)
</dt> <dt>

[<span data-ttu-id="2a5a2-108">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="2a5a2-108">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> </dl>

 

 




