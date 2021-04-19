---
description: La propriété Résumé des mots clés dans les bases de données d’installation ou les transformations contient une liste de mots clés.
ms.assetid: e19dc495-e4d4-465f-8464-c60af8985334
title: Propriété Résumé des mots clés
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3828146fef861cd993331045d6a1380d84c2bbc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537582"
---
# <a name="keywords-summary-property"></a><span data-ttu-id="0d323-103">Propriété Résumé des mots clés</span><span class="sxs-lookup"><span data-stu-id="0d323-103">Keywords Summary property</span></span>

<span data-ttu-id="0d323-104">La propriété **Résumé des mots clés** dans les bases de données d’installation ou les transformations contient une liste de mots clés.</span><span class="sxs-lookup"><span data-stu-id="0d323-104">The **Keywords Summary** property in installation databases or transforms contains a list of keywords.</span></span> <span data-ttu-id="0d323-105">Les mots clés peuvent être utilisés par les explorateurs de fichiers pour effectuer des recherches dans les mots clés d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="0d323-105">The keywords may be used by file browsers to do keyword searches for a file.</span></span> <span data-ttu-id="0d323-106">Cette propriété contient la liste des sources du correctif dans un package correctif.</span><span class="sxs-lookup"><span data-stu-id="0d323-106">This property contains a list of sources of the patch in a patch package.</span></span>

<span data-ttu-id="0d323-107">C’est à l’auteur d’une base de données d’installation, d’une transformation ou d’un package de correctifs de fournir la valeur de cette propriété dans les informations de résumé.</span><span class="sxs-lookup"><span data-stu-id="0d323-107">It is up to the author of an installation database, transform, or patch package to provide the value of this property in the summary information.</span></span> <span data-ttu-id="0d323-108">Les auteurs doivent effectuer les opérations suivantes pour déterminer la valeur correcte.</span><span class="sxs-lookup"><span data-stu-id="0d323-108">Authors should do the following to determine the correct value.</span></span>

-   <span data-ttu-id="0d323-109">Dans un package d’installation, définissez la valeur de cette propriété sur une liste de mots clés.</span><span class="sxs-lookup"><span data-stu-id="0d323-109">In an installation package, set the value of this property to a list of keywords.</span></span> <span data-ttu-id="0d323-110">Le mot clé doit inclure « installer », ainsi que des mots clés spécifiques au produit et peut être localisé.</span><span class="sxs-lookup"><span data-stu-id="0d323-110">The keyword should include "Installer" as well as product-specific keywords, and may be localized.</span></span>
-   <span data-ttu-id="0d323-111">Dans une transformation, définissez la valeur de cette propriété sur une liste de mots clés.</span><span class="sxs-lookup"><span data-stu-id="0d323-111">In a transform, set the value of this property to a list of keywords.</span></span> <span data-ttu-id="0d323-112">Le mot clé doit inclure « installer », ainsi que des mots clés spécifiques au produit et peut être localisé.</span><span class="sxs-lookup"><span data-stu-id="0d323-112">The keyword should include "Installer" as well as product-specific keywords, and may be localized.</span></span>
-   <span data-ttu-id="0d323-113">Dans un package correctif, définissez la valeur de cette propriété sur une liste délimitée par des points-virgules des emplacements réseau ou URL des sources du correctif.</span><span class="sxs-lookup"><span data-stu-id="0d323-113">In a patch package, set the value of this property to a semicolon-delimited list of network or URL locations for the sources of the patch.</span></span> <span data-ttu-id="0d323-114">Une fois le correctif installé, le programme d’installation les ajoute à la liste source pour le package de correctifs.</span><span class="sxs-lookup"><span data-stu-id="0d323-114">When the patch is installed, the installer adds these to the source list for the patch package.</span></span> <span data-ttu-id="0d323-115">Si le correctif mis en cache est manquant, le programme d’installation peut rechercher une source à l’emplacement d’origine, un emplacement ajouté à la liste source par la propriété **Résumé des mots clés** ou un emplacement ajouté à la liste source à l’aide des fonctions [**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) ou [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) .</span><span class="sxs-lookup"><span data-stu-id="0d323-115">If the cached patch becomes missing, the installer can search for a source in the original location, a location added to the source list by the **Keywords Summary** property, or a location added to the source list using the [**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) or [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d323-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0d323-116">Requirements</span></span>



| <span data-ttu-id="0d323-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0d323-117">Requirement</span></span> | <span data-ttu-id="0d323-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d323-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d323-119">Version</span><span class="sxs-lookup"><span data-stu-id="0d323-119">Version</span></span><br/> | <span data-ttu-id="0d323-120">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0d323-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0d323-121">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0d323-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0d323-122">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="0d323-122">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0d323-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d323-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d323-124">Descriptions des propriétés de synthèse</span><span class="sxs-lookup"><span data-stu-id="0d323-124">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




