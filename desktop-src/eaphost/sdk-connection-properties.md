---
title: Propriétés de connexion du SDK
description: En savoir plus sur les propriétés de connexion SDK. Consultez un exemple qui est une instance du schéma natif eaphostconfig.
ms.assetid: 34c9b423-4f4c-484e-86d7-4594566cd396
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edbd404246055a3c94daff4c029a94f16adfe51b
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "103734597"
---
# <a name="sdk-connection-properties"></a><span data-ttu-id="722f6-104">Propriétés de connexion du SDK</span><span class="sxs-lookup"><span data-stu-id="722f6-104">SDK Connection Properties</span></span>

<span data-ttu-id="722f6-105">Cet exemple est une instance du schéma natif [eaphostconfig](eaphostconfigschema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="722f6-105">This sample is an instance of the [eaphostconfig](eaphostconfigschema-schema.md) native schema.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="722f6-106">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="722f6-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="722f6-107">Propriétés de connexion</span><span class="sxs-lookup"><span data-stu-id="722f6-107">Connection Properties</span></span>](connection-profiles.md)
</dt> <dt>

[<span data-ttu-id="722f6-108">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="722f6-108">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> </dl>

 

 




