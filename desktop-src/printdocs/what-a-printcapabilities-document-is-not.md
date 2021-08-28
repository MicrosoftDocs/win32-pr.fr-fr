---
description: Découvrez quelques-unes des fonctionnalités et des informations que le document PrintCapabilities n’est pas destiné à fournir.
ms.assetid: 87a897cd-d3aa-488a-b129-9837d3500d0d
title: Ce qu’est un document PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 180c303a21dbed39908d87831a1e01e2965b09a68e1e23a6e1f8793e247556f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119718539"
---
# <a name="what-a-printcapabilities-document-is-not"></a>Ce qu’est un document PrintCapabilities

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Il est utile de répertorier certaines des fonctionnalités et informations que le document PrintCapabilities n’est pas destiné à fournir.

Un document PrintCapabilities :

-   Ne représente pas des données à valeurs multiples (dépendantes de la configuration).

    Chaque document PrintCapabilities est construit pour une configuration spécifique. Aucune propriété ou ScoredProperty dans le document ne peut avoir une valeur qui dépend de la configuration particulière. Dans la version de schéma initiale, le fournisseur PrintCapabilities doit traiter l’entrée PrintTicket et créer un document PrintCapabilities qui contient les valeurs de propriété appropriées pour la configuration spécifiée dans PrintTicket.

-   Ne contient pas d’informations de contrainte.

    Le document PrintCapabilities n’indique pas quelles configurations sont autorisées et qui ne sont pas autorisées. Dans la version de schéma initiale, le fournisseur PrintCapabilities doit stocker toutes les informations nécessaires pour valider les configurations, fournir une méthode qui valide l’entrée PrintTicket et retourner un PrintTicket corrigé dans le cas où le PrintTicket spécifié viole une ou plusieurs contraintes.

-   Ne contient pas d’informations sur l’appareil dynamique.

    Il y a trop de surcharge impliquée dans la construction du document PrintCapabilities pour qu’il soit utilisé pour conserver rapidement les informations d’État, telles que les niveaux d’encre, le papier restant dans chaque plateau ou l’état du bourrage papier.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



