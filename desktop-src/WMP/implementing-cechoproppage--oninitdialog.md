---
title: Implémentation de CEchoPropPage OnInitDialog
description: Implémentation de CEchoPropPage OnInitDialog
ms.assetid: 568989b0-bc07-480f-8b5c-41bbada713f8
keywords:
- Plug-ins du lecteur Windows Media, pages de propriétés de l’exemple Echo
- plug-ins, pages de propriétés d’exemple Echo
- plug-ins de traitement de signal numérique, pages de propriétés d’exemple Echo
- Plug-ins DSP, pages de propriétés d’exemple Echo
- Exemple de plug-in DSP Echo, pages de propriétés
- Echo DSP, exemple de plug-in, CEchoPropPage OnInitDialog, méthode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0874c750914b5caecf86ffa61a0c42d38bb1c02e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509374"
---
# <a name="implementing-cechoproppageoninitdialog"></a><span data-ttu-id="6fe1c-109">Implémentation de CEchoPropPage :: OnInitDialog</span><span class="sxs-lookup"><span data-stu-id="6fe1c-109">Implementing CEchoPropPage::OnInitDialog</span></span>

<span data-ttu-id="6fe1c-110">La méthode **CEchoPropPage :: OnInitDialog** est implémentée dans EchoPropPage. cpp.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-110">The **CEchoPropPage::OnInitDialog** method is implemented in EchoPropPage.cpp.</span></span> <span data-ttu-id="6fe1c-111">Elle s’exécute lorsque la boîte de dialogue page de propriétés est appelée.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-111">It executes when the property page dialog box is invoked.</span></span> <span data-ttu-id="6fe1c-112">Le code de cette méthode doit récupérer les valeurs de propriété actuelles et les afficher dans la zone d’édition appropriée.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-112">The code in this method needs to retrieve the current property values and display them in the correct edit box.</span></span> <span data-ttu-id="6fe1c-113">L’exemple de code de l’Assistant de plug-in fournit une implémentation pour une propriété unique.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-113">The plug-in wizard sample code provides an implementation for a single property.</span></span> <span data-ttu-id="6fe1c-114">Vous pouvez modifier ce code pour l’un des exemples de propriétés Echo, puis ajouter du code pour récupérer la deuxième valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-114">You can modify this code for one of the Echo sample properties, and then add code to retrieve the second property value.</span></span>

## <a name="declaring-the-oninitdialog-method-variables"></a><span data-ttu-id="6fe1c-115">Déclaration des variables de méthode OnInitDialog</span><span class="sxs-lookup"><span data-stu-id="6fe1c-115">Declaring the OnInitDialog Method Variables</span></span>

<span data-ttu-id="6fe1c-116">Tout d’abord, vous devez supprimer la déclaration de fScaleFactor et la remplacer par les déclarations de variables suivantes :</span><span class="sxs-lookup"><span data-stu-id="6fe1c-116">First, you must remove the declaration of fScaleFactor and replace it with the following variable declarations:</span></span>


```
DWORD  dwDelayTime = 1000;    // Default delay time.
DWORD  dwWetmix = 50;         // Default wet mix DWORD.
double fWetmix =  0.50;       // Default wet mix double.
```



## <a name="retrieving-the-current-values-from-the-plug-in"></a><span data-ttu-id="6fe1c-117">Récupération des valeurs actuelles du plug-in</span><span class="sxs-lookup"><span data-stu-id="6fe1c-117">Retrieving the Current Values from the Plug-in</span></span>

<span data-ttu-id="6fe1c-118">Le code doit ensuite tenter de récupérer les valeurs de propriété actuelles à partir du plug-in Echo.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-118">The code should next attempt to retrieve the current property values from the Echo plug-in.</span></span> <span data-ttu-id="6fe1c-119">L’exemple suivant tente de récupérer chaque propriété :</span><span class="sxs-lookup"><span data-stu-id="6fe1c-119">The following example attempts to retrieve each property:</span></span>


