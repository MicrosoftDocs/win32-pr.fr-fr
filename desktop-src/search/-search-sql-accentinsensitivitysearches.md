---
description: Par défaut, le catalogue et le moteur de recherche Windows sont insensibles aux signes diacritiques, qui sont des points d’accentuation ajoutés aux lettres pour modifier la signification ou la prononciation d’un mot.
ms.assetid: 71007bd4-5232-469c-982b-ff0d24bd0c1f
title: Respect des signes diacritiques dans les recherches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46fb68676418fc109fa24ed2d55fb9602b7ad41d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514792"
---
# <a name="diacritic-sensitivity-in-searches"></a><span data-ttu-id="45883-103">Respect des signes diacritiques dans les recherches</span><span class="sxs-lookup"><span data-stu-id="45883-103">Diacritic Sensitivity in Searches</span></span>

<span data-ttu-id="45883-104">Par défaut, le catalogue et le moteur de recherche Windows sont insensibles aux signes diacritiques, qui sont des points d’accentuation ajoutés aux lettres pour modifier la signification ou la prononciation d’un mot.</span><span class="sxs-lookup"><span data-stu-id="45883-104">By default, the Windows Search engine and catalog are insensitive to diacritics, which are accent marks added to letters to alter a word's meaning or pronunciation.</span></span> <span data-ttu-id="45883-105">Toutefois, Windows Search vous permet de modifier cela pour votre catalogue à l’aide du [Gestionnaire de catalogue](-search-3x-wds-mngidx-catalog-manager.md) pour définir la sensibilité des signes diacritiques.</span><span class="sxs-lookup"><span data-stu-id="45883-105">However, Windows Search enables you to change this for your catalog using the [Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md) to set diacritic sensitivity.</span></span> <span data-ttu-id="45883-106">Par exemple, si la sensibilité des signes diacritiques est définie sur **false**, le catalogue traiterait « Resume » et « Resumé » comme s’il s’agissait du même mot.</span><span class="sxs-lookup"><span data-stu-id="45883-106">For example, with diacritic sensitivity set to **FALSE**, the catalog would treat "resume" and "resumé" as if they were the same word.</span></span>

<span data-ttu-id="45883-107">Au niveau de la couche de requête, les termes de requête avec des signes diacritiques en FREETEXT et des clauses CONTAINs sont passés au moteur, puis normalisés (comme ils le seraient au moment de l’index) pour la mise en correspondance.</span><span class="sxs-lookup"><span data-stu-id="45883-107">At the query layer, query terms with diacritics in FREETEXT and CONTAINS clauses are passed through to the engine and are then normalized (as they would be at index time) for matching.</span></span> <span data-ttu-id="45883-108">La correspondance avec le catalogue est toujours respectée pour les signes diacritiques.</span><span class="sxs-lookup"><span data-stu-id="45883-108">Matching against the catalog is always diacritic sensitive.</span></span>

> [!Note]  
> <span data-ttu-id="45883-109">Ce n’est pas le cas pour les plages de caractères 0x2e81-F8FF et 0x1100-0x11ff.</span><span class="sxs-lookup"><span data-stu-id="45883-109">This is not the case for the character ranges 0x2e81-f8ff and 0x1100-0x11ff.</span></span>

 

 

 



