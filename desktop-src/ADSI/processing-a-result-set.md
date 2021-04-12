---
title: Traitement d’un jeu de résultats
description: Un jeu de résultats est retourné sous la forme d’une série de lignes.
ms.assetid: e0949c1c-a31a-440a-ae10-2934ffeb7128
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41ad422494fd2d384b612989e9e36cec7110e021
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316451"
---
# <a name="processing-a-result-set"></a><span data-ttu-id="c6215-103">Traitement d’un jeu de résultats</span><span class="sxs-lookup"><span data-stu-id="c6215-103">Processing a Result Set</span></span>

<span data-ttu-id="c6215-104">Un jeu de résultats est retourné sous la forme d’une série de lignes.</span><span class="sxs-lookup"><span data-stu-id="c6215-104">A result set is returned as a series of rows.</span></span> <span data-ttu-id="c6215-105">Chaque ligne peut contenir ou non un attribut donné.</span><span class="sxs-lookup"><span data-stu-id="c6215-105">Each row may or may not contain a given attribute.</span></span> <span data-ttu-id="c6215-106">Avec le fournisseur OLE DB, le jeu de résultats apparaît comme un jeu de résultats SQL normal.</span><span class="sxs-lookup"><span data-stu-id="c6215-106">With the OLE DB provider, the result set appears similar to a normal SQL result set.</span></span> <span data-ttu-id="c6215-107">Si vous utilisez ADO pour la requête, le [ADODB. L’objet Recordset](/sql/ado/reference/ado-api/recordset-object-ado?view=sql-server-ver15) est utilisé pour parcourir le jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="c6215-107">If you use ADO for the query, the [ADODB.Recordset](/sql/ado/reference/ado-api/recordset-object-ado?view=sql-server-ver15) object is used for traversing the result set.</span></span> <span data-ttu-id="c6215-108">[**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) (disponible uniquement à partir de langages qui prennent en charge les liaisons vtable) contient des membres pour déplacer le curseur de ligne et vérifier les valeurs de propriété dans une ligne donnée.</span><span class="sxs-lookup"><span data-stu-id="c6215-108">[**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) (available only from languages that support vtable bindings) contains members for moving the row cursor and checking property values in a given row.</span></span> <span data-ttu-id="c6215-109">Vous pouvez également utiliser [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) pour récupérer et définir des propriétés.</span><span class="sxs-lookup"><span data-stu-id="c6215-109">Alternatively, you can use [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) to get and set properties.</span></span>

 

 