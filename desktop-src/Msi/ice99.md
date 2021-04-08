---
description: ICE99 vérifie qu’aucun nom de propriété entré dans la table de répertoire ne duplique un nom réservé pour l’utilisation publique ou privée de l’Windows Installer.
ms.assetid: a7657c14-6542-4a7b-a8f7-727b109cfc39
title: ICE99
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7d70aeaf6480e45db5b47f76434f93e49adf317
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757041"
---
# <a name="ice99"></a><span data-ttu-id="ccd0e-103">ICE99</span><span class="sxs-lookup"><span data-stu-id="ccd0e-103">ICE99</span></span>

<span data-ttu-id="ccd0e-104">ICE99 vérifie qu’aucun nom de propriété entré dans la table de [répertoire](directory-table.md) ne duplique un nom réservé pour l’utilisation publique ou privée de l’Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ccd0e-104">ICE99 verifies that no property name entered in the [Directory](directory-table.md) table duplicates a name reserved for the public or private use of the Windows Installer.</span></span>

## <a name="result"></a><span data-ttu-id="ccd0e-105">Résultats</span><span class="sxs-lookup"><span data-stu-id="ccd0e-105">Result</span></span>

<span data-ttu-id="ccd0e-106">ICE99 publie l’erreur suivante.</span><span class="sxs-lookup"><span data-stu-id="ccd0e-106">ICE99 posts the following error.</span></span>



| <span data-ttu-id="ccd0e-107">Erreur ICE99</span><span class="sxs-lookup"><span data-stu-id="ccd0e-107">ICE99 error</span></span>                                                                                                      | <span data-ttu-id="ccd0e-108">Description</span><span class="sxs-lookup"><span data-stu-id="ccd0e-108">Description</span></span>                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccd0e-109">Le nom du répertoire : \[ 1 \] est identique à l’une des propriétés publiques du MSI et peut entraîner des effets secondaires imprévus.</span><span class="sxs-lookup"><span data-stu-id="ccd0e-109">The directory name: \[1\] is the same as one of the MSI Public Properties and can cause unforeseen side effects.</span></span> | <span data-ttu-id="ccd0e-110">La valeur de la colonne Directory de la table [Directory](directory-table.md) duplique un nom de propriété réservé par le Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ccd0e-110">The value in the Directory column of the [Directory](directory-table.md) table duplicates a property name reserved by the Windows Installer.</span></span> |



 

## <a name="example"></a><span data-ttu-id="ccd0e-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="ccd0e-111">Example</span></span>

<span data-ttu-id="ccd0e-112">ICE99 signale l’erreur suivante pour l’exemple :</span><span class="sxs-lookup"><span data-stu-id="ccd0e-112">ICE99 reports the following error for the example:</span></span>

``` syntax
CustomActionData is the same as one of the MSI Public Properties and can cause unforeseen side effects.
```

<span data-ttu-id="ccd0e-113">[Répertoire](directory-table.md) (partiel)</span><span class="sxs-lookup"><span data-stu-id="ccd0e-113">[Directory](directory-table.md) (partial)</span></span>



| <span data-ttu-id="ccd0e-114">Répertoire</span><span class="sxs-lookup"><span data-stu-id="ccd0e-114">Directory</span></span>        | <span data-ttu-id="ccd0e-115">Répertoire \_ parent</span><span class="sxs-lookup"><span data-stu-id="ccd0e-115">Directory\_Parent</span></span> | <span data-ttu-id="ccd0e-116">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="ccd0e-116">DefaultDir</span></span> |
|------------------|-------------------|------------|
| <span data-ttu-id="ccd0e-117">CustomActionData</span><span class="sxs-lookup"><span data-stu-id="ccd0e-117">CustomActionData</span></span> |                   |            |



 

<span data-ttu-id="ccd0e-118">Pour corriger cet avertissement, vous devez modifier le nom de CustomActionData.</span><span class="sxs-lookup"><span data-stu-id="ccd0e-118">To correct this warning you should change the name of CustomActionData.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ccd0e-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ccd0e-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ccd0e-120">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="ccd0e-120">ICE Reference</span></span>](ice-reference.md)
</dt> <dt>

[<span data-ttu-id="ccd0e-121">Table de répertoire</span><span class="sxs-lookup"><span data-stu-id="ccd0e-121">Directory Table</span></span>](directory-table.md)
</dt> <dt>

[<span data-ttu-id="ccd0e-122">Non pris en charge dans Windows Installer 3,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="ccd0e-122">Not Supported in Windows Installer 3.0 and earlier</span></span>](not-supported-in-windows-installer-version-3-0.md)
</dt> </dl>

 

 



