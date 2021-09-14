---
title: Traitement d’un jeu de résultats
description: Un jeu de résultats est retourné sous la forme d’une série de lignes.
ms.assetid: e0949c1c-a31a-440a-ae10-2934ffeb7128
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41ad422494fd2d384b612989e9e36cec7110e021
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127124366"
---
# <a name="processing-a-result-set"></a>Traitement d’un jeu de résultats

Un jeu de résultats est retourné sous la forme d’une série de lignes. Chaque ligne peut contenir ou non un attribut donné. avec le fournisseur de OLE DB, le jeu de résultats apparaît comme un jeu de résultats de SQL normal. Si vous utilisez ADO pour la requête, le [ADODB. L’objet Recordset](/sql/ado/reference/ado-api/recordset-object-ado?view=sql-server-ver15) est utilisé pour parcourir le jeu de résultats. [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) (disponible uniquement à partir de langages qui prennent en charge les liaisons vtable) contient des membres pour déplacer le curseur de ligne et vérifier les valeurs de propriété dans une ligne donnée. Vous pouvez également utiliser [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) pour récupérer et définir des propriétés.

 

 