---
description: La valeur de la propriété Résumé de l’objet transmet le nom du produit, de la transformation ou du correctif logiciel qui est installé par le package.
ms.assetid: fb08a240-db30-477f-8dc0-701156d73cfc
title: Propriété de résumé de l’objet
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d21139f686bc8a6cfc5ba2edecdfc57c349d84ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535958"
---
# <a name="subject-summary-property"></a><span data-ttu-id="d0f34-103">Propriété de résumé de l’objet</span><span class="sxs-lookup"><span data-stu-id="d0f34-103">Subject Summary property</span></span>

<span data-ttu-id="d0f34-104">La valeur de la propriété Résumé de l' **objet** transmet le nom du produit, de la transformation ou du correctif logiciel qui est installé par le package.</span><span class="sxs-lookup"><span data-stu-id="d0f34-104">The value of the **Subject Summary** property conveys the name of the product, transform, or patch that is installed by the package.</span></span>

<span data-ttu-id="d0f34-105">C’est à l’auteur d’une base de données d’installation, d’une transformation ou d’un package de correctifs de fournir la valeur de cette propriété dans les informations de résumé.</span><span class="sxs-lookup"><span data-stu-id="d0f34-105">It is up to the author of an installation database, transform, or patch package to provide the value of this property in the summary information.</span></span> <span data-ttu-id="d0f34-106">Les auteurs doivent effectuer les opérations suivantes pour déterminer la valeur correcte.</span><span class="sxs-lookup"><span data-stu-id="d0f34-106">Authors should do the following to determine the correct value.</span></span>

-   <span data-ttu-id="d0f34-107">Définissez la propriété Résumé de l' **objet** d’un package d’installation sur la même valeur que la propriété [**ProductName**](productname.md) .</span><span class="sxs-lookup"><span data-stu-id="d0f34-107">Set the **Subject Summary** property in an installation package to the same value as the [**ProductName**](productname.md) property.</span></span>
-   <span data-ttu-id="d0f34-108">Définissez la propriété Résumé de l' **objet** dans une transformation sur la même valeur que la propriété Résumé de l' **objet** dans le package d’installation d’origine.</span><span class="sxs-lookup"><span data-stu-id="d0f34-108">Set the **Subject Summary** property in a transform to the same value as the **Subject Summary** property in the original installation package.</span></span>
-   <span data-ttu-id="d0f34-109">Définissez la propriété Résumé de l' **objet** dans les informations récapitulatives d’un package de correctifs sur une brève description du correctif qui comprend le nom du produit.</span><span class="sxs-lookup"><span data-stu-id="d0f34-109">Set the **Subject Summary** property in the summary information of a patch package to a short description of the patch that includes the name of the product.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0f34-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d0f34-110">Requirements</span></span>



| <span data-ttu-id="d0f34-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d0f34-111">Requirement</span></span> | <span data-ttu-id="d0f34-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0f34-112">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0f34-113">Version</span><span class="sxs-lookup"><span data-stu-id="d0f34-113">Version</span></span><br/> | <span data-ttu-id="d0f34-114">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d0f34-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d0f34-115">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d0f34-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d0f34-116">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="d0f34-116">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d0f34-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0f34-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0f34-118">**PATCHNEWSUMMARYSUBJECT**</span><span class="sxs-lookup"><span data-stu-id="d0f34-118">**PATCHNEWSUMMARYSUBJECT**</span></span>](patchnewsummarysubject.md)
</dt> <dt>

[<span data-ttu-id="d0f34-119">Descriptions des propriétés de synthèse</span><span class="sxs-lookup"><span data-stu-id="d0f34-119">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




