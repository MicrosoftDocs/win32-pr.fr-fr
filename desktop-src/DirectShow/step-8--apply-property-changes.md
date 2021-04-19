---
description: 'Étape 8 :'
ms.assetid: c54745ef-beeb-40b6-9db6-6e3b5da860f8
title: 'Étape 8 : Appliquer les modifications de propriété'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46425613b8f23981a7b288121dc1a4ab0945452e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521115"
---
# <a name="step-8-apply-property-changes"></a><span data-ttu-id="f9604-104">Étape 8 :</span><span class="sxs-lookup"><span data-stu-id="f9604-104">Step 8.</span></span> <span data-ttu-id="f9604-105">Appliquer les modifications de propriété</span><span class="sxs-lookup"><span data-stu-id="f9604-105">Apply Property Changes</span></span>

<span data-ttu-id="f9604-106">Substituez la méthode [**CBasePropertyPage :: OnApplyChanges**](cbasepropertypage-onapplychanges.md) pour valider les modifications apportées aux propriétés.</span><span class="sxs-lookup"><span data-stu-id="f9604-106">Override the [**CBasePropertyPage::OnApplyChanges**](cbasepropertypage-onapplychanges.md) method to commit any property changes.</span></span> <span data-ttu-id="f9604-107">Dans cet exemple, la \_ variable m lNewVal est mise à jour chaque fois que l’utilisateur fait défiler la barre du curseur.</span><span class="sxs-lookup"><span data-stu-id="f9604-107">In this example, the m\_lNewVal variable is updated whenever the user scrolls the slider bar.</span></span> <span data-ttu-id="f9604-108">La méthode **OnApplyChanges** copie cette valeur dans la \_ variable m lVal, en remplaçant la valeur d’origine :</span><span class="sxs-lookup"><span data-stu-id="f9604-108">The **OnApplyChanges** method copies this value into the m\_lVal variable, overwriting the original value:</span></span>


```C++
HRESULT CGrayProp::OnApplyChanges(void)
{
    m_lVal = m_lNewVal;
    return S_OK;
} 
```



<span data-ttu-id="f9604-109">Suivant : [étape 9. Déconnectez la page de propriétés](step-9--disconnect-the-property-page.md).</span><span class="sxs-lookup"><span data-stu-id="f9604-109">Next: [Step 9. Disconnect the Property Page](step-9--disconnect-the-property-page.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9604-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f9604-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9604-111">Création d’une page de propriétés de filtre</span><span class="sxs-lookup"><span data-stu-id="f9604-111">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



