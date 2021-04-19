---
description: Étape 7.
ms.assetid: 12bb1288-e764-4bc1-bea5-196e17cf3557
title: Étape 7. Gérer les messages de fenêtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dd1c44dd65a4f9f430b4223f0a5a0e4763af981
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521116"
---
# <a name="step-7-handle-window-messages"></a><span data-ttu-id="487cd-104">Étape 7.</span><span class="sxs-lookup"><span data-stu-id="487cd-104">Step 7.</span></span> <span data-ttu-id="487cd-105">Gérer les messages de fenêtre</span><span class="sxs-lookup"><span data-stu-id="487cd-105">Handle Window Messages</span></span>

<span data-ttu-id="487cd-106">Substituez la méthode [**CBasePropertyPage :: OnReceiveMessage**](cbasepropertypage-onreceivemessage.md) pour mettre à jour les contrôles de boîte de dialogue en réponse à l’entrée utilisateur.</span><span class="sxs-lookup"><span data-stu-id="487cd-106">Override the [**CBasePropertyPage::OnReceiveMessage**](cbasepropertypage-onreceivemessage.md) method to update the dialog controls in response to user input.</span></span> <span data-ttu-id="487cd-107">Si vous ne gérez pas un message particulier, appelez la méthode **OnReceiveMessage** sur la classe parente.</span><span class="sxs-lookup"><span data-stu-id="487cd-107">If you don't handle a particular message, call the **OnReceiveMessage** method on the parent class.</span></span> <span data-ttu-id="487cd-108">Chaque fois que l’utilisateur modifie une propriété, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="487cd-108">Whenever the user changes a property, do the following:</span></span>

-   <span data-ttu-id="487cd-109">Affectez la valeur **true** à la variable **m \_ bDirty** de la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="487cd-109">Set the **m\_bDirty** variable of the property page to **TRUE**.</span></span>
-   <span data-ttu-id="487cd-110">Appelez la méthode **IPropertyPageSite :: OnStatusChange** du frame de propriété avec l' \_ indicateur de modification PROPPAGESTATUS.</span><span class="sxs-lookup"><span data-stu-id="487cd-110">Call the **IPropertyPageSite::OnStatusChange** method of the property frame with the PROPPAGESTATUS\_DIRTY flag.</span></span> <span data-ttu-id="487cd-111">Cet indicateur informe le frame de propriété qu’il doit activer le bouton **appliquer** .</span><span class="sxs-lookup"><span data-stu-id="487cd-111">This flag informs the property frame that it should enable the **Apply** button.</span></span> <span data-ttu-id="487cd-112">Le membre [**CBasePropertyPage :: m \_ pPageSite**](cbasepropertypage-m-ppagesite.md) contient un pointeur vers l’interface **IPropertyPageSite** .</span><span class="sxs-lookup"><span data-stu-id="487cd-112">The [**CBasePropertyPage::m\_pPageSite**](cbasepropertypage-m-ppagesite.md) member holds a pointer to the **IPropertyPageSite** interface.</span></span>

<span data-ttu-id="487cd-113">Pour simplifier cette étape, vous pouvez ajouter la fonction d’assistance suivante à la page de propriétés :</span><span class="sxs-lookup"><span data-stu-id="487cd-113">To simplify this step, you can add the following helper function to your property page:</span></span>


```C++
private:
    void SetDirty()
    {
        m_bDirty = TRUE;
        if (m_pPageSite)
        {
            m_pPageSite->OnStatusChange(PROPPAGESTATUS_DIRTY);
        }
    }
```



<span data-ttu-id="487cd-114">Appelez cette méthode privée à l’intérieur de **OnReceiveMessage** chaque fois qu’une action de l’utilisateur modifie une propriété, comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="487cd-114">Call this private method inside **OnReceiveMessage** whenever a user action changes a property, as shown in the following example:</span></span>


```C++
BOOL CGrayProp::OnReceiveMessage(HWND hwnd,
    UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_COMMAND:
        if (LOWORD(wParam) == IDC_DEFAULT)
        {
            // User clicked the 'Revert to Default' button.
            m_lNewVal = SATURATION_DEFAULT;
            m_pGray->SetSaturation(m_lNewVal);

            // Update the slider control.
            SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETPOS, 1,
                m_lNewVal);
            SetDirty();
            return (LRESULT) 1;
        }
        break;

    case WM_HSCROLL:
        {
            // User moved the slider.
            switch(LOWORD(wParam))
            {
            case TB_PAGEDOWN:
            case SB_THUMBTRACK:
            case TB_PAGEUP:
                m_lNewVal = SendDlgItemMessage(m_Dlg, IDC_SLIDER1,
                    TBM_GETPOS, 0, 0);
                m_pGray->SetSaturation(m_lNewVal);
                SetDirty();
            }
            return (LRESULT) 1;
        }
    } // Switch.
    
    // Let the parent class handle the message.
    return CBasePropertyPage::OnReceiveMessage(hwnd,uMsg,wParam,lParam);
} 
```



<span data-ttu-id="487cd-115">Dans cet exemple, la page de propriétés contient deux contrôles, une barre de curseur et un bouton **rétablir les valeurs par défaut** .</span><span class="sxs-lookup"><span data-stu-id="487cd-115">The property page in this example has two controls, a slider bar and a **Revert to Default** button.</span></span> <span data-ttu-id="487cd-116">Si l’utilisateur fait défiler la barre du curseur, la page de propriétés définit la valeur de saturation sur le filtre.</span><span class="sxs-lookup"><span data-stu-id="487cd-116">If the user scrolls the slider bar, the property page sets the saturation value on the filter.</span></span> <span data-ttu-id="487cd-117">Si l’utilisateur clique sur le bouton, la page de propriétés restaure la valeur de saturation par défaut du filtre.</span><span class="sxs-lookup"><span data-stu-id="487cd-117">If the user clicks the button, the property page restores the filter's default saturation value.</span></span> <span data-ttu-id="487cd-118">Dans chaque cas, m \_ lNewVal contient la valeur actuelle et m \_ lVal contient la valeur d’origine.</span><span class="sxs-lookup"><span data-stu-id="487cd-118">In each case, m\_lNewVal holds the current value and m\_lVal holds the original value.</span></span> <span data-ttu-id="487cd-119">La valeur de m \_ lVal n’est pas mise à jour tant que l’utilisateur n’a pas validé la modification, ce qui se produit lorsque l’utilisateur clique sur le bouton **OK** ou **appliquer** du frame de propriété.</span><span class="sxs-lookup"><span data-stu-id="487cd-119">The value of m\_lVal is not updated until the user commits the change, which happens when the user clicks the **OK** or **Apply** button on the property frame.</span></span>

<span data-ttu-id="487cd-120">Étape suivante : [étape 8. Appliquer les modifications de propriété](step-8--apply-property-changes.md).</span><span class="sxs-lookup"><span data-stu-id="487cd-120">Next: [Step 8. Apply Property Changes](step-8--apply-property-changes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="487cd-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="487cd-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="487cd-122">Création d’une page de propriétés de filtre</span><span class="sxs-lookup"><span data-stu-id="487cd-122">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



