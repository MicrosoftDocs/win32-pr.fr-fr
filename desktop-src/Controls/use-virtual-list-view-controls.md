---
title: Utilisation des contrôles de List-View virtuels
description: Cette rubrique montre comment utiliser les contrôles de liste virtuels.
ms.assetid: DA32D7B3-5FDB-4D73-9A72-0D4EEB2A0C4F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3baf5e37d0d4f6da0cdf596dd8ba3c71e852a99
ms.sourcegitcommit: e584514ced7396dde55e58501c8c8a872229acc4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2021
ms.locfileid: "106527055"
---
# <a name="how-to-use-virtual-list-view-controls"></a><span data-ttu-id="8c847-103">Utilisation des contrôles de List-View virtuels</span><span class="sxs-lookup"><span data-stu-id="8c847-103">How to Use Virtual List-View Controls</span></span>

<span data-ttu-id="8c847-104">Cette rubrique montre comment utiliser les contrôles de liste virtuels.</span><span class="sxs-lookup"><span data-stu-id="8c847-104">This topic demonstrates how to work with virtual list-view controls.</span></span> <span data-ttu-id="8c847-105">Les exemples de code C++ qui l’accompagnent montrent comment traiter des messages de notification de contrôle de liste virtuelle, comment optimiser le cache et comment récupérer un élément du cache.</span><span class="sxs-lookup"><span data-stu-id="8c847-105">The accompanying C++ code examples show how to process virtual list-view control notification messages, how to optimize the cache, and how to retrieve an item from the cache.</span></span>

