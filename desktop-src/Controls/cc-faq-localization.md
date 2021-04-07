---
title: Prise en charge de la localisation des contrôles communs
description: Cette rubrique décrit la prise en charge des langues nationales intégrées aux contrôles communs.
ms.assetid: c5720198-9071-4213-8dad-50b4c015c5f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70ccc307defa687c8640425dd781660641fe78a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939757"
---
# <a name="localization-support-for-common-controls"></a><span data-ttu-id="0c61b-103">Prise en charge de la localisation des contrôles communs</span><span class="sxs-lookup"><span data-stu-id="0c61b-103">Localization Support for Common Controls</span></span>

<span data-ttu-id="0c61b-104">Cette rubrique décrit la prise en charge des langues nationales intégrées aux contrôles communs.</span><span class="sxs-lookup"><span data-stu-id="0c61b-104">This topic describes the support for national languages that is built into the common controls.</span></span> <span data-ttu-id="0c61b-105">La prise en charge intégrée du langage national simplifie l’implémentation des applications localisées.</span><span class="sxs-lookup"><span data-stu-id="0c61b-105">The built-in national language support simplifies the implementation of localized applications.</span></span>

<span data-ttu-id="0c61b-106">Cette rubrique contient les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="0c61b-106">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="0c61b-107">Spécification d’une langue pour les contrôles communs</span><span class="sxs-lookup"><span data-stu-id="0c61b-107">Specifying a Language for the Common Controls</span></span>](#specifying-a-language-for-the-common-controls)
-   [<span data-ttu-id="0c61b-108">Spécification d’une langue pour les contrôles dans une boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="0c61b-108">Specifying a Language for Controls in a Dialog Box</span></span>](#specifying-a-language-for-controls-in-a-dialog-box)
-   [<span data-ttu-id="0c61b-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0c61b-109">Related topics</span></span>](#related-topics)

## <a name="specifying-a-language-for-the-common-controls"></a><span data-ttu-id="0c61b-110">Spécification d’une langue pour les contrôles communs</span><span class="sxs-lookup"><span data-stu-id="0c61b-110">Specifying a Language for the Common Controls</span></span>

<span data-ttu-id="0c61b-111">Si vous souhaitez spécifier une langue pour les contrôles communs qui est différente de la langue du système, appelez [**InitMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-initmuilanguage).</span><span class="sxs-lookup"><span data-stu-id="0c61b-111">If you want to specify a language for the common controls that is different than the system language, call [**InitMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-initmuilanguage).</span></span> <span data-ttu-id="0c61b-112">Le langage spécifié par cette fonction s’applique uniquement au processus à partir duquel la fonction est appelée.</span><span class="sxs-lookup"><span data-stu-id="0c61b-112">The language specified by this function applies only to the process from which the function is called.</span></span>

<span data-ttu-id="0c61b-113">Pour déterminer la langue actuellement utilisée par les contrôles communs, appelez [**GetMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-getmuilanguage).</span><span class="sxs-lookup"><span data-stu-id="0c61b-113">To determine the language currently being used by the common controls, call [**GetMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-getmuilanguage).</span></span> <span data-ttu-id="0c61b-114">Elle retourne la valeur qui a été définie par un appel précédent à [**InitMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-initmuilanguage).</span><span class="sxs-lookup"><span data-stu-id="0c61b-114">It returns the value that was set by a previous call to [**InitMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-initmuilanguage).</span></span> <span data-ttu-id="0c61b-115">Le langage retourné est celui qui a été spécifié pour le processus à partir duquel il est appelé.</span><span class="sxs-lookup"><span data-stu-id="0c61b-115">The language returned is the one that was specified for the process it is called from.</span></span> <span data-ttu-id="0c61b-116">Si **InitMUILanguage** n’a pas été appelé ou a été appelé à partir d’un autre processus, **GetMUILanguage** retourne une valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="0c61b-116">If **InitMUILanguage** has not been called, or was called from another process, **GetMUILanguage** will return a default value.</span></span>

## <a name="specifying-a-language-for-controls-in-a-dialog-box"></a><span data-ttu-id="0c61b-117">Spécification d’une langue pour les contrôles dans une boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="0c61b-117">Specifying a Language for Controls in a Dialog Box</span></span>

<span data-ttu-id="0c61b-118">Contrairement aux contrôles communs, les contrôles prédéfinis, tels que les boutons ou les zones d’édition, n’utilisent pas la langue actuelle du système par défaut.</span><span class="sxs-lookup"><span data-stu-id="0c61b-118">Unlike common controls, predefined controls such as buttons or edit boxes do not use the current system language by default.</span></span> <span data-ttu-id="0c61b-119">Le contrôle de police natif est un contrôle invisible qui fonctionne en arrière-plan pour permettre aux contrôles prédéfinis d’une boîte de dialogue d’afficher la langue actuelle du système.</span><span class="sxs-lookup"><span data-stu-id="0c61b-119">The native font control is an invisible control that works in the background to allow a dialog box's predefined controls to display the current system language.</span></span>

<span data-ttu-id="0c61b-120">Pour utiliser le contrôle de police natif, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="0c61b-120">To use the native font control, follow this procedure.</span></span>

1.  <span data-ttu-id="0c61b-121">Initialisez le contrôle de police natif en appelant [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex).</span><span class="sxs-lookup"><span data-stu-id="0c61b-121">Initialize the native font control by calling [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex).</span></span> <span data-ttu-id="0c61b-122">Définissez le membre **dwICC** de la structure [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) désignée par *lpInitCtrls* à la \_ classe ICC NATIVEFNTCTL \_ .</span><span class="sxs-lookup"><span data-stu-id="0c61b-122">Set the **dwICC** member of the [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure pointed to by *lpInitCtrls* to ICC\_NATIVEFNTCTL\_CLASS.</span></span>
2.  <span data-ttu-id="0c61b-123">Ajoutez le contrôle au script de ressources pour la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="0c61b-123">Add the control to the resource script for the dialog box.</span></span> <span data-ttu-id="0c61b-124">Définissez un ou plusieurs des indicateurs de style suivants pour spécifier les contrôles qui seront affectés.</span><span class="sxs-lookup"><span data-stu-id="0c61b-124">Set one or more of the following style flags to specify which controls will be affected.</span></span> 

    | <span data-ttu-id="0c61b-125">Indicateur</span><span class="sxs-lookup"><span data-stu-id="0c61b-125">Flag</span></span>              | <span data-ttu-id="0c61b-126">S’applique à</span><span class="sxs-lookup"><span data-stu-id="0c61b-126">Applies to</span></span>                                                                                                                                                                                                                                                       |
    |-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="0c61b-127">\_modification NFS</span><span class="sxs-lookup"><span data-stu-id="0c61b-127">NFS\_EDIT</span></span>         | <span data-ttu-id="0c61b-128">Contrôles d’édition</span><span class="sxs-lookup"><span data-stu-id="0c61b-128">Edit controls</span></span>                                                                                                                                                                                                                                                    |
    | <span data-ttu-id="0c61b-129">NFS \_ statique</span><span class="sxs-lookup"><span data-stu-id="0c61b-129">NFS\_STATIC</span></span>       | <span data-ttu-id="0c61b-130">Contrôles statiques</span><span class="sxs-lookup"><span data-stu-id="0c61b-130">Static controls</span></span>                                                                                                                                                                                                                                                  |
    | <span data-ttu-id="0c61b-131">\_LISTCOMBO NFS</span><span class="sxs-lookup"><span data-stu-id="0c61b-131">NFS\_LISTCOMBO</span></span>    | <span data-ttu-id="0c61b-132">Contrôles List, ComboBox, List-View et ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="0c61b-132">List, ComboBox, List-View, and ComboBoxEx controls</span></span>                                                                                                                                                                                                               |
    | <span data-ttu-id="0c61b-133">\_bouton NFS</span><span class="sxs-lookup"><span data-stu-id="0c61b-133">NFS\_BUTTON</span></span>       | <span data-ttu-id="0c61b-134">Contrôles boutons</span><span class="sxs-lookup"><span data-stu-id="0c61b-134">Button controls</span></span>                                                                                                                                                                                                                                                  |
    | <span data-ttu-id="0c61b-135">\_tout NFS</span><span class="sxs-lookup"><span data-stu-id="0c61b-135">NFS\_ALL</span></span>          | <span data-ttu-id="0c61b-136">Tous les contrôles</span><span class="sxs-lookup"><span data-stu-id="0c61b-136">All controls</span></span>                                                                                                                                                                                                                                                     |
    | <span data-ttu-id="0c61b-137">\_USEFONTASSOC NFS</span><span class="sxs-lookup"><span data-stu-id="0c61b-137">NFS\_USEFONTASSOC</span></span> | <span data-ttu-id="0c61b-138">Plateforme d’Extrême-Orient.</span><span class="sxs-lookup"><span data-stu-id="0c61b-138">East Asian platform.</span></span> <span data-ttu-id="0c61b-139">Le contrôle utilise la fonctionnalité d’association de polices au lieu de basculer vers la police native.</span><span class="sxs-lookup"><span data-stu-id="0c61b-139">The control uses the font association feature instead of switching to the native font.</span></span> <span data-ttu-id="0c61b-140">Toutes les autres plateformes l’ignorent.</span><span class="sxs-lookup"><span data-stu-id="0c61b-140">All other platforms ignore it.</span></span> <span data-ttu-id="0c61b-141">Cela est déconseillé pour Windows Vista et n’est pas pris en charge dans COMCTL V6.</span><span class="sxs-lookup"><span data-stu-id="0c61b-141">This is deprecated for Windows Vista, and is not supported in comctl v6.</span></span> <span data-ttu-id="0c61b-142">Cela existe dans COMCTL V5 pour des raisons d’héritage.</span><span class="sxs-lookup"><span data-stu-id="0c61b-142">This exists in comctl v5 for legacy reasons.</span></span> |

    

     

<span data-ttu-id="0c61b-143">L’exemple suivant montre comment ajouter un contrôle de police natif à un script de ressources.</span><span class="sxs-lookup"><span data-stu-id="0c61b-143">The following example illustrates how to add a native font control to a resource script.</span></span> <span data-ttu-id="0c61b-144">Les contrôles Edit, List et zone de liste modifiable de la boîte de dialogue affichent le texte à l’aide de la langue système actuelle.</span><span class="sxs-lookup"><span data-stu-id="0c61b-144">It causes the dialog box's edit, list, and combo box controls to display text using the current system language.</span></span>


```
CONTROL    "",-1,"NativeFontCtl",NFS_EDIT|NFS_LISTCOMBO,0,0,0,0
```



## <a name="related-topics"></a><span data-ttu-id="0c61b-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0c61b-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c61b-146">À propos des contrôles communs</span><span class="sxs-lookup"><span data-stu-id="0c61b-146">About Common Controls</span></span>](common-controls-intro.md)
</dt> </dl>

 

 




