---
description: La propriété ProductLanguage doit être mise à jour vers l’identificateur de langue numérique (LANGID) pour la nouvelle langue.
ms.assetid: e00ef69b-c54b-41de-9230-a7582b260891
title: Mise à jour des propriétés ProductLanguage et ProductCode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37a7537cdb0295075fbfd1b8b58e45a051610cf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536867"
---
# <a name="updating-productlanguage-and-productcode-properties"></a><span data-ttu-id="fac97-103">Mise à jour des propriétés ProductLanguage et ProductCode</span><span class="sxs-lookup"><span data-stu-id="fac97-103">Updating ProductLanguage and ProductCode Properties</span></span>

<span data-ttu-id="fac97-104">La propriété [**ProductLanguage**](productlanguage.md) doit être mise à jour vers l’identificateur de langue numérique (LANGID) pour la nouvelle langue.</span><span class="sxs-lookup"><span data-stu-id="fac97-104">The [**ProductLanguage**](productlanguage.md) property must be updated to the numeric language identifier (LANGID) for the new language.</span></span> <span data-ttu-id="fac97-105">Dans le cas de l’exemple de localisation, la valeur de la propriété **ProductLanguage** doit être remplacée par celle de l’anglais (1033) par celle de l’ID de langue français (1036) dans la [table des propriétés](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="fac97-105">In the case of the localization example, the value of the **ProductLanguage** property must be changed from the LANGID for English (1033) to the LANGID for French (1036) in the [Property table](property-table.md).</span></span>

<span data-ttu-id="fac97-106">La valeur de la propriété [**ProductCode**](productcode.md) dans la [table de propriétés](property-table.md) doit être remplacée par une nouvelle valeur unique lors de la localisation d’une base de données, car un produit localisé est considéré comme un produit différent.</span><span class="sxs-lookup"><span data-stu-id="fac97-106">The value of the [**ProductCode**](productcode.md) property in the [Property table](property-table.md) must be changed to a new, unique value when localizing a database because a localized product is considered a different product.</span></span> <span data-ttu-id="fac97-107">Par exemple, les versions allemande et anglaise d’une application sont considérées comme deux produits différents et doivent avoir des codes de produit différents.</span><span class="sxs-lookup"><span data-stu-id="fac97-107">For example, the German and English versions of an application are considered two different products and must have different product codes.</span></span> <span data-ttu-id="fac97-108">Consultez la section [codes de produit](product-codes.md).</span><span class="sxs-lookup"><span data-stu-id="fac97-108">See [Product Codes](product-codes.md).</span></span>

<span data-ttu-id="fac97-109">Utilisez votre éditeur de table de base de données pour mettre à jour les valeurs des propriétés ProductCode et ProductLanguage dans la table de propriétés.</span><span class="sxs-lookup"><span data-stu-id="fac97-109">Use your database table editor to update the values of the ProductCode and ProductLanguage properties in the Property table.</span></span> <span data-ttu-id="fac97-110">Ne réutilisez pas le GUID affiché si vous copiez cet exemple.</span><span class="sxs-lookup"><span data-stu-id="fac97-110">Do not reuse the GUID shown if you copy this example.</span></span>

[<span data-ttu-id="fac97-111">Table de propriétés</span><span class="sxs-lookup"><span data-stu-id="fac97-111">Property Table</span></span>](property-table.md)



| <span data-ttu-id="fac97-112">Propriété</span><span class="sxs-lookup"><span data-stu-id="fac97-112">Property</span></span>                                   | <span data-ttu-id="fac97-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="fac97-113">Value</span></span>                                  |
|--------------------------------------------|----------------------------------------|
| [<span data-ttu-id="fac97-114">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="fac97-114">**ProductCode**</span></span>](productcode.md)         | <span data-ttu-id="fac97-115">{EE389960-E426-4EEA-B669-AD8129249881}</span><span class="sxs-lookup"><span data-stu-id="fac97-115">{EE389960-E426-4EEA-B669-AD8129249881}</span></span> |
| [<span data-ttu-id="fac97-116">**ProductLanguage**</span><span class="sxs-lookup"><span data-stu-id="fac97-116">**ProductLanguage**</span></span>](productlanguage.md) | <span data-ttu-id="fac97-117">1036</span><span class="sxs-lookup"><span data-stu-id="fac97-117">1036</span></span>                                   |



 

[<span data-ttu-id="fac97-118">Continuer</span><span class="sxs-lookup"><span data-stu-id="fac97-118">Continue</span></span>](updating-a-summary-information-stream.md)

 

 



