---
title: Ajout et modification des événements
description: Ajout et modification des événements
ms.assetid: 342b0592-67b7-4c13-bee8-48ac322d3d27
keywords:
- Plug-ins du lecteur Windows Media, pages de propriétés de l’exemple Echo
- plug-ins, pages de propriétés d’exemple Echo
- plug-ins de traitement de signal numérique, pages de propriétés d’exemple Echo
- Plug-ins DSP, pages de propriétés d’exemple Echo
- Exemple de plug-in DSP Echo, pages de propriétés
- Exemple de plug-in DSP Echo, événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77c8e069c20dc2c953998b9e5c2a47f509166ca3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310606"
---
# <a name="adding-and-modifying-the-events"></a><span data-ttu-id="8cbf9-109">Ajout et modification des événements</span><span class="sxs-lookup"><span data-stu-id="8cbf9-109">Adding and Modifying the Events</span></span>

<span data-ttu-id="8cbf9-110">Vous devez fournir des gestionnaires d’événements pour les \_ événements en modification qui se produisent lorsque l’utilisateur modifie le texte dans les zones d’édition de la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="8cbf9-110">You need to supply event handlers for the EN\_CHANGE events that occur when the user changes the text in the property page edit boxes.</span></span> <span data-ttu-id="8cbf9-111">Ces gestionnaires d’événements ont une implémentation simple qui active simplement **apply** dans la boîte de dialogue page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="8cbf9-111">These event handlers have a simple implementation that merely enables **Apply** in the property page dialog box.</span></span>

## <a name="modifying-the-scale-factor-event-handler"></a><span data-ttu-id="8cbf9-112">Modification du gestionnaire d’événements de facteur d’échelle</span><span class="sxs-lookup"><span data-stu-id="8cbf9-112">Modifying the Scale Factor Event Handler</span></span>

<span data-ttu-id="8cbf9-113">Vous devez modifier le nom du gestionnaire d’événements existant fourni par l’Assistant de plug-in pour la zone d’édition facteur d’échelle.</span><span class="sxs-lookup"><span data-stu-id="8cbf9-113">You need to change the name of the existing event handler that the plug-in wizard provided for the scale factor edit box.</span></span> <span data-ttu-id="8cbf9-114">Vous devez remplacer le nom OnChangeScale par OnChangeDelay dans trois emplacements :</span><span class="sxs-lookup"><span data-stu-id="8cbf9-114">You should change the name from OnChangeScale to OnChangeDelay in three locations:</span></span>

1.  <span data-ttu-id="8cbf9-115">Dans EchoPropPage. h, modifiez le nom dans la section macro de la table des messages.</span><span class="sxs-lookup"><span data-stu-id="8cbf9-115">In EchoPropPage.h, change the name in the message map macro section.</span></span> <span data-ttu-id="8cbf9-116">Remplacez la ligne qui mappe l’événement de modification du facteur d’échelle à la méthode OnChangeScale par le code suivant :</span><span class="sxs-lookup"><span data-stu-id="8cbf9-116">Replace the line that maps the scale factor change event to the OnChangeScale method with the following code:</span></span>
    ```C++
    COMMAND_HANDLER(IDC_DELAYTIME, EN_CHANGE, OnChangeDelay)
    
    ```

    

2.  <span data-ttu-id="8cbf9-117">Dans EchoPropPage. h, modifiez le nom de la ligne qui prototype la fonction OnChangeScale :</span><span class="sxs-lookup"><span data-stu-id="8cbf9-117">In EchoPropPage.h, change the name in the line that prototypes the OnChangeScale function:</span></span>
    ```C++
    LRESULT (OnChangeDelay)(WORD wNotifyCode, WORD wID, HWND hWndCtl, BOOL& bHandled);
    
    ```

    

3.  <span data-ttu-id="8cbf9-118">Dans EchoPropPage. cpp, modifiez le nom dans l’en-tête de fonction :</span><span class="sxs-lookup"><span data-stu-id="8cbf9-118">In EchoPropPage.cpp, change the name in the function header:</span></span>
    ```C++
    LRESULT CEchoPropPage::OnChangeDelay(WORD wNotifyCode, WORD wID, HWND hWndCtl, BOOL& bHandled)
    
    ```

    

## <a name="adding-the-wet-mix-event-handler"></a><span data-ttu-id="8cbf9-119">Ajout du gestionnaire d’événements de mélange mouillé</span><span class="sxs-lookup"><span data-stu-id="8cbf9-119">Adding the Wet Mix Event Handler</span></span>

<span data-ttu-id="8cbf9-120">Vous pouvez facilement ajouter le gestionnaire d’événements pour l' \_ événement en modification attaché au \_ contrôle de zone d’édition WETMIX d’IDC.</span><span class="sxs-lookup"><span data-stu-id="8cbf9-120">You can easily add the event handler for the EN\_CHANGE event that is attached to the IDC\_WETMIX edit box control.</span></span> <span data-ttu-id="8cbf9-121">Dans l’éditeur de ressources de boîte de dialogue :</span><span class="sxs-lookup"><span data-stu-id="8cbf9-121">From the dialog resource editor:</span></span>

