---
title: Propriétés de l’utilisateur MS-CHAPv2 PEAP
description: En savoir plus sur les propriétés PEAP MS-CHAPv2 utilisateur. Consultez un exemple qui est une instance du schéma hérité mschapv2userpropertiesv1.
ms.assetid: af1ed6b1-712e-4b55-9ab4-b6b38f486fb1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d5f5218510f87def8253e3a3f5bd30978523f95e50d7e5aa1b9ede55b96d655
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118784879"
---
# <a name="peap-ms-chapv2-user-properties"></a>Propriétés de l’utilisateur MS-CHAPv2 PEAP

Cet exemple est une instance du schéma hérité [mschapv2userpropertiesv1](mschapv2userpropertiesv1schema-schema.md) .

``` syntax
  <?xml version="1.0" ?> 
  <EapHostUserCredentials xmlns="https://www.microsoft.com/provisioning/EapHostUserCredentials"
    xmlns:eapCommon="https://www.microsoft.com/provisioning/EapCommon" 
    xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapMethodUserCredentials">
    <EapMethod>
      <eapCommon:Type>25</eapCommon:Type> 
      <eapCommon:AuthorId>0</eapCommon:AuthorId> 
    </EapMethod>
    <Credentials xmlns:eapUser="https://www.microsoft.com/provisioning/EapUserPropertiesV1"
      xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
      xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapUserPropertiesV1"
      xmlns:MsPeap="https://www.microsoft.com/provisioning/MsPeapUserPropertiesV1"
      xmlns:MsChapV2="https://www.microsoft.com/provisioning/MsChapV2UserPropertiesV1">
      <baseEap:Eap>
        <baseEap:Type>25</baseEap:Type> 
        <MsPeap:EapType>
          <MsPeap:RoutingIdentity>test</MsPeap:RoutingIdentity> 
          <baseEap:Eap>
            <baseEap:Type>26</baseEap:Type> 
            <MsChapV2:EapType>
              <MsChapV2:Username>test</MsChapV2:Username> 
              <MsChapV2:Password>test</MsChapV2:Password> 
              <MsChapV2:LogonDomain>ias-domain</MsChapV2:LogonDomain> 
            </MsChapV2:EapType>
          </baseEap:Eap>
        </MsPeap:EapType>
      </baseEap:Eap>
    </Credentials>
  </EapHostUserCredentials>
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Propriétés de l’utilisateur](user-profiles.md)
</dt> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> </dl>

 

 




