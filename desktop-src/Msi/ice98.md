---
description: ICE98 vérifie le champ de description de la table ODBCDataSource pour une source de données ODBC. Elle utilise la fonction SQLValidDSN pour vérifier que seuls les caractères valides sont utilisés et que la description ne dépasse pas la longueur maximale autorisée.
ms.assetid: ed78db96-10a1-4e42-9147-2309c9ca9c6e
title: ICE98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bf06e97341bd8f15502b1ea1fe43a975dc9cde2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203406"
---
# <a name="ice98"></a><span data-ttu-id="be86e-104">ICE98</span><span class="sxs-lookup"><span data-stu-id="be86e-104">ICE98</span></span>

<span data-ttu-id="be86e-105">ICE98 vérifie le champ de description de la [table ODBCDataSource](odbcdatasource-table.md) pour une source de données ODBC.</span><span class="sxs-lookup"><span data-stu-id="be86e-105">ICE98 verifies the description field of the [ODBCDataSource Table](odbcdatasource-table.md) for an ODBC data source.</span></span> <span data-ttu-id="be86e-106">Elle utilise la fonction **SQLValidDSN** pour vérifier que seuls les caractères valides sont utilisés et que la description ne dépasse pas la longueur maximale autorisée.</span><span class="sxs-lookup"><span data-stu-id="be86e-106">It uses the **SQLValidDSN** function to check that only valid characters are used, and that the description does not exceed the maximum allowed length.</span></span>

## <a name="result"></a><span data-ttu-id="be86e-107">Résultats</span><span class="sxs-lookup"><span data-stu-id="be86e-107">Result</span></span>

<span data-ttu-id="be86e-108">ICE98 publie les avertissements suivants.</span><span class="sxs-lookup"><span data-stu-id="be86e-108">ICE98 posts the following warnings.</span></span>



| <span data-ttu-id="be86e-109">AVERTISSEMENT ICE98</span><span class="sxs-lookup"><span data-stu-id="be86e-109">ICE98 warning</span></span>                    | <span data-ttu-id="be86e-110">Description</span><span class="sxs-lookup"><span data-stu-id="be86e-110">Description</span></span>                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be86e-111">Le nom de la source de données n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="be86e-111">The data source name is invalid.</span></span> | <span data-ttu-id="be86e-112">La valeur dans la colonne Description de la [table ODBCDataSource](odbcdatasource-table.md) contient des caractères non valides ou est trop longue, ce qui signifie qu’elle dépasse la \_ \_ \_ longueur de DSN max. de 32.</span><span class="sxs-lookup"><span data-stu-id="be86e-112">The value in the Description column of the [ODBCDataSource Table](odbcdatasource-table.md) either contains invalid characters or is too long, which means that it exceeds the SQL\_MAX\_DSN\_LENGTH of 32.</span></span> |



 

## <a name="example"></a><span data-ttu-id="be86e-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="be86e-113">Example</span></span>

<span data-ttu-id="be86e-114">ICE98 signale les avertissements suivants pour l’exemple :</span><span class="sxs-lookup"><span data-stu-id="be86e-114">ICE98 reports the following warnings for the example:</span></span>

``` syntax
The data source name is invalid: !
The data source name is invalid: <String of length > 32>
```

<span data-ttu-id="be86e-115">[Table ODBCDataSource](odbcdatasource-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="be86e-115">[ODBCDataSource Table](odbcdatasource-table.md) (partial)</span></span>



| <span data-ttu-id="be86e-116">DataSource</span><span class="sxs-lookup"><span data-stu-id="be86e-116">DataSource</span></span> | <span data-ttu-id="be86e-117">Description</span><span class="sxs-lookup"><span data-stu-id="be86e-117">Description</span></span>                      |
|------------|----------------------------------|
| <span data-ttu-id="be86e-118">BadChar</span><span class="sxs-lookup"><span data-stu-id="be86e-118">BadChar</span></span>    | <span data-ttu-id="be86e-119">!</span><span class="sxs-lookup"><span data-stu-id="be86e-119">!</span></span>                                |
| <span data-ttu-id="be86e-120">TooLong</span><span class="sxs-lookup"><span data-stu-id="be86e-120">TooLong</span></span>    | <span data-ttu-id="be86e-121"><String of length > 32></span><span class="sxs-lookup"><span data-stu-id="be86e-121"><String of length > 32></span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="be86e-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="be86e-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be86e-123">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="be86e-123">ICE Reference</span></span>](ice-reference.md)
</dt> <dt>

[<span data-ttu-id="be86e-124">Table ODBCDataSource</span><span class="sxs-lookup"><span data-stu-id="be86e-124">ODBCDataSource Table</span></span>](odbcdatasource-table.md)
</dt> </dl>

 

 