```
if (m_spEcho)
{
    m_spEcho->get_delay(&dwDelayTime);
    m_spEcho->get_wetmix(&fWetmix);
    // Convert wet mix from double to DWORD.
    dwWetmix = (DWORD)(fWetmix * 100);
}
```



<span data-ttu-id="6fe1c-120">La boîte de dialogue affiche la valeur de niveau d’effet pour l’utilisateur sous la forme d’un entier, mais le plug-in stocke la valeur sous la forme d’un nombre à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-120">The dialog box displays the effects level value to the user as an integer, but the plug-in stores the value as a floating-point number.</span></span> <span data-ttu-id="6fe1c-121">Par conséquent, le code convertit la valeur à virgule flottante en valeur **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="6fe1c-121">Therefore, the code converts the floating-point value to a **DWORD** value.</span></span>

## <a name="retrieving-the-current-values-from-the-registry"></a><span data-ttu-id="6fe1c-122">Récupération des valeurs actuelles à partir du Registre</span><span class="sxs-lookup"><span data-stu-id="6fe1c-122">Retrieving the Current Values from the Registry</span></span>

<span data-ttu-id="6fe1c-123">Si la page de propriétés ne peut pas récupérer les valeurs actuelles du plug-in, elle doit tenter de les lire à partir du Registre.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-123">If the property page cannot retrieve the current values from the plug-in, it must attempt to read them from the registry.</span></span> <span data-ttu-id="6fe1c-124">Le code suivant lit chaque valeur de propriété :</span><span class="sxs-lookup"><span data-stu-id="6fe1c-124">The following code reads each property value:</span></span>


```
else // Otherwise, read values from registry
{
    CRegKey key;
    LONG    lResult;

    lResult = key.Open(HKEY_CURRENT_USER, kszPrefsRegKey, KEY_READ);
    if (ERROR_SUCCESS == lResult)
    {
        DWORD   dwValue = 0;

        // Read the delay time.
        lResult = key.QueryValue(dwValue, kszPrefsDelayTime );
        if (ERROR_SUCCESS == lResult)
        {
            dwDelayTime = dwValue;
        }

        // Read the wet mix value.
        lResult = key.QueryValue(dwValue, kszPrefsWetmix );
        if (ERROR_SUCCESS == lResult)
        {
            dwWetmix = dwValue;
        }
    }
}
```



<span data-ttu-id="6fe1c-125">Notez l’utilisation des constantes de registre que vous avez créées précédemment.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-125">Notice the use of the registry constants you created previously.</span></span>

## <a name="displaying-the-values-to-the-user"></a><span data-ttu-id="6fe1c-126">Affichage des valeurs pour l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="6fe1c-126">Displaying the Values to the User</span></span>

<span data-ttu-id="6fe1c-127">Enfin, la page de propriétés doit afficher les valeurs dans les contrôles de zone d’édition appropriés.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-127">Finally, the property page must display the values in the correct edit box controls.</span></span> <span data-ttu-id="6fe1c-128">L’exemple de code suivant illustre ceci :</span><span class="sxs-lookup"><span data-stu-id="6fe1c-128">The following example code demonstrates this:</span></span>


```
 TCHAR   szStr[MAXSTRING];

// Display the delay time.
_stprintf_s(szStr, MAXSTRING, _T("%u"), dwDelayTime);
SetDlgItemText(IDC_DELAYTIME, szStr);

// Display the effect level.
_stprintf_s(szStr, MAXSTRING, _T("%u"), dwWetmix);
SetDlgItemText(IDC_WETMIX, szStr);
```



## <a name="related-topics"></a><span data-ttu-id="6fe1c-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6fe1c-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6fe1c-130">**Modification de la page de propriétés de l’exemple Echo**</span><span class="sxs-lookup"><span data-stu-id="6fe1c-130">**Modifying the Echo Sample Property Page**</span></span>](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




