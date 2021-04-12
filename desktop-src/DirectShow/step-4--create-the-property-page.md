---
description: Étape 4.
ms.assetid: ed71f26b-0812-4be8-96a4-b9f5dde45540
title: Étape 4. Créer la page de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52e8ea1a22e30c57c66b263a62afc1e0cf801903
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104211111"
---
# <a name="step-4-create-the-property-page"></a><span data-ttu-id="a1113-104">Étape 4.</span><span class="sxs-lookup"><span data-stu-id="a1113-104">Step 4.</span></span> <span data-ttu-id="a1113-105">Créer la page de propriétés</span><span class="sxs-lookup"><span data-stu-id="a1113-105">Create the Property Page</span></span>

<span data-ttu-id="a1113-106">À ce stade, le filtre prend en charge tout ce dont il a besoin pour une page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="a1113-106">At this point the filter supports everything that it needs for a property page.</span></span> <span data-ttu-id="a1113-107">L’étape suivante consiste à implémenter la page de propriétés proprement dite.</span><span class="sxs-lookup"><span data-stu-id="a1113-107">The next step is implementing the property page itself.</span></span> <span data-ttu-id="a1113-108">Commencez par dériver une nouvelle classe de **CBasePropertyPage**.</span><span class="sxs-lookup"><span data-stu-id="a1113-108">Start by deriving a new class from **CBasePropertyPage**.</span></span> <span data-ttu-id="a1113-109">L’exemple suivant montre une partie de la déclaration, y compris certaines variables de membre privé qui seront utilisées ultérieurement dans l’exemple :</span><span class="sxs-lookup"><span data-stu-id="a1113-109">The following example shows part of the declaration, including some private member variables that will be used later in the example:</span></span>


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



<span data-ttu-id="a1113-110">Ensuite, créez une ressource de boîte de dialogue dans l’éditeur de ressources, ainsi qu’une ressource de type chaîne pour le titre de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="a1113-110">Next, create a dialog resource in the resource editor, along with a string resource for the dialog title.</span></span> <span data-ttu-id="a1113-111">La chaîne s’affiche dans l’onglet de la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="a1113-111">The string will appear in the tab for the property page.</span></span> <span data-ttu-id="a1113-112">Les deux ID de ressource sont des arguments du constructeur **CBasePropertyPage** :</span><span class="sxs-lookup"><span data-stu-id="a1113-112">The two resource IDs are arguments to the **CBasePropertyPage** constructor:</span></span>


```C++
CGrayProp::CGrayProp(IUnknown *pUnk) : 
  CBasePropertyPage(NAME("GrayProp"), pUnk, IDD_PROPPAGE, IDS_PROPPAGE_TITLE),
  m_pGray(0)
{ }
```



<span data-ttu-id="a1113-113">L’illustration suivante montre la ressource de boîte de dialogue pour la page de propriétés exemple.</span><span class="sxs-lookup"><span data-stu-id="a1113-113">The following illustration shows the dialog resource for the example property page.</span></span>

![boîte de dialogue page de propriétés](images/proppage.png)

<span data-ttu-id="a1113-115">Vous êtes maintenant prêt à implémenter la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="a1113-115">Now you are ready to implement the property page.</span></span> <span data-ttu-id="a1113-116">Voici les méthodes de **CBasePropertyPage** à remplacer :</span><span class="sxs-lookup"><span data-stu-id="a1113-116">Here are the methods in **CBasePropertyPage** to override:</span></span>

-   <span data-ttu-id="a1113-117">**OnConnect** est appelé lorsque le client crée la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="a1113-117">**OnConnect** is called when the client creates the property page.</span></span> <span data-ttu-id="a1113-118">Il définit le pointeur **IUnknown** sur le filtre.</span><span class="sxs-lookup"><span data-stu-id="a1113-118">It sets the **IUnknown** pointer to the filter.</span></span>
-   <span data-ttu-id="a1113-119">**OnActivate** est appelé lors de la création de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="a1113-119">**OnActivate** is called when the dialog is created.</span></span>
-   <span data-ttu-id="a1113-120">**OnReceiveMessage** est appelé lorsque la boîte de dialogue reçoit un message de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="a1113-120">**OnReceiveMessage** is called when the dialog receives a window message.</span></span>
-   <span data-ttu-id="a1113-121">**OnApplyChanges** est appelé lorsque l’utilisateur valide les modifications apportées aux propriétés en cliquant sur le bouton **OK** ou **appliquer** .</span><span class="sxs-lookup"><span data-stu-id="a1113-121">**OnApplyChanges** is called when the user commits the property changes by clicking the **OK** or **Apply** button.</span></span>
-   <span data-ttu-id="a1113-122">**OnDisconnect** est appelé lorsque l’utilisateur ignore la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="a1113-122">**OnDisconnect** is called when the user dismisses the property sheet.</span></span>

<span data-ttu-id="a1113-123">Le reste de ce didacticiel décrit chacune de ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="a1113-123">The remainder of this tutorial describes each of these methods.</span></span>

<span data-ttu-id="a1113-124">Suivant : [étape 5. Stocke un pointeur vers le filtre](step-5--store-a-pointer-to-the-filter.md).</span><span class="sxs-lookup"><span data-stu-id="a1113-124">Next: [Step 5. Store a Pointer to the Filter](step-5--store-a-pointer-to-the-filter.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1113-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a1113-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1113-126">Création d’une page de propriétés de filtre</span><span class="sxs-lookup"><span data-stu-id="a1113-126">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



