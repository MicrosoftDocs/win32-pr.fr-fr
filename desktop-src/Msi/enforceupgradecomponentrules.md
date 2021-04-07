---
description: Il s’agit d’une stratégie système par ordinateur qui peut être utilisée pour appliquer des règles de composants de mise à niveau lors de petites mises à jour et de mises à niveau mineures.
ms.assetid: 0d39c059-d936-454c-aed8-efedd3da7473
title: EnforceUpgradeComponentRules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5a2fc093c2f0beb4167374f93447d978bbca8eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952179"
---
# <a name="enforceupgradecomponentrules"></a><span data-ttu-id="d4450-103">EnforceUpgradeComponentRules</span><span class="sxs-lookup"><span data-stu-id="d4450-103">EnforceUpgradeComponentRules</span></span>

<span data-ttu-id="d4450-104">Il s’agit d’une [stratégie système](system-policy.md) par ordinateur qui peut être utilisée pour appliquer des règles de composants de mise à niveau lors de [petites mises à jour](small-updates.md) et de [mises à niveau mineures](minor-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="d4450-104">This is a per-machine [system policy](system-policy.md) that can be used to apply upgrade component rules during [small updates](small-updates.md) and [minor upgrades](minor-upgrades.md).</span></span>

<span data-ttu-id="d4450-105">Définissez la stratégie EnforceUpgradeComponentRules sur 1 pour appliquer les règles des composants de mise à niveau pendant les [petites mises à jour](small-updates.md) et les [mises à niveau mineures](minor-upgrades.md) de tous les produits sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d4450-105">Set the EnforceUpgradeComponentRules policy to 1 to apply upgrade component rules during [small updates](small-updates.md) and [minor upgrades](minor-upgrades.md) of all products on the computer.</span></span> <span data-ttu-id="d4450-106">Pour appliquer les règles pendant les petites mises à jour et les mises à niveau mineures d’un produit particulier, affectez la valeur 1 à la propriété [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md) sur la ligne de commande ou dans la [table des propriétés](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="d4450-106">To apply the rules during small updates and minor upgrades of a particular product, set the [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md) property to 1 on the command line or in the [Property table](property-table.md).</span></span>

<span data-ttu-id="d4450-107">Lorsque la propriété ou la stratégie a la valeur 1, les [petites mises à jour](small-updates.md) et les [mises à niveau mineures](minor-upgrades.md) peuvent échouer parce que la mise à jour tente d’effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4450-107">When the property or policy has been set to 1, [small updates](small-updates.md) and [minor upgrades](minor-upgrades.md) can fail because the update attempts to do the following:</span></span>

-   <span data-ttu-id="d4450-108">Ajoutez une nouvelle fonctionnalité au sommet ou au milieu d’une arborescence de fonctionnalités existante.</span><span class="sxs-lookup"><span data-stu-id="d4450-108">Add a new feature to the top or middle of an existing feature tree.</span></span>

    <span data-ttu-id="d4450-109">La nouvelle fonctionnalité doit être ajoutée en tant que nouvelle fonctionnalité feuille à une arborescence de fonctionnalités existante.</span><span class="sxs-lookup"><span data-stu-id="d4450-109">The new feature must be added as a new leaf feature to an existing feature tree.</span></span>

    <span data-ttu-id="d4450-110">Dans ce cas, la valeur [**ProductCode**](productcode.md) du produit peut être modifiée et les mises à jour peuvent être traitées comme une [mise à niveau majeure](major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="d4450-110">In this case, the [**ProductCode**](productcode.md) of the product can be changed and the updates can be treated as a [major upgrade](major-upgrades.md).</span></span>

-   <span data-ttu-id="d4450-111">Supprimer un composant d’une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="d4450-111">Remove a component from a feature.</span></span>

    <span data-ttu-id="d4450-112">Cela peut également se produire si vous modifiez le GUID d’un composant.</span><span class="sxs-lookup"><span data-stu-id="d4450-112">This can also occur if you change the GUID of a component.</span></span> <span data-ttu-id="d4450-113">Le composant identifié par le GUID d’origine semble être supprimé et le composant identifié par le nouveau GUID apparaît en tant que nouveau composant.</span><span class="sxs-lookup"><span data-stu-id="d4450-113">The component identified by the original GUID appears to be removed and the component as identified by the new GUID appears as a new component.</span></span>

    <span data-ttu-id="d4450-114">**Windows Installer 4,5 et versions ultérieures :** Le composant peut être supprimé correctement à l’aide de Windows Installer 4,5 ou version ultérieure en définissant l’attribut **msidbComponentAttributesUninstallOnSupersedence** dans la [table des composants](component-table.md) ou en définissant la propriété [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md) .</span><span class="sxs-lookup"><span data-stu-id="d4450-114">**Windows Installer 4.5 and later:** The component can be removed correctly using Windows Installer 4.5 or later by setting the **msidbComponentAttributesUninstallOnSupersedence** attribute in the [Component table](component-table.md) or by setting the [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md) property.</span></span>

    <span data-ttu-id="d4450-115">La valeur [**ProductCode**](productcode.md) du produit peut également être modifiée et les mises à jour peuvent être traitées comme une [mise à niveau majeure](major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="d4450-115">Alternatively, the [**ProductCode**](productcode.md) of the product can be changed and the updates can be treated as a [major upgrade](major-upgrades.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="d4450-116">Clé de Registre</span><span class="sxs-lookup"><span data-stu-id="d4450-116">Registry Key</span></span>

<span data-ttu-id="d4450-117">**HKEY \_ \_** \\ **Stratégies logicielles** de l’ordinateur local \\  \\ **Microsoft** \\ **Windows** \\ **installer**</span><span class="sxs-lookup"><span data-stu-id="d4450-117">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="d4450-118">Type de données</span><span class="sxs-lookup"><span data-stu-id="d4450-118">Data Type</span></span>

<span data-ttu-id="d4450-119">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="d4450-119">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4450-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d4450-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4450-121">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="d4450-121">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