1.  <span data-ttu-id="8cbf9-122">Cliquez avec le bouton droit sur la \_ zone d’édition IDC WETMIX et choisissez **événements**.</span><span class="sxs-lookup"><span data-stu-id="8cbf9-122">Right-click the IDC\_WETMIX edit box and choose **Events**.</span></span> <span data-ttu-id="8cbf9-123">La boîte de dialogue nouveaux messages et gestionnaires d’événements Windows s’affiche.</span><span class="sxs-lookup"><span data-stu-id="8cbf9-123">The New Windows Message and Event Handlers dialog box appears.</span></span>
2.  <span data-ttu-id="8cbf9-124">Dans la zone **classe ou objet à gérer** , cliquez sur le nom de la ressource de zone d’édition, IDC \_ WETMIX.</span><span class="sxs-lookup"><span data-stu-id="8cbf9-124">In the **Class or object to handle** box, click the name of the edit box resource, IDC\_WETMIX.</span></span>
3.  <span data-ttu-id="8cbf9-125">Dans la zone **nouveaux messages/événements Windows** , cliquez sur \_ Modifier pour le sélectionner.</span><span class="sxs-lookup"><span data-stu-id="8cbf9-125">In the **New Windows messages/events** box, click EN\_CHANGE to select it.</span></span>
4.  <span data-ttu-id="8cbf9-126">Cliquez sur **Ajouter un gestionnaire**.</span><span class="sxs-lookup"><span data-stu-id="8cbf9-126">Click **Add Handler**.</span></span> <span data-ttu-id="8cbf9-127">La boîte de dialogue Ajouter une fonction membre s’affiche.</span><span class="sxs-lookup"><span data-stu-id="8cbf9-127">The Add Member Function dialog box appears.</span></span>
5.  <span data-ttu-id="8cbf9-128">Dans la zone nom de la **fonction membre** , tapez le nom OnChangeWetmix.</span><span class="sxs-lookup"><span data-stu-id="8cbf9-128">In the **Member function name** box, type the name OnChangeWetmix.</span></span>
6.  <span data-ttu-id="8cbf9-129">Cliquez sur **OK** pour fermer la boîte de dialogue Ajouter une fonction membre.</span><span class="sxs-lookup"><span data-stu-id="8cbf9-129">Click **OK** to close the Add Member Function dialog box.</span></span>
7.  <span data-ttu-id="8cbf9-130">Cliquez sur **OK** pour revenir à l’éditeur de ressources de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="8cbf9-130">Click **OK** to return to the dialog box resource editor.</span></span>

<span data-ttu-id="8cbf9-131">Visual C++ ajoute automatiquement le code pour la table des messages et pour la fonction de gestionnaire d’événements à EchoPropPage. h.</span><span class="sxs-lookup"><span data-stu-id="8cbf9-131">Visual C++ automatically adds the code for the message map and for the event handler function to EchoPropPage.h.</span></span> <span data-ttu-id="8cbf9-132">Le code qu’il insère fournit un commentaire TODO dans lequel vous pouvez ajouter l’implémentation dans l’en-tête pour la fonction.</span><span class="sxs-lookup"><span data-stu-id="8cbf9-132">The code it inserts provides a TODO comment where you can add the implementation in the header for the function.</span></span> <span data-ttu-id="8cbf9-133">Il s’agit d’un style légèrement différent de celui utilisé par l’exemple de code du plug-in du lecteur Windows Media, mais il est acceptable.</span><span class="sxs-lookup"><span data-stu-id="8cbf9-133">This is a slightly different style than the Windows Media Player Plug-in Wizard sample code uses, but is acceptable.</span></span>

<span data-ttu-id="8cbf9-134">Que vous souhaitiez écrire votre implémentation dans le fichier d’en-tête ou la déplacer vers EchoPropPage. cpp vous convient.</span><span class="sxs-lookup"><span data-stu-id="8cbf9-134">Whether you want to write your implementation in the header file or move it to EchoPropPage.cpp is up to you.</span></span> <span data-ttu-id="8cbf9-135">Dans les deux cas, l’implémentation a besoin d’une seule ligne de code supplémentaire pour activer l' **application** dans la boîte de dialogue de la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="8cbf9-135">In either case, the implementation needs only a single additional line of code to enable **Apply** in the property page dialog.</span></span> <span data-ttu-id="8cbf9-136">Insérez cette ligne de code avant la ligne qui retourne à partir de la fonction :</span><span class="sxs-lookup"><span data-stu-id="8cbf9-136">Insert this line of code before the line that returns from the function:</span></span>


```C++
SetDirty(TRUE);  // Enable Apply.

```



## <a name="related-topics"></a><span data-ttu-id="8cbf9-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8cbf9-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8cbf9-138">**Modification de la page de propriétés de l’exemple Echo**</span><span class="sxs-lookup"><span data-stu-id="8cbf9-138">**Modifying the Echo Sample Property Page**</span></span>](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




