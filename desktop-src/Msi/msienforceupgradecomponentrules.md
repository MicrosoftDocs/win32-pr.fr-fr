---
description: Affectez la valeur 1 à la propriété MSIENFORCEUPGRADECOMPONENTRULES sur la ligne de commande ou dans la table de propriétés pour appliquer les règles des composants de mise à niveau pendant les petites mises à jour et les mises à niveau mineures d’un produit particulier.
ms.assetid: 0c8424c7-ab9b-4a09-aaa8-6a3f44c2789f
title: Propriété MSIENFORCEUPGRADECOMPONENTRULES
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85d5946ba3a0001c988ddfe76eeaf95c008205b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540508"
---
# <a name="msienforceupgradecomponentrules-property"></a><span data-ttu-id="114fb-103">Propriété MSIENFORCEUPGRADECOMPONENTRULES</span><span class="sxs-lookup"><span data-stu-id="114fb-103">MSIENFORCEUPGRADECOMPONENTRULES property</span></span>

<span data-ttu-id="114fb-104">Affectez la valeur 1 à la propriété **MSIENFORCEUPGRADECOMPONENTRULES** sur la ligne de commande ou dans la [table de propriétés](property-table.md) pour appliquer les règles des composants de mise à niveau pendant les [petites mises à jour](small-updates.md) et les [mises à niveau mineures](minor-upgrades.md) d’un produit particulier.</span><span class="sxs-lookup"><span data-stu-id="114fb-104">Set the **MSIENFORCEUPGRADECOMPONENTRULES** property to 1 on the command line or in the [Property table](property-table.md) to apply the upgrade component rules during [small updates](small-updates.md) and [minor upgrades](minor-upgrades.md) of a particular product.</span></span> <span data-ttu-id="114fb-105">Pour appliquer les règles pendant les petites mises à jour et les mises à niveau mineures de tous les produits sur l’ordinateur, définissez la stratégie [EnforceUpgradeComponentRules](enforceupgradecomponentrules.md) sur 1.</span><span class="sxs-lookup"><span data-stu-id="114fb-105">To apply the rules during small updates and minor upgrades of all products on the computer, set the [EnforceUpgradeComponentRules](enforceupgradecomponentrules.md) policy to 1.</span></span>

<span data-ttu-id="114fb-106">Lorsque la propriété ou la stratégie a la valeur 1, les [mises](small-updates.md) à jour [mineures et les mises à niveau mineures](minor-upgrades.md) peuvent échouer parce que la mise à jour tente d’effectuer les opérations suivantes qui ne respectent pas les règles du composant de mise à niveau :</span><span class="sxs-lookup"><span data-stu-id="114fb-106">When the property or policy is set to 1, [small updates](small-updates.md) and [minor upgrades](minor-upgrades.md) can fail because the update tries to do the following that violates the upgrade component rules:</span></span>

-   <span data-ttu-id="114fb-107">Ajoutez une nouvelle fonctionnalité au sommet ou au milieu d’une arborescence de fonctionnalités existante.</span><span class="sxs-lookup"><span data-stu-id="114fb-107">Add a new feature to the top or middle of an existing feature tree.</span></span>

    <span data-ttu-id="114fb-108">La nouvelle fonctionnalité doit être ajoutée en tant que nouvelle fonctionnalité feuille à une arborescence de fonctionnalités existante.</span><span class="sxs-lookup"><span data-stu-id="114fb-108">The new feature must be added as a new leaf feature to an existing feature tree.</span></span>

    <span data-ttu-id="114fb-109">Dans ce cas, la valeur [**ProductCode**](productcode.md) du produit peut être modifiée et la mise à jour peut être traitée comme une [mise à niveau majeure](major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="114fb-109">In this case, the [**ProductCode**](productcode.md) of the product can be changed and the update can be treated as a [major upgrade](major-upgrades.md).</span></span>

-   <span data-ttu-id="114fb-110">Supprimer un composant d’une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="114fb-110">Remove a component from a feature.</span></span>

    <span data-ttu-id="114fb-111">Cela peut également se produire si vous modifiez le GUID d’un composant.</span><span class="sxs-lookup"><span data-stu-id="114fb-111">This can also occur if you change the GUID of a component.</span></span> <span data-ttu-id="114fb-112">Le composant identifié par le GUID d’origine semble être supprimé et le composant identifié par le nouveau GUID apparaît en tant que nouveau composant.</span><span class="sxs-lookup"><span data-stu-id="114fb-112">The component identified by the original GUID appears to be removed and the component as identified by the new GUID appears as a new component.</span></span>

    <span data-ttu-id="114fb-113">**Windows Installer 4,5 et versions ultérieures :** Le composant peut être supprimé correctement à l’aide de Windows Installer 4,5 et versions ultérieures, en définissant l’attribut **msidbComponentAttributesUninstallOnSupersedence** dans la [table des composants](component-table.md) ou en définissant la propriété [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md) .</span><span class="sxs-lookup"><span data-stu-id="114fb-113">**Windows Installer 4.5 and later:** The component can be removed correctly using Windows Installer 4.5 and later by setting the **msidbComponentAttributesUninstallOnSupersedence** attribute in the [Component Table](component-table.md) or by setting the [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md) property.</span></span>

    <span data-ttu-id="114fb-114">La valeur [**ProductCode**](productcode.md) du produit peut également être modifiée et la mise à jour peut être traitée comme une [mise à niveau majeure](major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="114fb-114">Alternatively, the [**ProductCode**](productcode.md) of the product can be changed and the update can be treated as a [major upgrade](major-upgrades.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="114fb-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="114fb-115">Requirements</span></span>



| <span data-ttu-id="114fb-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="114fb-116">Requirement</span></span> | <span data-ttu-id="114fb-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="114fb-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="114fb-118">Version</span><span class="sxs-lookup"><span data-stu-id="114fb-118">Version</span></span><br/> | <span data-ttu-id="114fb-119">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="114fb-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="114fb-120">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="114fb-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="114fb-121">Windows Installer 3,0 ou version ultérieure sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="114fb-121">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="114fb-122">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="114fb-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="114fb-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="114fb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="114fb-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="114fb-124">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="114fb-125">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="114fb-125">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




