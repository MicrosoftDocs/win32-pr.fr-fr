---
title: Implémentation de CEchoPropPage Apply
description: Implémentation de CEchoPropPage Apply
ms.assetid: e887b851-e623-4ec4-8d8b-165e4b21e116
keywords:
- Plug-ins du lecteur Windows Media, pages de propriétés de l’exemple Echo
- plug-ins, pages de propriétés d’exemple Echo
- plug-ins de traitement de signal numérique, pages de propriétés d’exemple Echo
- Plug-ins DSP, pages de propriétés d’exemple Echo
- Exemple de plug-in DSP Echo, pages de propriétés
- Echo DSP, exemple de plug-in, méthode Apply CEchoPropPage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bdca8a771d3e3e26923567f25bf7d19e968595e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840198"
---
# <a name="implementing-cechoproppageapply"></a><span data-ttu-id="f09e5-109">Implémentation de CEchoPropPage :: apply</span><span class="sxs-lookup"><span data-stu-id="f09e5-109">Implementing CEchoPropPage::Apply</span></span>

<span data-ttu-id="f09e5-110">La méthode CEchoPropPage :: apply est implémentée dans EchoPropPage. cpp.</span><span class="sxs-lookup"><span data-stu-id="f09e5-110">The CEchoPropPage::Apply method is implemented in EchoPropPage.cpp.</span></span> <span data-ttu-id="f09e5-111">Elle s’exécute lorsque l’utilisateur clique sur **appliquer** dans la boîte de dialogue page de propriétés du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f09e5-111">It executes when the user clicks **Apply** in the property page dialog box in Windows Media Player.</span></span> <span data-ttu-id="f09e5-112">L’exemple de code de l’Assistant de plug-in fournit une implémentation pour gérer une seule propriété.</span><span class="sxs-lookup"><span data-stu-id="f09e5-112">The plug-in wizard sample code provides an implementation to handle a single property.</span></span> <span data-ttu-id="f09e5-113">Vous pouvez modifier ce code pour l’un des exemples de propriétés Echo, puis ajouter du code pour stocker l’autre valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="f09e5-113">You can modify this code for one of the Echo sample properties, and then add code to store the other property value.</span></span>

## <a name="declaring-the-apply-method-variables"></a><span data-ttu-id="f09e5-114">Déclaration des variables de méthode Apply</span><span class="sxs-lookup"><span data-stu-id="f09e5-114">Declaring the Apply Method Variables</span></span>

<span data-ttu-id="f09e5-115">Tout d’abord, vous devez supprimer la déclaration de fScaleFactor.</span><span class="sxs-lookup"><span data-stu-id="f09e5-115">First, you must remove the declaration of fScaleFactor.</span></span> <span data-ttu-id="f09e5-116">Ensuite, ajoutez les déclarations de variables dont vous aurez besoin.</span><span class="sxs-lookup"><span data-stu-id="f09e5-116">Then, add variable declarations that you will need.</span></span> <span data-ttu-id="f09e5-117">L’exemple suivant montre les déclarations de variables terminées :</span><span class="sxs-lookup"><span data-stu-id="f09e5-117">The following example shows the completed variable declarations:</span></span>


```
TCHAR   szStr[MAXSTRING] = { 0 };
DWORD   dwDelayTime = 1000;  // Initialize the delay time.
DWORD   dwWetmix = 50;       // Initialize a DWORD for effect level.
double  fWetmix = 0.50;      // Initialize a double for effect level.
```



## <a name="retrieving-the-values-from-the-property-page"></a><span data-ttu-id="f09e5-118">Récupération des valeurs à partir de la page de propriétés</span><span class="sxs-lookup"><span data-stu-id="f09e5-118">Retrieving the Values from the Property Page</span></span>

<span data-ttu-id="f09e5-119">Vous devez implémenter le code pour récupérer et valider les entrées utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f09e5-119">You must implement code to retrieve and validate the user input.</span></span> <span data-ttu-id="f09e5-120">L’exemple de code suivant récupère la valeur de temps de délai dans la \_ zone d’édition IDC DELAYTIME, puis vérifie que la valeur est comprise dans une plage spécifiée :</span><span class="sxs-lookup"><span data-stu-id="f09e5-120">The following code example retrieves the delay time value from the IDC\_DELAYTIME edit box, and then verifies that the value is within a specified range:</span></span>


```
// Get the delay time value from the dialog box.
GetDlgItemText(IDC_DELAYTIME, szStr, sizeof(szStr) / sizeof(szStr[0]));

dwDelayTime = atoi(szStr);

// Make sure delay time is valid.
if ((dwDelayTime < 10) || (dwDelayTime > 2000))
{
    if (::LoadString(_Module.GetResourceInstance(), IDS_DELAYRANGEERROR, szStr, sizeof(szStr) / sizeof(szStr[0])))
    {
        MessageBox(szStr);
    }

    return E_FAIL;
}
```



<span data-ttu-id="f09e5-121">Si l’entrée utilisateur n’est pas dans la plage spécifiée, le code affiche une boîte de message.</span><span class="sxs-lookup"><span data-stu-id="f09e5-121">If the user input is not in the specified range, the code displays a message box.</span></span> <span data-ttu-id="f09e5-122">Notez l’utilisation de la ressource de type chaîne que vous avez créée précédemment pour le message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="f09e5-122">Notice the use of the string resource you created earlier for the error message.</span></span>

