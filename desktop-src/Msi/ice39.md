---
description: ICE39 valide le flux d’informations de synthèse de la base de données.
ms.assetid: 9de72de6-fd9c-4d94-92f7-61b85dff0f6a
title: ICE39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdb912afbe7220eee1aa3bbcd494f6531736279b85c5736f6867fdf8779e39bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528439"
---
# <a name="ice39"></a>ICE39

ICE39 valide le [flux d’informations de synthèse](summary-information-stream.md) de la base de données.

ICE39 vérifie le format des propriétés suivantes :

-   [**Résumé du nombre de mots**](word-count-summary.md)
-   [**Résumé du nombre de pages**](page-count-summary.md)
-   [**Résumé du modèle**](template-summary.md)
-   [**Résumé du numéro de révision**](revision-number-summary.md)
-   [**Créer un résumé de l’heure/date**](create-time-date-summary.md)
-   [**Résumé de l’heure/date du dernier enregistrement**](last-saved-time-date-summary.md)
-   [**Dernier Résumé imprimé**](last-printed-summary.md)

Si la propriété [**Résumé du nombre de mots**](word-count-summary.md) spécifie que la source est compressée, ICE39 publie un avertissement si des fichiers sont également marqués comme compressés dans la colonne attributs de la table de [fichiers](file-table.md). Consultez [utilisation des armoires et des sources compressées](using-cabinets-and-compressed-sources.md).

ICE39 publie un avertissement si la propriété [**Résumé du nombre de mots**](word-count-summary.md) spécifie que le package est conforme au contrôle de compte d’utilisateur et que la [table MsiPackageCertificate](msipackagecertificate-table.md) n’est pas vide.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



