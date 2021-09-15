---
title: Propriétés de connexion du SDK
description: En savoir plus sur les propriétés de connexion SDK. Consultez un exemple qui est une instance du schéma natif eaphostconfig.
ms.assetid: 34c9b423-4f4c-484e-86d7-4594566cd396
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edbd404246055a3c94daff4c029a94f16adfe51b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519192"
---
# <a name="sdk-connection-properties"></a>Propriétés de connexion du SDK

Cet exemple est une instance du schéma natif [eaphostconfig](eaphostconfigschema-schema.md) .

``` syntax
  <?xml version="1.0" ?> 
  <EapHostConfig xmlns="https://www.microsoft.com/provisioning/EapHostConfig" 
    xmlns:eapCommon="https://www.microsoft.com/provisioning/EapCommon" 
    xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapMethodConfig">
    <EapMethod>
      <eapCommon:Type>40</eapCommon:Type> 
      <eapCommon:AuthorId>100</eapCommon:AuthorId> 
    </EapMethod>
    <Config>
      <EapType>40</EapType> 
      <ConfigData>seatac.bingo.com</ConfigData> 
    </Config>
  </EapHostConfig>
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Propriétés de connexion](connection-profiles.md)
</dt> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> </dl>

 

 




