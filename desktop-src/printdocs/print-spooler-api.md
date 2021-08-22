---
description: L’API spouleur d’impression fournit une interface au spouleur d’impression permettant aux applications de gérer les imprimantes et les travaux d’impression.
ms.assetid: b6cc0c9d-9f28-4e80-b847-39c72d98bed6
title: API du spouleur d’impression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64eaa89e0f28aa3bc5479e9b1bb872d0a114678ce3e641394c3919b28f37f4df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460493"
---
# <a name="print-spooler-api"></a>API du spouleur d’impression

L’API spouleur d’impression fournit une interface au spouleur d’impression permettant aux applications de gérer les imprimantes et les travaux d’impression.

L’API spouleur d’impression est utilisée par une application dans le cadre de sa programmation et non directement par les utilisateurs finaux.

Cette section contient des informations sur les rubriques suivantes.



| Rubrique                                                                                             | Description                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Référence d’API du spouleur d’impression](printing-and-print-spooler-reference.md)<br/>                | Informations détaillées sur les fonctions, structures et autres éléments de l’API du spouleur d’impression.<br/>                                                                                                           |
| [Référence de notification d’impression asynchrone](asynchronous-printing-notification.md)<br/> | Descriptions des fonctions, interfaces et énumérations utilisées pour la communication asynchrone entre les applications et les composants hébergés par le spouleur d’impression, tels que les pilotes d’imprimante et les moniteurs de port.<br/> |
| [Référence d’installation du pilote d’imprimante](printer-driver-installation-reference.md)<br/>     | Décrit les fonctions qui installent et configurent les pilotes d’imprimante sur un ordinateur.<br/>                                                                                                                            |



 

le diagramme suivant montre la relation entre l’api du spouleur d’impression et les autres api d’impression qu’une application de Windows native peut utiliser.

![diagramme qui montre la relation entre l’API du spouleur d’impression et les autres API d’impression qu’une application Windows Native peut utiliser](images/print-apis-ps.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[API d’impression XPS](xps-printing.md)
</dt> <dt>

[API ticket d’impression](print-ticket-api.md)
</dt> <dt>

[API d’impression GDI](gdi-printing.md)
</dt> </dl>

 

 




