---
description: En savoir plus sur l’ajout d’instances de propriété. Le schéma d’impression permet de présenter des instances de propriété dans une instance d’option.
ms.assetid: dac287a9-77ca-44d8-8019-b05e4c61dc52
title: Ajout d’instances de propriété
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5af1a84435ec67c3f27615693e153c6a764e4451d93cb7ff5c73970a39587296
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950799"
---
# <a name="adding-property-instances"></a>Ajout d’instances de propriété

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Le schéma d’impression permet de présenter des instances de propriété dans une instance d’option. Les instances de propriété définies dans le document PrintCapabilities ne sont pas propagées vers les instances d’option enregistrées dans PrintTicket. Les éléments de propriété n’affectent pas le résultat du processus de notation lorsque deux instances d’option sont comparées, mais les instances ScoredProperty affectent ce processus. Tous les pilotes de périphérique qui implémentent un algorithme de notation doivent respecter cette Convention. Les fournisseurs PrintCapabilities sont autorisés à ajouter des instances de propriété à une option si ces instances sont spécifiques à cette option particulière, et pas d’autres, ou si le fournisseur prévoit que la valeur de cette propriété s’affiche pour chaque option de la fonctionnalité. Par exemple, supposons que la propriété PrintRate dépend de l’option sélectionnée pour la fonctionnalité PageResolution. Si la propriété PrintRate a été placée au niveau racine du document PrintCapabilities, elle est à valeur unique et reflète uniquement le taux d’impression pour la résolution actuellement sélectionnée. Toutefois, si la propriété PrintRate a été placée dans chaque option PageResolution, chaque instance de la propriété PrintRate peut refléter la vitesse d’impression de l’option PageResolution qui l’a contenue. Le document PrintCapabilities contient plusieurs définitions pour PrintRate, l’une correspondant à chaque option PageResolution. À l’aide d’une représentation sténographique, le PrintCapabilities contiendra :

``` syntax
<psf:Feature name="psk:PageResolution">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:ResolutionX">
      <psf:Value xsi:type="xs:string">800dpi</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:ResolutionY">
      <psf:Value xsi:type="xs:string">600dpi</psf:Value>
    </psf:ScoredProperty>
    <!-- Note: The following Property is not part of the Print Schema Framework -->
    <!-- It is included for illustration purposes. -->
    <!-- It is shown as a privately defined implementation-->
    <Property name="FabrikamES500:PrintRate">
      <Value xsi:type="string">20ppm</Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

Dans certains cas, le fait de placer une propriété de taux d’impression dans chaque option de résolution est plus pratique pour le client, car le client peut déterminer en un clin d’œil l’effet de chaque option de résolution sur le taux d’impression, sans avoir à obtenir un nouveau document PrintCapabilities pour chaque paramètre de résolution.

Notez également que les instances de propriété peuvent également être ajoutées en tant qu’éléments enfants d’éléments de fonctionnalité. Cela est utile si des instances de propriété ou des valeurs d’instances de propriété sont spécifiques à chaque fonctionnalité. Par exemple, il peut y avoir une propriété qui spécifie s’il est possible de sélectionner une seule option à la fois pour une fonctionnalité, ou si plusieurs options peuvent être sélectionnées. Il s’agit de l’une des propriétés choisies \_ \_ dans les fichiers PPD et GPD. Étant donné que certaines instances de fonctionnalités peuvent être identifiées comme en PICK \_ un, tandis que d’autres peuvent être identifiées en tant que sélection \_ de plusieurs, cette propriété doit être définie pour chaque fonctionnalité. La recherche de la propriété en tant qu’élément enfant de la fonctionnalité produit l’association entre la propriété et la fonctionnalité.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



