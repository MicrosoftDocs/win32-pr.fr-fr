---
title: Propriétés de connexion du SDK
description: En savoir plus sur les propriétés de connexion SDK. Consultez un exemple qui est une instance du schéma natif eaphostconfig.
ms.assetid: 34c9b423-4f4c-484e-86d7-4594566cd396
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7c514fc276601ee02cc9d24fc4961f07e7be722ab4ff69dae0316687d8d74d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948049"
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

 

 




