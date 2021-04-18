---
description: Le programme d’installation définit la dernière propriété enregistrée par Résumé sur une valeur qui varie selon qu’il s’agit d’un package d’installation, d’une transformation ou d’un package de correctifs. Dans un package d’installation, le programme d’installation définit cette propriété sur la valeur de la propriété LogonUser au cours d’une installation d’administration. Les développeurs d’outils d’édition de base de données peuvent utiliser cette propriété pendant le processus de développement pour suivre la dernière personne à modifier la base de données d’installation. Cette propriété doit avoir la valeur null dans une base de données d’expédition finale. Le programme d’installation n’utilise jamais cette propriété et un utilisateur n’a jamais besoin de le modifier. Dans une transformation, cette propriété Summary contient les ID de plateforme et de langue qu’une base de données doit avoir une fois qu’elle a été transformée. La propriété spécifie ce que le résumé de modèle doit être défini dans la nouvelle base de données. Dans un package correctif, cette propriété Summary contient une liste délimitée par des points-virgules de noms de sous-stockage de transformation dans l’ordre dans lequel ils sont appliqués par ce correctif.
ms.assetid: 6da171d9-29db-4524-abc6-77db8fbfca38
title: Dernier enregistrement par propriété de résumé
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dfd1c00863eee3bc31728783042ada8298b2067
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528913"
---
# <a name="last-saved-by-summary-property"></a><span data-ttu-id="bf510-107">Dernier enregistrement par propriété de résumé</span><span class="sxs-lookup"><span data-stu-id="bf510-107">Last Saved By Summary property</span></span>

<span data-ttu-id="bf510-108">Le programme d’installation définit la **dernière propriété enregistrée par Résumé** sur une valeur qui varie selon qu’il s’agit d’un package d’installation, d’une transformation ou d’un package de correctifs.</span><span class="sxs-lookup"><span data-stu-id="bf510-108">The installer sets the **Last Saved by Summary** Property to a value that depends on whether this is an installation package, transform, or patch package.</span></span>

<span data-ttu-id="bf510-109">Dans un package d’installation, le programme d’installation définit cette propriété sur la valeur de la propriété [**LogonUser**](logonuser.md) au cours d’une [installation d’administration](administrative-installation.md).</span><span class="sxs-lookup"><span data-stu-id="bf510-109">In an installation package, the installer sets this property to the value of the [**LogonUser**](logonuser.md) property during an [administrative installation](administrative-installation.md).</span></span> <span data-ttu-id="bf510-110">Les développeurs d’outils d’édition de base de données peuvent utiliser cette propriété pendant le processus de développement pour suivre la dernière personne à modifier la base de données d’installation.</span><span class="sxs-lookup"><span data-stu-id="bf510-110">Developers of database editing tools may use this property during the development process to track the last person to modify the installation database.</span></span> <span data-ttu-id="bf510-111">Cette propriété doit avoir la valeur null dans une base de données d’expédition finale.</span><span class="sxs-lookup"><span data-stu-id="bf510-111">This property should be set to Null in a final shipping database.</span></span> <span data-ttu-id="bf510-112">Le programme d’installation n’utilise jamais cette propriété et un utilisateur n’a jamais besoin de le modifier.</span><span class="sxs-lookup"><span data-stu-id="bf510-112">The installer never uses this property and a user never needs to modify it.</span></span>

<span data-ttu-id="bf510-113">Dans une transformation, cette propriété Summary contient les ID de plateforme et de langue qu’une base de données doit avoir une fois qu’elle a été transformée.</span><span class="sxs-lookup"><span data-stu-id="bf510-113">In a transform, this summary property contains the platform and language ID(s) that a database should have after it has been transformed.</span></span> <span data-ttu-id="bf510-114">La propriété spécifie ce que le [**Résumé de modèle**](template-summary.md) doit être défini dans la nouvelle base de données.</span><span class="sxs-lookup"><span data-stu-id="bf510-114">The property specifies to what the [**Template Summary**](template-summary.md) should be set in the new database.</span></span>

<span data-ttu-id="bf510-115">Dans un package correctif, cette propriété Summary contient une liste délimitée par des points-virgules de noms de sous-stockage de transformation dans l’ordre dans lequel ils sont appliqués par ce correctif.</span><span class="sxs-lookup"><span data-stu-id="bf510-115">In a patch package, this summary property contains a semicolon-delimited list of transform substorage names in the order they are applied by this patch.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf510-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf510-116">Requirements</span></span>



| <span data-ttu-id="bf510-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bf510-117">Requirement</span></span> | <span data-ttu-id="bf510-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf510-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf510-119">Version</span><span class="sxs-lookup"><span data-stu-id="bf510-119">Version</span></span><br/> | <span data-ttu-id="bf510-120">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bf510-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="bf510-121">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bf510-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="bf510-122">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="bf510-122">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bf510-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf510-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf510-124">Descriptions des propriétés de synthèse</span><span class="sxs-lookup"><span data-stu-id="bf510-124">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




