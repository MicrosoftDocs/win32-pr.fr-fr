---
title: Utilisation d’appareils mobiles
description: Utilisation d’appareils mobiles
ms.assetid: 145ede07-a23b-486b-a561-9c87a48b72a8
keywords:
- Lecteur Windows Media, appareils mobiles
- Modèle objet du lecteur Windows Media, appareils mobiles
- modèle objet, appareils mobiles
- Contrôle ActiveX du lecteur Windows Media, appareils mobiles
- Contrôle ActiveX, appareils mobiles
- Windows Media Player Mobile contrôle ActiveX, appareils mobiles
- Windows Media Player Mobile, appareils mobiles
- appareils mobiles, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b64c6e7047864b899a2d7dca2ba4754cc7cb5dc2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311314"
---
# <a name="working-with-portable-devices"></a><span data-ttu-id="019af-111">Utilisation d’appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="019af-111">Working with Portable Devices</span></span>

<span data-ttu-id="019af-112">Cette section explique comment utiliser un contrôle ActiveX Windows Media Player distant pour travailler avec des appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="019af-112">This section describes how to use a remoted Windows Media Player ActiveX control to work with portable devices.</span></span>

<span data-ttu-id="019af-113">Les exemples de code de cette section utilisent des classes Active Template Library (ATL), telles que **CComPtr**.</span><span class="sxs-lookup"><span data-stu-id="019af-113">The code examples in this section use Active Template Library (ATL) classes, such as **CComPtr**.</span></span>

## <a name="included-headers"></a><span data-ttu-id="019af-114">En-têtes inclus</span><span class="sxs-lookup"><span data-stu-id="019af-114">Included Headers</span></span>

<span data-ttu-id="019af-115">Pour utiliser le code de cette section, incluez les en-têtes suivants :</span><span class="sxs-lookup"><span data-stu-id="019af-115">To use the code in this section, include the following headers:</span></span>


```C++
#include <atlbase.h>
#include <atlcom.h>
#include <atlwin.h>
#include <commctrl.h>
#include "wmp.h"
#include "wmpids.h"
```



## <a name="iwmpplayer-pointer"></a><span data-ttu-id="019af-116">Pointeur IWMPPlayer</span><span class="sxs-lookup"><span data-stu-id="019af-116">IWMPPlayer Pointer</span></span>

<span data-ttu-id="019af-117">Le pointeur **IWMPPlayer** est stocké dans une variable membre.</span><span class="sxs-lookup"><span data-stu-id="019af-117">The **IWMPPlayer** pointer is stored in a member variable.</span></span>


```C++
CComPtr<IWMPPlayer> m_spPlayer;
```



## <a name="devices-are-stored-in-an-array"></a><span data-ttu-id="019af-118">Les appareils sont stockés dans un tableau</span><span class="sxs-lookup"><span data-stu-id="019af-118">Devices are Stored in an Array</span></span>

<span data-ttu-id="019af-119">L’exemple de code accède à la variable de membre suivante, qui doit être déclarée dans l’en-tête du projet :</span><span class="sxs-lookup"><span data-stu-id="019af-119">The example code accesses the following member variable, to be declared in the project header:</span></span>


```C++
IWMPSyncDevice **m_ppWMPDevices; // Points to the custom device array.
```



<span data-ttu-id="019af-120">Le nombre de périphériques est stocké dans une variable membre.</span><span class="sxs-lookup"><span data-stu-id="019af-120">The device count is stored in a member variable.</span></span>


```C++
int m_cDevices; // Count of devices.
```



## <a name="retrieving-a-device-pointer"></a><span data-ttu-id="019af-121">Récupération d’un pointeur d’appareil</span><span class="sxs-lookup"><span data-stu-id="019af-121">Retrieving a Device Pointer</span></span>

<span data-ttu-id="019af-122">Un pointeur vers un appareil particulier est récupéré via son index de tableau à l’aide d’un code similaire à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="019af-122">A pointer to a particular device is retrieved through its array index by using code similar to the following:</span></span>


```C++
CComPtr<IWMPSyncDevice> spSyncDevice(m_ppWMPDevices[lIndex]);
```



<span data-ttu-id="019af-123">Notez que l’index présenté dans les exemples précédents n’est pas l’index de partenariat pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="019af-123">Note that the index shown in the preceding examples is not the partnership index for the device.</span></span> <span data-ttu-id="019af-124">Il s’agit de l’index de l’appareil dans le tableau personnalisé des appareils.</span><span class="sxs-lookup"><span data-stu-id="019af-124">It is the index to the device in the custom array of devices.</span></span>

## <a name="cleaning-up"></a><span data-ttu-id="019af-125">Nettoyage</span><span class="sxs-lookup"><span data-stu-id="019af-125">Cleaning Up</span></span>

