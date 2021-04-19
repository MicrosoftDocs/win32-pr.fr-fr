---
description: ICE24 valide la table de propriétés dans une base de données Windows Installer.
ms.assetid: 1250677b-691e-46bd-83e0-e349106c820b
title: ICE24
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 193af1e53a3274d1d1307f132fe066ca8940c282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106537041"
---
# <a name="ice24"></a>ICE24

ICE24 valide les propriétés suivantes dans la [table de propriétés](property-table.md):

-   Que la propriété [**ProductCode**](productcode.md) est un type de données [GUID](guid.md) valide.
-   Que la propriété [**ProductVersion**](productversion.md) est une version de produit valide.
-   Que la propriété [**ProductLanguage**](productlanguage.md) est un type de données de [langage](language.md) valide.

## <a name="result"></a>Résultats

ICE24 publie un message d’erreur si l’une de ces propriétés ne se présente pas sous la forme d’un type de données valide.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