<span data-ttu-id="f09e5-123">L’exemple suivant récupère le niveau d’effet à partir de la \_ zone d’édition IDC WETMIX, puis vérifie que la valeur est comprise dans une plage spécifiée :</span><span class="sxs-lookup"><span data-stu-id="f09e5-123">The following example retrieves the effect level from the IDC\_WETMIX edit box and then verifies that the value is within a specified range:</span></span>


```
// Get the effects level value from the dialog box.
GetDlgItemText(IDC_WETMIX, szStr, sizeof(szStr) / sizeof(szStr[0]));

dwWetmix = atoi(szStr);

// Make sure wet mix value is valid.
if ((dwWetmix < 0) || (dwWetmix > 100))
{
    if (::LoadString(_Module.GetResourceInstance(), IDS_MIXRANGEERROR, szStr, sizeof(szStr) / sizeof(szStr[0])))
    {
        MessageBox(szStr);
    }

    return E_FAIL;
}
```



## <a name="storing-the-property-values-in-the-registry"></a><span data-ttu-id="f09e5-124">Stockage des valeurs de propriété dans le registre</span><span class="sxs-lookup"><span data-stu-id="f09e5-124">Storing the Property Values in the Registry</span></span>

<span data-ttu-id="f09e5-125">Ensuite, votre code doit conserver les nouvelles valeurs de propriété dans le registre.</span><span class="sxs-lookup"><span data-stu-id="f09e5-125">Next, your code must persist the new property values to the registry.</span></span> <span data-ttu-id="f09e5-126">Le code suivant stocke les deux valeurs de propriété :</span><span class="sxs-lookup"><span data-stu-id="f09e5-126">The following code stores both property values:</span></span>


```
// update the registry
CRegKey key;
LONG    lResult;

// Write the delay time value to the registry.
lResult = key.Create(HKEY_CURRENT_USER, kszPrefsRegKey);
if (ERROR_SUCCESS == lResult)
{
    lResult = key.SetValue( dwDelayTime , kszPrefsDelayTime );
}

// Write the wet mix value to the registry.
lResult = key.Create(HKEY_CURRENT_USER, kszPrefsRegKey);
if (ERROR_SUCCESS == lResult)
{
    lResult = key.SetValue( dwWetmix , kszPrefsWetmix );
}
```



## <a name="updating-the-echo-plug-in-property-values"></a><span data-ttu-id="f09e5-127">Mise à jour des valeurs de propriété du plug-in Echo</span><span class="sxs-lookup"><span data-stu-id="f09e5-127">Updating the Echo Plug-in Property Values</span></span>

<span data-ttu-id="f09e5-128">La méthode **apply** doit informer le plug-in ECHO que les valeurs des propriétés ont changé.</span><span class="sxs-lookup"><span data-stu-id="f09e5-128">The **Apply** method must inform the Echo plug-in that the property values have changed.</span></span> <span data-ttu-id="f09e5-129">Le code suivant appelle la méthode put de propriété pour chaque propriété à l’aide du pointeur d’interface récupéré dans CEchoPropPage :: SetObjects :</span><span class="sxs-lookup"><span data-stu-id="f09e5-129">The following code calls the property put method for each property using the interface pointer retrieved in CEchoPropPage::SetObjects:</span></span>


```
// update the plug-in
if (m_spEcho)
{
    m_spEcho->put_delay(dwDelayTime);

    // Convert the wet mix value from DWORD to double.
    fWetmix = (double)dwWetmix / 100;
    m_spEcho->put_wetmix(fWetmix);
}
```



<span data-ttu-id="f09e5-130">Notez que la valeur de la combinaison humide est convertie en virgule flottante avant d’être transmise au plug-in.</span><span class="sxs-lookup"><span data-stu-id="f09e5-130">Notice that the wet mix value is converted to floating point before being passed to the plug-in.</span></span>

## <a name="disabling-the-apply-button"></a><span data-ttu-id="f09e5-131">Désactivation du bouton appliquer</span><span class="sxs-lookup"><span data-stu-id="f09e5-131">Disabling the Apply Button</span></span>

<span data-ttu-id="f09e5-132">En guise de dernière étape, votre code doit désactiver l’application dans la boîte de dialogue page de propriétés en tant que signal à l’utilisateur que les valeurs ont été correctement mises à jour.</span><span class="sxs-lookup"><span data-stu-id="f09e5-132">As a final step, your code should disable Apply in the property page dialog box as a signal to the user that the values have been successfully updated.</span></span> <span data-ttu-id="f09e5-133">Pour cela, vous devez disposer de la seule ligne de code suivante :</span><span class="sxs-lookup"><span data-stu-id="f09e5-133">This requires the following single line of code:</span></span>


```
m_bDirty = FALSE; // Tell the property page to disable Apply.
```



## <a name="related-topics"></a><span data-ttu-id="f09e5-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f09e5-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f09e5-135">**Modification de la page de propriétés de l’exemple Echo**</span><span class="sxs-lookup"><span data-stu-id="f09e5-135">**Modifying the Echo Sample Property Page**</span></span>](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




