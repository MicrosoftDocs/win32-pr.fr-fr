---
description: La propriété de résumé du nombre de caractères est utilisée uniquement dans les transformations.
ms.assetid: d26d24a5-558e-4333-ae39-ffba1bbc5247
title: Propriété de résumé du nombre de caractères
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afc99c065721f0f0b94691a12e00204305940efd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530530"
---
# <a name="character-count-summary-property"></a><span data-ttu-id="11304-103">Propriété de résumé du nombre de caractères</span><span class="sxs-lookup"><span data-stu-id="11304-103">Character Count Summary property</span></span>

<span data-ttu-id="11304-104">La propriété de **Résumé du nombre de caractères** est utilisée uniquement dans les transformations.</span><span class="sxs-lookup"><span data-stu-id="11304-104">The **Character Count Summary** property is only used in transforms.</span></span> <span data-ttu-id="11304-105">Cette partie du flux d’informations de résumé est divisée en mots de 2 16 bits.</span><span class="sxs-lookup"><span data-stu-id="11304-105">This part of the summary information stream is divided into two 16-bit words.</span></span> <span data-ttu-id="11304-106">Le mot supérieur contient les [*indicateurs de validation*](t-gly.md)de la transformation.</span><span class="sxs-lookup"><span data-stu-id="11304-106">The upper word contains the [*transform validation flags*](t-gly.md).</span></span> <span data-ttu-id="11304-107">Le mot inférieur contient les [*indicateurs de condition d’erreur de transformation*](t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="11304-107">The lower word contains the [*transform error condition flags*](t-gly.md).</span></span>

<span data-ttu-id="11304-108">Cette propriété doit avoir la valeur null dans un package d’installation ou un package de correctifs.</span><span class="sxs-lookup"><span data-stu-id="11304-108">This property should be Null in an installation package or patch package.</span></span>

## <a name="requirements"></a><span data-ttu-id="11304-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="11304-109">Requirements</span></span>



| <span data-ttu-id="11304-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="11304-110">Requirement</span></span> | <span data-ttu-id="11304-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="11304-111">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11304-112">Version</span><span class="sxs-lookup"><span data-stu-id="11304-112">Version</span></span><br/> | <span data-ttu-id="11304-113">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="11304-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="11304-114">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="11304-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="11304-115">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="11304-115">Windows Installer on Windows Server 2003 or Windows XP.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="11304-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="11304-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11304-117">Descriptions des propriétés de synthèse</span><span class="sxs-lookup"><span data-stu-id="11304-117">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