-   [<span data-ttu-id="8c847-106">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="8c847-106">What you need to know</span></span>](#what-you-need-to-know)
-   [<span data-ttu-id="8c847-107">Traiter les codes de notification de contrôle de List-View virtuel</span><span class="sxs-lookup"><span data-stu-id="8c847-107">Process Virtual List-View Control Notification Codes</span></span>](#process-virtual-list-view-control-notification-codes)
-   [<span data-ttu-id="8c847-108">Optimiser le cache</span><span class="sxs-lookup"><span data-stu-id="8c847-108">Optimize the Cache</span></span>](#optimize-the-cache)
-   [<span data-ttu-id="8c847-109">Récupérer un élément du cache</span><span class="sxs-lookup"><span data-stu-id="8c847-109">Retrieve an Item From the Cache</span></span>](#retrieve-an-item-from-the-cache)
-   [<span data-ttu-id="8c847-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8c847-110">Related topics</span></span>](#related-topics)

> [!Note]  
> <span data-ttu-id="8c847-111">L’exemple de code dans cette section suppose que le cache est un tableau alloué dynamiquement des structures définies par l’application.</span><span class="sxs-lookup"><span data-stu-id="8c847-111">The example code in this section assumes that the cache is a dynamically allocated array of application-defined structures.</span></span> <span data-ttu-id="8c847-112">La structure est définie dans l’exemple de code C++ suivant.</span><span class="sxs-lookup"><span data-stu-id="8c847-112">The structure is defined in the following C++ code example.</span></span>

 


```C++
struct RndItem
{
    int   iIcon;                 // Bitmap assigned to this item.
    UINT  state;                 // Item state value.
    TCHAR Title[BUFFER_SIZE];    // BUFFER_SIZE is a user-defined macro value.
    TCHAR SubText1[BUFFER_SIZE]; // Text for the label of the first sub-item.
    TCHAR SubText2[BUFFER_SIZE]; // Text for the label of the second item.
};

```



## <a name="what-you-need-to-know"></a><span data-ttu-id="8c847-113">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="8c847-113">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="8c847-114">Technologies</span><span class="sxs-lookup"><span data-stu-id="8c847-114">Technologies</span></span>

-   [<span data-ttu-id="8c847-115">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="8c847-115">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="8c847-116">Prérequis</span><span class="sxs-lookup"><span data-stu-id="8c847-116">Prerequisites</span></span>

-   <span data-ttu-id="8c847-117">C/C++</span><span class="sxs-lookup"><span data-stu-id="8c847-117">C/C++</span></span>
-   <span data-ttu-id="8c847-118">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="8c847-118">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="8c847-119">Instructions</span><span class="sxs-lookup"><span data-stu-id="8c847-119">Instructions</span></span>

### <a name="process-virtual-list-view-control-notification-codes"></a><span data-ttu-id="8c847-120">Traiter les codes de notification de contrôle de List-View virtuel</span><span class="sxs-lookup"><span data-stu-id="8c847-120">Process Virtual List-View Control Notification Codes</span></span>

<span data-ttu-id="8c847-121">En plus des codes de notification envoyés par d’autres contrôles d’affichage de liste, les contrôles de liste virtuels peuvent également envoyer les codes de notification [LVN \_ ODCACHEHINT](lvn-odcachehint.md) et [**LVN \_ ODFINDITEM**](lvn-odfinditem.md) .</span><span class="sxs-lookup"><span data-stu-id="8c847-121">In addition to the notification codes sent by other list-view controls, virtual list-view controls can also send the [LVN\_ODCACHEHINT](lvn-odcachehint.md) and [**LVN\_ODFINDITEM**](lvn-odfinditem.md) notification codes.</span></span>

<span data-ttu-id="8c847-122">Cette fonction définie par l’application gère les messages de notification qui sont généralement envoyés à partir d’un contrôle List-View virtuel.</span><span class="sxs-lookup"><span data-stu-id="8c847-122">This application-defined function handles notification messages that are commonly sent from a virtual list-view control.</span></span>


```C++
LRESULT OnNotify(HWND hwnd, NMHDR* pnmhdr)
{
    HRESULT hr;
    LRESULT lrt = FALSE;

    switch (pnmhdr->code)
    {
    case LVN_GETDISPINFO:
        {
            RndItem rndItem;
            NMLVDISPINFO* plvdi = (NMLVDISPINFO*) pnmhdr;

            if (-1 == plvdi->item.iItem)
            {
                OutputDebugString(TEXT("LVOWNER: Request for -1 item?\n"));
                DebugBreak();
            }

            // Retrieve information for item at index iItem.
            RetrieveItem( &rndItem, plvdi->item.iItem );

            if(plvdi->item.mask & LVIF_STATE)
            {
                // Fill in the state information.
                plvdi->item.state |= rndItem.state;
            }

            if(plvdi->item.mask & LVIF_IMAGE)
            {
                // Fill in the image information.
                plvdi->item.iImage = rndItem.iIcon;
            }

            if(plvdi->item.mask & LVIF_TEXT)
            {
                // Fill in the text information.
                switch (plvdi->item.iSubItem)
                {
                case 0:
                    // Copy the main item text.
                    hr = StringCchCopy(plvdi->item.pszText, MAX_COUNT, rndItem.Title);

                    if(FAILED(hr))
                    { 
                        // Insert error handling code here. MAX_COUNT
                        // is a user-defined value. You must not enter                                
                        // more characters than specified by MAX_COUNT or  
                        // the text will be truncated.
                    }
                    break;

                case 1:
                    // Copy SubItem1 text.
                    hr = StringCchCopy( plvdi->item.pszText, MAX_COUNT, rndItem.SubText1);

                    if(FAILED(hr))
                    {
                        // Insert error handling code here. MAX_COUNT
                        // is a user-defined value. You must not enter               
                        // more characters than specified by MAX_COUNT or   
                        // the text will be truncated..
                    }
                    break;

                case 2:
                    // Copy SubItem2 text.
                    hr = StringCchCopy(plvdi->item.pszText, MAX_COUNT, rndItem.SubText2);

                    if(FAILED(hr))
                    {
                        // Insert error handling code here. MAX_COUNT
                        // is a user-defined value. You must not enter                    
                        // more characters than specified by MAX_COUNT or  
                        // the text will be truncated..
                    }
                    break;

                default:
                    break;

                }

            }

            lrt = FALSE;
            break;
        }

    case LVN_ODCACHEHINT:
        {
            NMLVCACHEHINT* pcachehint = (NMLVCACHEHINT*) pnmhdr;

            // Load the cache with the recommended range.
            PrepCache( pcachehint->iFrom, pcachehint->iTo );
            break;
        }

    case LVN_ODFINDITEM:
        {
            LPNMLVFINDITEM pnmfi = NULL;
            
            pnmfi = (LPNMLVFINDITEM)pnmhdr;

            // Call a user-defined function that finds the index according to
            // LVFINDINFO (which is embedded in the LPNMLVFINDITEM structure).
            // If nothing is found, then set the return value to -1.

            break;
        }

    default:
        break;

    }       // End Switch block.

    return(lrt);
}
```



### <a name="optimize-the-cache"></a><span data-ttu-id="8c847-123">Optimiser le cache</span><span class="sxs-lookup"><span data-stu-id="8c847-123">Optimize the Cache</span></span>

<span data-ttu-id="8c847-124">Un contrôle d’affichage de liste virtuel envoie un message de notification [LVN \_ ODCACHEHINT](lvn-odcachehint.md) lorsque le contenu de sa zone d’affichage a changé.</span><span class="sxs-lookup"><span data-stu-id="8c847-124">A virtual list-view control sends a [LVN\_ODCACHEHINT](lvn-odcachehint.md) notification message when the contents of its display area have changed.</span></span> <span data-ttu-id="8c847-125">Le message contient des informations sur la plage d’éléments à mettre en cache.</span><span class="sxs-lookup"><span data-stu-id="8c847-125">The message contains information about the range of items to be cached.</span></span> <span data-ttu-id="8c847-126">À la réception du message de notification, votre application doit être préparée à charger le cache avec les informations relatives à l’élément pour la plage demandée afin que les informations soient immédiatement disponibles lorsqu’un message de notification [LVN \_ GETDISPINFO](lvn-getdispinfo.md) est envoyé.</span><span class="sxs-lookup"><span data-stu-id="8c847-126">Upon receiving the notification message, your application must be prepared to load the cache with item information for the requested range so that the information will be readily available when an [LVN\_GETDISPINFO](lvn-getdispinfo.md) notification message is sent.</span></span>

<span data-ttu-id="8c847-127">Dans l’exemple de code C++ suivant, la fonction définie par l’application accepte la plage d’éléments pour le cache qui est envoyé par un contrôle List-View virtuel.</span><span class="sxs-lookup"><span data-stu-id="8c847-127">In the following C++ code example, the application-defined function accepts the range of items for the cache that is sent by a virtual list-view control.</span></span> <span data-ttu-id="8c847-128">Il effectue une vérification pour déterminer que la plage d’éléments demandée n’est pas déjà mise en cache, puis alloue la mémoire globale requise et remplit le cache si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="8c847-128">It performs a verification to determine that the requested range of items is not already cached, and then it allocates the required global memory and fills the cache if necessary.</span></span>


```C++
void PrepCache(int iFrom, int iTo)
{
    /*  Global Variables

     *  g_priCache[ ]: the main cache.
     *  g_iCache:      the index of the first item in the main cache.
     *  g_cCache:      the count of items in the main cache.
     *
     *  g_priEndCache[ ]: the cache of items at the end of the list.
     *  g_iEndCache:      the index of the first item in the end cache.
     *  g_cEndCache:      the count of items in the end cache.
     */
     
    // Local Variables
    int i;
    BOOL fOLFrom = FALSE;
    BOOL   fOLTo = FALSE;

    // Check to see if this is the end cache.
    if ((iTo == g_cCache - 1) && ((iTo - iFrom) < 30))  // 30 entries wide.
    {
        // Check to see if this is a portion of the current end cache.
        if ((g_cCache) && (iFrom >= g_iEndCache) && (iFrom < g_iEndCache+g_cEndCache))
            return;
            // If it is a part of current end cache, no loading is necessary.

        // This is a new end cache. Free the old memory.
        if ( g_priEndCache )
            GlobalFree( g_priEndCache );
            
        // Set the index and count values for the new end cache,
        // and then retrieve the memory.
        g_iEndCache   = iFrom;
        g_cEndCache   = (iTo - iFrom + 1);
        g_priEndCache = (RndItem *)GlobalAlloc(GPTR, sizeof(RndItem) * g_cEndCache);

        if (! g_priEndCache)
        {
            // TODO: Out of memory. Perform error handling.
        }

        // Loop to fill the cache with the recommended items.
        for (i=0; i<g_cEndCache; i++)
        {
            // TODO: Call a function that accesses item information and
            // fills a cache element.
        }
    }

    else
    {   
        // It is not a member of the current end cache.
        // Try the primary cache instead.

        // Check to see if iFrom is within the primary cache.
        if ((g_cCache) && (iFrom >= g_iCache) && (iFrom < g_iCache+g_cCache))
            fOLFrom = TRUE;

        // Check to see if iTo is within the primary cache.
        if ((g_cCache) && (iTo >= g_iCache) && (iTo <= g_iCache+g_cCache))
            fOLTo = TRUE;

        // do nothing if both iFrom and iTo are within the current cache.

        if (fOLFrom && fOLTo)
            return;

        // Enlarge the cache size rather than make it specific to this hint.
        if (fOLFrom)
            iFrom = g_iCache;

        else if (fOLTo)
            iTo = g_iCache + g_cCache;

        // A new primary cache is needed. Free the old primary cache.
        if ( g_priCache )
            GlobalFree( g_priCache );

        // Set the index and count values for the new primary cache,
        // and then retrieve the memory.
        g_iCache   = iFrom;
        g_cCache   = (iTo - iFrom + 1);
        g_priCache = (RndItem *)GlobalAlloc( GPTR, sizeof( RndItem ) * g_cCache );

        if (!g_priCache)
        {
            // TODO: Out of memory. Do error handling.
        }

        // Loop to fill the cache with the recommended items.
        for (i=0; i<g_cCache; i++)
        {
            // TODO: Call a function that accesses item information
            // and fills a cache element.
        }
    }
}
```



### <a name="retrieve-an-item-from-the-cache"></a><span data-ttu-id="8c847-129">Récupérer un élément du cache</span><span class="sxs-lookup"><span data-stu-id="8c847-129">Retrieve an Item From the Cache</span></span>

<span data-ttu-id="8c847-130">Cet exemple de fonction accepte deux paramètres, l’adresse de la structure définie par l’application et une valeur entière représentant l’index de l’élément dans la liste.</span><span class="sxs-lookup"><span data-stu-id="8c847-130">This example function accepts two parameters, the address of the application-defined structure and an integer value representing the index of the item in the list.</span></span> <span data-ttu-id="8c847-131">Il vérifie la valeur d’index pour déterminer si l’élément souhaité est mis en cache.</span><span class="sxs-lookup"><span data-stu-id="8c847-131">It checks the index value to discover if the desired item is cached.</span></span> <span data-ttu-id="8c847-132">Si c’est le cas, le pointeur qui a été passé à la fonction est défini sur un emplacement dans le cache.</span><span class="sxs-lookup"><span data-stu-id="8c847-132">If it is, the pointer that was passed to the function is set to a location in the cache.</span></span> <span data-ttu-id="8c847-133">Si l’élément ne se trouve pas dans le cache principal ou de fin, les informations de l’élément doivent être situées manuellement.</span><span class="sxs-lookup"><span data-stu-id="8c847-133">If the item is not in the main or end cache, the item information must be located manually.</span></span>


```C++
void RetrieveItem( RndItem * prndItem, int index )
{
    // Global Variables

    // g_priCache[ ]: the main cache.
    // g_iCache:      the index of the first item in the main cache.
    // c_cCache:      the count of items in the main cache.
    //
    // g_priEndCache[ ]:  the cache of items at the end of the list.
    // g_iEndCache:       the index of the first item in the end cache.
    // g_cEndCache:       the count of items in the end cache.
    //

    // Check to see if the item is in the main cache.
    if ((index >= g_iCache) && (index < g_iCache + g_cCache))
        *prndItem = g_priCache[index-g_iCache];

    // If it is not in the main cache, then check to see if
    // the item is in the end area cache.
    else if ((index >= g_iEndCache) && (index < g_iEndCache + g_cEndCache))
        *prndItem = g_priEndCache[index-g_iEndCache];

    else
    {
        // The item is not in either cache.
        // Therefore, retrieve the item information manually.
    }
}
```



## <a name="remarks"></a><span data-ttu-id="8c847-134">Notes</span><span class="sxs-lookup"><span data-stu-id="8c847-134">Remarks</span></span>

<span data-ttu-id="8c847-135">Pour obtenir la liste des messages de fenêtre traités par un contrôle de liste, consultez [List-View le traitement des messages par défaut](listview-message-processing.md).</span><span class="sxs-lookup"><span data-stu-id="8c847-135">For a list of the window messages processed by a list-view control, see [Default List-View Message Processing](listview-message-processing.md).</span></span>

## <a name="complete-example"></a><span data-ttu-id="8c847-136">Exemple complet</span><span class="sxs-lookup"><span data-stu-id="8c847-136">Complete example</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c847-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8c847-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c847-138">Référence du contrôle List-View</span><span class="sxs-lookup"><span data-stu-id="8c847-138">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="8c847-139">À propos des contrôles List-View</span><span class="sxs-lookup"><span data-stu-id="8c847-139">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="8c847-140">Utilisation de contrôles List-View</span><span class="sxs-lookup"><span data-stu-id="8c847-140">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 




