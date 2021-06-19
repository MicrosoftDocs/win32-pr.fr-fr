---
description: Implémentez une page de propriétés dans le cadre de la création d’une page de propriétés de filtre pour un filtre DirectShow personnalisé.
ms.assetid: ed71f26b-0812-4be8-96a4-b9f5dde45540
title: Étape 4. Créer la page de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d32cd9eacc98af5f273897a3837390ab5cc75f7a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406852"
---
# <a name="step-4-create-the-property-page"></a><span data-ttu-id="2b797-104">Étape 4.</span><span class="sxs-lookup"><span data-stu-id="2b797-104">Step 4.</span></span> <span data-ttu-id="2b797-105">Créer la page de propriétés</span><span class="sxs-lookup"><span data-stu-id="2b797-105">Create the Property Page</span></span>

<span data-ttu-id="2b797-106">À ce stade, le filtre prend en charge tout ce dont il a besoin pour une page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="2b797-106">At this point the filter supports everything that it needs for a property page.</span></span> <span data-ttu-id="2b797-107">L’étape suivante consiste à implémenter la page de propriétés proprement dite.</span><span class="sxs-lookup"><span data-stu-id="2b797-107">The next step is implementing the property page itself.</span></span> <span data-ttu-id="2b797-108">Commencez par dériver une nouvelle classe de **CBasePropertyPage**.</span><span class="sxs-lookup"><span data-stu-id="2b797-108">Start by deriving a new class from **CBasePropertyPage**.</span></span> <span data-ttu-id="2b797-109">L’exemple suivant montre une partie de la déclaration, y compris certaines variables de membre privé qui seront utilisées ultérieurement dans l’exemple :</span><span class="sxs-lookup"><span data-stu-id="2b797-109">The following example shows part of the declaration, including some private member variables that will be used later in the example:</span></span>


```C++
class CGrayProp : public CBasePropertyPage
{
private:
    ISaturation *m_pGray;    // Pointer to the filter's custom interface.
    long        m_lVal       // Store the old value, so we can revert.
    long        m_lNewVal;   // New value.
public:
    /* ... */
};
```



<span data-ttu-id="2b797-110">Ensuite, créez une ressource de boîte de dialogue dans l’éditeur de ressources, ainsi qu’une ressource de type chaîne pour le titre de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="2b797-110">Next, create a dialog resource in the resource editor, along with a string resource for the dialog title.</span></span> <span data-ttu-id="2b797-111">La chaîne s’affiche dans l’onglet de la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="2b797-111">The string will appear in the tab for the property page.</span></span> <span data-ttu-id="2b797-112">Les deux ID de ressource sont des arguments du constructeur **CBasePropertyPage** :</span><span class="sxs-lookup"><span data-stu-id="2b797-112">The two resource IDs are arguments to the **CBasePropertyPage** constructor:</span></span>


```C++
CGrayProp::CGrayProp(IUnknown *pUnk) : 
  CBasePropertyPage(NAME("GrayProp"), pUnk, IDD_PROPPAGE, IDS_PROPPAGE_TITLE),
  m_pGray(0)
{ }
```



<span data-ttu-id="2b797-113">L’illustration suivante montre la ressource de boîte de dialogue pour la page de propriétés exemple.</span><span class="sxs-lookup"><span data-stu-id="2b797-113">The following illustration shows the dialog resource for the example property page.</span></span>

![boîte de dialogue page de propriétés](images/proppage.png)

<span data-ttu-id="2b797-115">Vous êtes maintenant prêt à implémenter la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="2b797-115">Now you are ready to implement the property page.</span></span> <span data-ttu-id="2b797-116">Voici les méthodes de **CBasePropertyPage** à remplacer :</span><span class="sxs-lookup"><span data-stu-id="2b797-116">Here are the methods in **CBasePropertyPage** to override:</span></span>

-   <span data-ttu-id="2b797-117">**OnConnect** est appelé lorsque le client crée la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="2b797-117">**OnConnect** is called when the client creates the property page.</span></span> <span data-ttu-id="2b797-118">Il définit le pointeur **IUnknown** sur le filtre.</span><span class="sxs-lookup"><span data-stu-id="2b797-118">It sets the **IUnknown** pointer to the filter.</span></span>
-   <span data-ttu-id="2b797-119">**OnActivate** est appelé lors de la création de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="2b797-119">**OnActivate** is called when the dialog is created.</span></span>
-   <span data-ttu-id="2b797-120">**OnReceiveMessage** est appelé lorsque la boîte de dialogue reçoit un message de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="2b797-120">**OnReceiveMessage** is called when the dialog receives a window message.</span></span>
-   <span data-ttu-id="2b797-121">**OnApplyChanges** est appelé lorsque l’utilisateur valide les modifications apportées aux propriétés en cliquant sur le bouton **OK** ou **appliquer** .</span><span class="sxs-lookup"><span data-stu-id="2b797-121">**OnApplyChanges** is called when the user commits the property changes by clicking the **OK** or **Apply** button.</span></span>
-   <span data-ttu-id="2b797-122">**OnDisconnect** est appelé lorsque l’utilisateur ignore la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="2b797-122">**OnDisconnect** is called when the user dismisses the property sheet.</span></span>

<span data-ttu-id="2b797-123">Le reste de ce didacticiel décrit chacune de ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="2b797-123">The remainder of this tutorial describes each of these methods.</span></span>

<span data-ttu-id="2b797-124">Suivant : [étape 5. Stocke un pointeur vers le filtre](step-5--store-a-pointer-to-the-filter.md).</span><span class="sxs-lookup"><span data-stu-id="2b797-124">Next: [Step 5. Store a Pointer to the Filter](step-5--store-a-pointer-to-the-filter.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b797-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2b797-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b797-126">Création d’une page de propriétés de filtre</span><span class="sxs-lookup"><span data-stu-id="2b797-126">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



