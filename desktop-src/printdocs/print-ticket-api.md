---
description: L’API Print ticket fournit aux applications la possibilité de gérer et de convertir les tickets d’impression.
ms.assetid: 4f854c1a-f2e1-48c4-9cc1-8a0fcf1bebed
title: API ticket d’impression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac91cc976addba630bae3f250d244442ba1dd3b61f741575fe21cb250bab4a2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119947792"
---
# <a name="print-ticket-api"></a>API ticket d’impression

L’API Print ticket fournit aux applications la possibilité de gérer et de convertir les tickets d’impression.

Un ticket d’impression est un composant de document XPS qui contient les paramètres d’imprimante préférés pour une page dans un document ou pour un document entier, ou pour un travail d’impression qui contient un ou plusieurs documents. Notez que les tickets d’impression sont uniquement disponibles dans les documents XPS.

Pour que l’imprimante puisse utiliser le ticket d’impression, le ticket d’impression doit être validé par rapport aux caractéristiques de l’imprimante, qui sont définies dans les fonctionnalités d’impression de l’imprimante. L’application effectue cette validation en appelant l’API Print ticket.

PrintTicket et PrintCapabilities sont décrits à l’aide d’éléments du schéma d’impression, qui est défini par la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Cette rubrique contient des informations sur les éléments d’API suivants :

-   [Fonctions de l’API ticket d’impression](print-ticket-api-functions.md)
-   [Énumérations de l’API ticket d’impression](print-ticket-api-enumerations.md)

le diagramme suivant montre la relation entre l’api Ticket d’impression et les autres api d’impression qu’une application Windows native peut utiliser.

![diagramme qui montre la relation entre l’API ticket d’impression et les autres API d’impression qu’une application Windows Native peut utiliser](images/print-apis-pt.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[API d’impression XPS](xps-printing.md)
</dt> <dt>

[API du spouleur d’impression](print-spooler-api.md)
</dt> <dt>

[API d’impression GDI](gdi-printing.md)
</dt> <dt>

[Spécification du schéma d’impression](https://go.microsoft.com/fwlink/?linkid=2022117)
</dt> <dt>

[XML Paper Specification](https://go.microsoft.com/fwlink/?linkid=2022122)
</dt> </dl>

 

 



