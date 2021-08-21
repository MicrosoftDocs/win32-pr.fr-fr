---
description: ICE24 valide la table de propriétés dans une base de données Windows Installer.
ms.assetid: 1250677b-691e-46bd-83e0-e349106c820b
title: ICE24
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa3cbeb62285aa9c22a366647dbaeec9e54097a07bb4e876e6bff11bd435cdb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528989"
---
# <a name="ice24"></a>ICE24

ICE24 valide les propriétés suivantes dans la [table de propriétés](property-table.md):

-   Que la propriété [**ProductCode**](productcode.md) est un type de données [GUID](guid.md) valide.
-   Que la propriété [**ProductVersion**](productversion.md) est une version de produit valide.
-   Que la propriété [**ProductLanguage**](productlanguage.md) est un type de données de [langage](language.md) valide.

## <a name="result"></a>Résultat

ICE24 publie un message d’erreur si l’une de ces propriétés ne se présente pas sous la forme d’un type de données valide.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



