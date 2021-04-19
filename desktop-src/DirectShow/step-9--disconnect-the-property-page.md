---
description: Étape 9.
ms.assetid: 3e476422-ab76-4a2b-af9b-d9d065d79e5b
title: Étape 9. Déconnecter la page de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d59c620179e95afa3f1b949ed40cbfc3a2bca11a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520689"
---
# <a name="step-9-disconnect-the-property-page"></a><span data-ttu-id="b1a55-104">Étape 9.</span><span class="sxs-lookup"><span data-stu-id="b1a55-104">Step 9.</span></span> <span data-ttu-id="b1a55-105">Déconnecter la page de propriétés</span><span class="sxs-lookup"><span data-stu-id="b1a55-105">Disconnect the Property Page</span></span>

<span data-ttu-id="b1a55-106">Substituez la méthode [**CBasePropertyPage :: OnDisconnect**](cbasepropertypage-ondisconnect.md) pour libérer toutes les interfaces obtenues dans la méthode **OnConnect** .</span><span class="sxs-lookup"><span data-stu-id="b1a55-106">Override the [**CBasePropertyPage::OnDisconnect**](cbasepropertypage-ondisconnect.md) method to release any interfaces that you obtained in the **OnConnect** method.</span></span> <span data-ttu-id="b1a55-107">En outre, si l’utilisateur ignore la feuille de propriétés sans valider les modifications, vous devez restaurer les valeurs d’origine si elles ont été modifiées.</span><span class="sxs-lookup"><span data-stu-id="b1a55-107">Also, if the user dismisses the property sheet without committing the changes, you should restore the original values if they have changed.</span></span> <span data-ttu-id="b1a55-108">Il n’existe aucune méthode « OnCancel » appelée lorsque l’utilisateur annule. vous devez donc effectuer le suivi du fait que l’utilisateur a appelé **OnApplyChanges**.</span><span class="sxs-lookup"><span data-stu-id="b1a55-108">There is no "OnCancel" method that gets called when the user cancels, so you need to keep track of whether the user has called **OnApplyChanges**.</span></span> <span data-ttu-id="b1a55-109">Cet exemple utilise la \_ variable m lVal, décrite précédemment :</span><span class="sxs-lookup"><span data-stu-id="b1a55-109">This example uses the m\_lVal variable, described earlier:</span></span>


```C++
HRESULT CGrayProp::OnDisconnect(void)
{
    if (m_pGray)
    {
        // If the user clicked OK, m_lVal holds the new value.
        // Otherwise, if the user clicked Cancel, m_lVal is the old value.
        m_pGray->SetSaturation(m_lVal);  
        m_pGray->Release();
        m_pGray = NULL;
    }
    return S_OK;
}
```



<span data-ttu-id="b1a55-110">Ensuite : [étape 10. Prise en charge de l’inscription COM](step-10--support-com-registration.md)</span><span class="sxs-lookup"><span data-stu-id="b1a55-110">Next: [Step 10. Support COM Registration](step-10--support-com-registration.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="b1a55-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b1a55-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1a55-112">Création d’une page de propriétés de filtre</span><span class="sxs-lookup"><span data-stu-id="b1a55-112">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



