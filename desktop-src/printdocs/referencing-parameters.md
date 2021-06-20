---
description: En savoir plus sur le référencement des paramètres et l’élément ParameterDef. L’option taille de média personnalisée est un exemple d’option qui comprend un élément ParameterRef.
ms.assetid: 2c796d5c-1556-4348-83e2-23e93780ebc1
title: Référencement des paramètres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 650790af5ca6849bd082b4819dd4c411adea320f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405322"
---
# <a name="referencing-parameters"></a>Référencement des paramètres

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

L’option Personnaliser la taille du média est un exemple concret d’une option qui comprend un élément ParameterRef. Notez qu’il fait référence à deux paramètres : PageMediaSizeMediaSizeWidth et PageMediaSizeMediaSizeHeight. Chaque instance ParameterRef fait référence à une instance ParameterDef qui est définie ailleurs dans le document PrintCapabilities. Pour plus d’informations sur l’élément ParameterDef, consultez [ParameterDef](parameterdef.md). Pour obtenir des informations conceptuelles sur la définition des paramètres, consultez [ParameterDef et ParameterInit Elements](parameterdef-and-parameterinit-elements.md).

``` syntax
<!--Example of ParamterRef usage within a Feature-->
<psf:Option name="psk:CustomMediaSize" constrained="psk:None">
  <psf:ScoredProperty name="psk:MediaSizeWidth">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeWidth" />
  </psf:ScoredProperty>
  <psf:ScoredProperty name="psk:MediaSizeHeight">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeHeight" />
  </psf:ScoredProperty>
</psf:Option>
```

La simple création d’une option paramétrable n’est pas suffisante pour s’assurer que l’option sera gérée et traitée correctement. Le fournisseur et les clients PrintCapabilities/PrintTicket doivent fournir une prise en charge supplémentaire pour implémenter correctement des instances d’option paramétrées. Les comportements requis sont décrits dans les sections suivantes.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



