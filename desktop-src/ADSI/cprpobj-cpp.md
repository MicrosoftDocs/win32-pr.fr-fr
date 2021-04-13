---
title: CPRPOBJ. COTISATIONS
description: Dans l’exemple de composant fournisseur, les méthodes d’objet de propriété, dans cprpobj. cpp, sont répertoriées dans le tableau suivant.
ms.assetid: 88628b9b-12e6-4d64-9a21-b30f7392a5f2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 948409cc135daaffa249f8aa0b3729b34799957c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190744"
---
# <a name="cprpobjcpp"></a>CPRPOBJ. COTISATIONS

Dans l’exemple de composant fournisseur, les méthodes d’objet de propriété, dans cprpobj. cpp, sont répertoriées dans le tableau suivant.



| Méthode                                                 | Description                                                                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| **CSampleDSProperty::CSampleDSProperty**               | Constructeur standard.                                                                                                                          |
| **CSampleDSProperty :: ~ CSampleDSProperty**              | Destructeur standard.                                                                                                                           |
| **CSampleDSProperty :: CreateProperty**                  | Créez un objet de propriété ADS, en recherchant les définitions d’attributs en appelant **SampleDSGetPropertyDefinition**.                              |
| **CSampleDSProperty :: CreateProperty**                  | À partir de la définition d’attribut, créez un objet de propriété, en définissant la correspondance entre les syntaxes ADS prises en charge et les syntaxes du fournisseur. |
| **CSampleDSProperty::AllocatePropertyObject**          | Créez un objet de propriété et chargez ses données de type.                                                                                               |
| **CSampleDSProperty :: QueryInterface**                  | Retourne le pointeur d’interface demandé, s’il est disponible.                                                                                          |
| Méthodes [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) standard.                 |                                                                                                                                                |
| Méthodes [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) standard. |                                                                                                                                                |
| **MapSyntaxIdtoADsSyntax**                             | Définissez la correspondance entre l’ID de syntaxe et la syntaxe ADS.                                                                               |
| **MapSyntaxIdtoSampleDSSyntax**                        | Définissez la correspondance entre l’ID de syntaxe et la syntaxe du fournisseur.                                                                          |



 

 

 




