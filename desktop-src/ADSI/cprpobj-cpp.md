---
title: CPRPOBJ. COTISATIONS
description: Dans l’exemple de composant fournisseur, les méthodes d’objet de propriété, dans cprpobj. cpp, sont répertoriées dans le tableau suivant.
ms.assetid: 88628b9b-12e6-4d64-9a21-b30f7392a5f2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edb130d6deced939aa718e839c0e7f178329e6a5b14c383dbf1a2719c0f25cfa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117840333"
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



 

 

 




