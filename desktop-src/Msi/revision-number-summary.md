---
description: Pour un package d’installation, la propriété Résumé du numéro de révision contient le code du package du programme d’installation.
ms.assetid: 79702b44-846a-4672-8e22-9b6e3f4b4678
title: Propriété Résumé du numéro de révision
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e97df1eafec2d543be0f975b9f5daca7728267b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541718"
---
# <a name="revision-number-summary-property"></a><span data-ttu-id="42db0-103">Propriété Résumé du numéro de révision</span><span class="sxs-lookup"><span data-stu-id="42db0-103">Revision Number Summary property</span></span>

<span data-ttu-id="42db0-104">Pour un package d’installation, la propriété **Résumé du numéro de révision** contient le [*code*](p-gly.md) du package du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="42db0-104">For an installation package, the **Revision Number Summary** property contains the [*package code*](p-gly.md) for the installer package.</span></span> <span data-ttu-id="42db0-105">Pour plus d’informations sur les codes de package, consultez [codes de package](package-codes.md).</span><span class="sxs-lookup"><span data-stu-id="42db0-105">For more information about package codes, see [Package Codes](package-codes.md).</span></span>

<span data-ttu-id="42db0-106">Pour une transformation, la propriété **Résumé du numéro de révision** répertorie les GUID et la version des codes de produit des nouveaux produits et originaux et le GUID du code de mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="42db0-106">For a transform, the **Revision Number Summary** property lists the product code GUIDs and version of the new and original products and the upgrade code GUID.</span></span> <span data-ttu-id="42db0-107">La liste est séparée par des points-virgules, comme suit.</span><span class="sxs-lookup"><span data-stu-id="42db0-107">The list is separated with semicolons as follows.</span></span>

<span data-ttu-id="42db0-108">«Original-version du produit original-version du produit ; New-Product code New-Product-version ; Upgrade-code»</span><span class="sxs-lookup"><span data-stu-id="42db0-108">"Original-Product-Code Original-Product-Version ; New-Product Code New-Product-Version; Upgrade-Code"</span></span>

<span data-ttu-id="42db0-109">Pour un package de correctifs, la propriété **Résumé du numéro de révision** spécifie le code correctif du GUID pour le correctif.</span><span class="sxs-lookup"><span data-stu-id="42db0-109">For a patch package, the **Revision Number Summary** property specifies the GUID patch code for the patch.</span></span> <span data-ttu-id="42db0-110">Elle peut être suivie d’une liste de GUID de code correctif pour les correctifs obsolètes à supprimer lorsque ce correctif est appliqué.</span><span class="sxs-lookup"><span data-stu-id="42db0-110">This can be followed by a list of patch code GUIDs for obsolete patches that are to be removed when this patch is applied.</span></span> <span data-ttu-id="42db0-111">Les codes de correctif sont concaténés, sans délimiteur, en séparant les GUID dans la liste.</span><span class="sxs-lookup"><span data-stu-id="42db0-111">The patch codes are concatenated with no delimiters separating GUIDs in the list.</span></span>

<span data-ttu-id="42db0-112">\* \* Windows Installer 3,0 : \* \* si des informations de séquencement sont présentes dans la [table MsiPatchSequence](msipatchsequence-table.md), Windows Installer 3,0 utilise les informations de séquencement dans le tableau et ignore la liste des correctifs obsolètes inclus dans la propriété **Résumé du numéro de révision** .</span><span class="sxs-lookup"><span data-stu-id="42db0-112">\*\*Windows Installer 3.0:  \*\* If there is sequencing information present in the [MsiPatchSequence table](msipatchsequence-table.md), Windows Installer 3.0 uses the sequencing information in the table and ignores the list of obsolete patches included in the **Revision Number Summary** property.</span></span> <span data-ttu-id="42db0-113">Windows Installer 3,0 peuvent toujours utiliser les informations sur les correctifs obsolètes dans la propriété **Résumé du numéro de révision** si le package ne contient pas de table MsiPatchSequence.</span><span class="sxs-lookup"><span data-stu-id="42db0-113">Windows Installer 3.0 can still use the obsolete patch information in the **Revision Number Summary** property if the package does not contain a MsiPatchSequence table.</span></span>

<span data-ttu-id="42db0-114">\* \* Windows Installer 2,0 : \* \* la [table MsiPatchSequence](msipatchsequence-table.md) n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="42db0-114">\*\*Windows Installer 2.0:  \*\* The [MsiPatchSequence table](msipatchsequence-table.md) is not supported.</span></span> <span data-ttu-id="42db0-115">Windows Installer 2,0 peuvent toujours utiliser les informations sur les correctifs obsolètes dans la propriété **Résumé du numéro de révision** si le package ne contient pas de table MsiPatchSequence.</span><span class="sxs-lookup"><span data-stu-id="42db0-115">Windows Installer 2.0 can still use the obsolete patch information in the **Revision Number Summary** property if the package does not contain a MsiPatchSequence table.</span></span>

<span data-ttu-id="42db0-116">Cette propriété de résumé est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="42db0-116">This summary property is required.</span></span>

## <a name="requirements"></a><span data-ttu-id="42db0-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="42db0-117">Requirements</span></span>



| <span data-ttu-id="42db0-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="42db0-118">Requirement</span></span> | <span data-ttu-id="42db0-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="42db0-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42db0-120">Version</span><span class="sxs-lookup"><span data-stu-id="42db0-120">Version</span></span><br/> | <span data-ttu-id="42db0-121">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="42db0-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="42db0-122">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="42db0-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="42db0-123">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="42db0-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="42db0-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42db0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42db0-125">Descriptions des propriétés de synthèse</span><span class="sxs-lookup"><span data-stu-id="42db0-125">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