<span data-ttu-id="019af-126">Les exemples utilisent la fonction suivante pour libérer la mémoire dans le tableau de périphériques et pour libérer les pointeurs d’interface :</span><span class="sxs-lookup"><span data-stu-id="019af-126">The examples use the following function to free the memory in the device array and to release the interface pointers:</span></span>


```C++
void CMainDlg::FreeDeviceArray()
{
    if(m_ppWMPDevices)
    {
        for(long i = 0; i < m_cDevices; i++)
        {
            m_ppWMPDevices[i]->Release();
        }
 
        delete[] m_ppWMPDevices;
        m_ppWMPDevices = NULL;        
    }
}
```



## <a name="devices-are-displayed-in-a-list-box"></a><span data-ttu-id="019af-127">Les appareils s’affichent dans une zone de liste</span><span class="sxs-lookup"><span data-stu-id="019af-127">Devices are Displayed in a List Box</span></span>

<span data-ttu-id="019af-128">La fonction GetSelectedDeviceIndex retourne l’index de l’appareil que l’utilisateur a sélectionné dans une zone de liste à l’aide du code suivant :</span><span class="sxs-lookup"><span data-stu-id="019af-128">The GetSelectedDeviceIndex function returns the index of the device the user selected in a list box by using the following code:</span></span>


```C++
long CMainDlg::GetSelectedDeviceIndex()
{
    return (long)SendMessage(GetDlgItem(IDC_DEVICES), LB_GETCURSEL, 0, 0);
}
```



## <a name="user-interface-state-is-managed-by-a-single-function"></a><span data-ttu-id="019af-129">L’état de l’interface utilisateur est géré par une seule fonction</span><span class="sxs-lookup"><span data-stu-id="019af-129">User Interface State is Managed by a Single Function</span></span>

<span data-ttu-id="019af-130">La fonction SetUIState gère l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="019af-130">The SetUIState function manages the user interface.</span></span>


```C++
SetUIState(UIState 
NewState, BOOL 
bConnected)
```



<span data-ttu-id="019af-131">Les détails de cette fonction ne sont pas pertinents pour les discussions de cette section, mais n’oubliez pas que cette fonction effectue des tâches telles que l’activation ou la désactivation de contrôles et la modification du texte affiché dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="019af-131">The details of this function are not relevant to the discussions in this section, but be aware that this function performs tasks like enabling or disabling controls and changing display text in the user interface.</span></span>

<span data-ttu-id="019af-132">L’énumération UIState a été définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="019af-132">The UIState enumeration was defined as follows:</span></span>


```C++
enum UIState
{
    Partnership,
    NoPartnership,
    Synchronizing
};
```



<span data-ttu-id="019af-133">Le paramètre *bconnected* spécifie s’il faut configurer l’interface utilisateur pour un appareil connecté (true signifie que l’appareil est connecté).</span><span class="sxs-lookup"><span data-stu-id="019af-133">The *bConnected* parameter specifies whether to configure the user interface for a connected device (TRUE means the device is connected).</span></span> <span data-ttu-id="019af-134">Les paramètres *NewState* et *bconnected* fournissent les informations nécessaires à la fonction pour effectuer son travail.</span><span class="sxs-lookup"><span data-stu-id="019af-134">The *NewState* and *bConnected* parameters convey the information needed for the function to do its work.</span></span>

<span data-ttu-id="019af-135">Les sections suivantes fournissent des explications sur l’exemple de code :</span><span class="sxs-lookup"><span data-stu-id="019af-135">The following sections provide explanations of the example code:</span></span>

-   [<span data-ttu-id="019af-136">Énumération des appareils</span><span class="sxs-lookup"><span data-stu-id="019af-136">Enumerating Devices</span></span>](enumerating-devices.md)
-   [<span data-ttu-id="019af-137">Récupération des attributs de l’appareil</span><span class="sxs-lookup"><span data-stu-id="019af-137">Retrieving Device Attributes</span></span>](retrieving-device-attributes.md)
-   [<span data-ttu-id="019af-138">Indication de la progression de la synchronisation</span><span class="sxs-lookup"><span data-stu-id="019af-138">Showing Synchronization Progress</span></span>](showing-synchronization-progress.md)
-   [<span data-ttu-id="019af-139">Gestion des sélections de synchronisation</span><span class="sxs-lookup"><span data-stu-id="019af-139">Managing Synchronization Playlists</span></span>](managing-synchronization-playlists.md)

## <a name="related-topics"></a><span data-ttu-id="019af-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="019af-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="019af-141">**Guide de contrôle du lecteur**</span><span class="sxs-lookup"><span data-stu-id="019af-141">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




