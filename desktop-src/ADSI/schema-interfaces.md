---
title: Interfaces de schéma
description: Interfaces de schéma
ms.assetid: b3427202-352b-4b35-877e-d28fb3d3906a
ms.tgt_platform: multiple
keywords:
- interfaces ADSI des interfaces de schéma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f414fdea2418fb92a0a3c8c9e8bf88eb6d7f00b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939581"
---
# <a name="schema-interfaces"></a>Interfaces de schéma

Le conteneur de schéma contient un ensemble de définitions de schéma qui sont attachées à une partie de l’arborescence d’espace de noms du fournisseur. En règle générale, chaque instance d’un espace de noms a son propre schéma. Par exemple, dans l’illustration suivante, l’exemple de fournisseur ADSI définit un conteneur de schéma dans chacun des nœuds racine « Seattle » et « Toronto ».

![relation contenant-contenu de schéma](images/schemacont.png)

Pour créer une implémentation ADSI pour un fournisseur, vous devez fournir des objets de gestion de schéma qui reflètent l’espace de noms sous-jacent du fournisseur et qui prennent en charge les interfaces de schéma ADSI. La liste suivante répertorie les interfaces de schéma ADSI qui sont contenues dans le conteneur de schéma.

-   [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) représente des classes de service d’annuaire.
-   [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) représente les propriétés du service d’annuaire qui ont une ou plusieurs valeurs.
-   [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax) représente le type Variant unique.

Les interfaces définies par ADSI peuvent prendre en charge des propriétés spécifiques et des syntaxes pour votre fournisseur. Les fournisseurs peuvent choisir d’étendre une définition ADSI à l’aide des méthodes qui créent et accèdent aux propriétés, par exemple, vous pouvez utiliser les méthodes de l’interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) , telles que [**obtenir**](/windows/desktop/api/Iads/nf-iads-iads-get), [**GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex), [**put**](/windows/desktop/api/Iads/nf-iads-iads-put) [**et.**](/windows/desktop/api/Iads/nf-iads-iads-putex) Les fournisseurs peuvent également prendre en charge des propriétés supplémentaires via des interfaces supplémentaires. Pour obtenir la liste complète des interfaces ADSI, consultez [interfaces ADSI](adsi-interfaces.md).

Un composant fournisseur ADSI avec un espace de noms complexe peut permettre l’existence de plusieurs schémas dans une instance d’espace de noms, chacun d’entre eux ayant une autre partie de l’arborescence. Toutefois, la propriété [**IADs :: Schema**](iads-property-methods.md) d’un objet nomme toujours sa propre définition de schéma.

 

 




