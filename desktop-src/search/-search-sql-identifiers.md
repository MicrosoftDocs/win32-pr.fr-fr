---
description: Les identificateurs spécifient les noms des colonnes (parfois appelées propriétés), les catalogues et les alias.
ms.assetid: 799afe2c-9217-4006-a4a3-644e5393993c
title: Identificateurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df79bd0d70564ea3e87ff4821a1cb59e3d0a5eb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112423"
---
# <a name="identifiers"></a><span data-ttu-id="d4dc6-103">Identificateurs</span><span class="sxs-lookup"><span data-stu-id="d4dc6-103">Identifiers</span></span>

<span data-ttu-id="d4dc6-104">Les identificateurs spécifient les noms des colonnes (parfois appelées propriétés), les catalogues et les alias.</span><span class="sxs-lookup"><span data-stu-id="d4dc6-104">Identifiers specify the names of columns (sometimes referred to as properties), catalogs, and aliases.</span></span> <span data-ttu-id="d4dc6-105">Par exemple, System. ItemName et System. DateCreated sont les identificateurs de deux colonnes de propriété définies par le système.</span><span class="sxs-lookup"><span data-stu-id="d4dc6-105">For example, System.ItemName and System.DateCreated are the identifiers of two system-defined property columns.</span></span> <span data-ttu-id="d4dc6-106">En revanche, les littéraux spécifient des valeurs numériques et de chaîne.</span><span class="sxs-lookup"><span data-stu-id="d4dc6-106">Literals, by contrast, specify string and numeric values.</span></span>


<span data-ttu-id="d4dc6-107">Vous pouvez créer des identificateurs d’une longueur maximale de 128 caractères, et dans l’un des deux types, distingués par les caractères utilisés dans le nom de l’identificateur :</span><span class="sxs-lookup"><span data-stu-id="d4dc6-107">You can create identifiers that are up to 128 characters long, and in one of two types, distinguished by the characters used in the identifier name:</span></span>

-   <span data-ttu-id="d4dc6-108">Les **identificateurs réguliers** contiennent uniquement les caractères a-z, a-z, 0-9, le trait de soulignement () et le \_ point (.), et ils commencent par une lettre.</span><span class="sxs-lookup"><span data-stu-id="d4dc6-108">**Regular identifiers** contain only the characters A-Z, a-z, 0-9, underscore (\_), and dot (.), and they begin with a letter.</span></span> <span data-ttu-id="d4dc6-109">Vous n’avez pas besoin de placer les identificateurs réguliers entre guillemets doubles ("").</span><span class="sxs-lookup"><span data-stu-id="d4dc6-109">You do not need to enclose regular identifiers in double quotation marks (" ").</span></span>
-   <span data-ttu-id="d4dc6-110">Les **identificateurs délimités** peuvent contenir n’importe quel caractère Unicode valide et doivent être placés entre guillemets doubles.</span><span class="sxs-lookup"><span data-stu-id="d4dc6-110">**Delimited identifiers** can contain any valid Unicode character and must be enclosed in double quotation marks.</span></span>

> [!Note]  
> <span data-ttu-id="d4dc6-111">Dans les clauses FREETEXT et CONTAINs, vous pouvez utiliser l’astérisque ( \* ) comme identificateur de colonne spécial lorsque vous souhaitez spécifier que la recherche Windows inclut toutes les propriétés indexées dans la requête.</span><span class="sxs-lookup"><span data-stu-id="d4dc6-111">In FREETEXT and CONTAINS clauses, you can use the asterisk (\*) as a special column identifier when you want to specify that Windows Search includes all of the indexed properties in the query.</span></span> <span data-ttu-id="d4dc6-112">Bien qu’il ne s’agisse pas d’un identificateur régulier, il ne requiert pas de guillemets doubles.</span><span class="sxs-lookup"><span data-stu-id="d4dc6-112">Although it is not a regular identifier, it does not require double quotation marks.</span></span>

 

 

 



