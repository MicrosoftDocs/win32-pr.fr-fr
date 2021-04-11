---
description: Windows envoie à toutes les fenêtres de niveau supérieur un ensemble de \_ messages WM DEVICECHANGE par défaut quand de nouveaux périphériques ou médias (tels qu’un CD ou un DVD) sont ajoutés et disponibles, et lorsque des appareils ou des médias existants sont supprimés.
ms.assetid: 26baa3aa-e54d-42fe-b2b2-a3fcca6dee91
title: Détection de l’insertion ou de la suppression d’un média
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e6cfd4539d6f2ce5eac41e355f56a5a87835505
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104116054"
---
# <a name="detecting-media-insertion-or-removal"></a><span data-ttu-id="85340-103">Détection de l’insertion ou de la suppression d’un média</span><span class="sxs-lookup"><span data-stu-id="85340-103">Detecting Media Insertion or Removal</span></span>

<span data-ttu-id="85340-104">Windows envoie à toutes les fenêtres de niveau supérieur un ensemble de messages [**WM \_ DEVICECHANGE**](wm-devicechange.md) par défaut quand de nouveaux périphériques ou médias (tels qu’un CD ou un DVD) sont ajoutés et disponibles, et lorsque des appareils ou des médias existants sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="85340-104">Windows sends all top-level windows a set of default [**WM\_DEVICECHANGE**](wm-devicechange.md) messages when new devices or media (such as a CD or DVD) are added and become available, and when existing devices or media are removed.</span></span> <span data-ttu-id="85340-105">Vous n’avez pas besoin de vous inscrire pour recevoir ces messages par défaut.</span><span class="sxs-lookup"><span data-stu-id="85340-105">You do not need to register to receive these default messages.</span></span> <span data-ttu-id="85340-106">Consultez la section Notes dans [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) pour plus d’informations sur les messages qui sont envoyés par défaut.</span><span class="sxs-lookup"><span data-stu-id="85340-106">See the Remarks section in [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) for details on which messages are sent by default.</span></span> <span data-ttu-id="85340-107">Les messages dans l’exemple de code ci-dessous figurent parmi les messages par défaut.</span><span class="sxs-lookup"><span data-stu-id="85340-107">The messages in the code example below are among the default messages.</span></span>

> [!Note]  
> <span data-ttu-id="85340-108">Windows envoie uniquement les messages [**WM \_ DEVICECHANGE**](wm-devicechange.md) pour les événements de support CD ou DVD aux fenêtres de niveau supérieur qui sont détenues par les applications qui s’exécutent dans la session de la console active.</span><span class="sxs-lookup"><span data-stu-id="85340-108">Windows only sends [**WM\_DEVICECHANGE**](wm-devicechange.md) messages for CD or DVD media events to top-level windows that are owned by applications that run in the active console session.</span></span> <span data-ttu-id="85340-109">Les fenêtres de niveau supérieur qui sont détenues par les applications qui s’exécutent dans une session Bureau à distance ne reçoivent pas les messages [**WM \_ DEVICECHANGE**](wm-devicechange.md) pour les événements de média CD ou DVD.</span><span class="sxs-lookup"><span data-stu-id="85340-109">Top-level windows that are owned by applications that run in a remote desktop session do not receive [**WM\_DEVICECHANGE**](wm-devicechange.md) messages for CD or DVD media events.</span></span>

 

<span data-ttu-id="85340-110">Chaque message [**WM \_ DEVICECHANGE**](wm-devicechange.md) est associé à un événement qui décrit la modification et une structure qui fournit des informations détaillées sur la modification.</span><span class="sxs-lookup"><span data-stu-id="85340-110">Each [**WM\_DEVICECHANGE**](wm-devicechange.md) message has an associated event that describes the change, and a structure that provides detailed information about the change.</span></span> <span data-ttu-id="85340-111">La structure se compose d’un en-tête indépendant des événements, d’un [**\_ \_ HDR de diffusion de développement**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr), suivi de membres dépendants d’événements.</span><span class="sxs-lookup"><span data-stu-id="85340-111">The structure consists of an event-independent header, [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr), followed by event-dependent members.</span></span> <span data-ttu-id="85340-112">Les membres dépendants des événements décrivent l’appareil auquel s’applique l’événement.</span><span class="sxs-lookup"><span data-stu-id="85340-112">The event-dependent members describe the device to which the event applies.</span></span> <span data-ttu-id="85340-113">Pour utiliser cette structure, les applications doivent d’abord déterminer le type d’événement et le type d’appareil.</span><span class="sxs-lookup"><span data-stu-id="85340-113">To use this structure, applications must first determine the event type and the device type.</span></span> <span data-ttu-id="85340-114">Ils peuvent ensuite utiliser la structure appropriée pour prendre les mesures appropriées.</span><span class="sxs-lookup"><span data-stu-id="85340-114">Then, they can use the correct structure to take appropriate action.</span></span>

<span data-ttu-id="85340-115">Lorsque l’utilisateur insère un nouveau CD ou DVD dans un lecteur, les applications reçoivent un message [**WM \_ DEVICECHANGE**](wm-devicechange.md) avec un [événement \_ DEVICEARRIVAL DBT](dbt-devicearrival.md) .</span><span class="sxs-lookup"><span data-stu-id="85340-115">When the user inserts a new CD or DVD into a drive, applications receive a [**WM\_DEVICECHANGE**](wm-devicechange.md) message with a [DBT\_DEVICEARRIVAL](dbt-devicearrival.md) event.</span></span> <span data-ttu-id="85340-116">L’application doit vérifier l’événement pour s’assurer que le type d’appareil arrivant est un volume (le membre **dbch \_ DeviceType** est **DBT \_ DEVTYP \_**) et que la modification affecte le support (le membre des **\_ indicateurs DBCV** est **DBTF \_ Media**).</span><span class="sxs-lookup"><span data-stu-id="85340-116">The application must check the event to ensure that the type of device arriving is a volume (the **dbch\_devicetype** member is **DBT\_DEVTYP\_VOLUME**) and that the change affects the media (the **dbcv\_flags** member is **DBTF\_MEDIA**).</span></span>

<span data-ttu-id="85340-117">Lorsque l’utilisateur supprime un CD ou un DVD d’un lecteur, les applications reçoivent un message [**WM \_ DEVICECHANGE**](wm-devicechange.md) avec un événement [ \_ DEVICEREMOVECOMPLETE DBT](dbt-deviceremovecomplete.md) .</span><span class="sxs-lookup"><span data-stu-id="85340-117">When the user removes a CD or DVD from a drive, applications receive a [**WM\_DEVICECHANGE**](wm-devicechange.md) message with a [DBT\_DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md) event.</span></span> <span data-ttu-id="85340-118">Là encore, l’application doit vérifier l’événement pour s’assurer que le périphérique en cours de suppression est un volume et que la modification affecte le support.</span><span class="sxs-lookup"><span data-stu-id="85340-118">Again, the application must check the event to ensure that the device being removed is a volume and that the change affects the media.</span></span>

<span data-ttu-id="85340-119">Le code suivant montre comment vérifier l’insertion ou la suppression d’un CD ou d’un DVD.</span><span class="sxs-lookup"><span data-stu-id="85340-119">The following code demonstrates how to check for insertion or removal of a CD or DVD.</span></span>


```C++
#include <windows.h>
#include <dbt.h>
#include <strsafe.h>
#pragma comment(lib, "user32.lib" )

void Main_OnDeviceChange( HWND hwnd, WPARAM wParam, LPARAM lParam );
char FirstDriveFromMask( ULONG unitmask );  //prototype

/*------------------------------------------------------------------
   Main_OnDeviceChange( hwnd, wParam, lParam )

   Description
      Handles WM_DEVICECHANGE messages sent to the application's
      top-level window.
--------------------------------------------------------------------*/

void Main_OnDeviceChange( HWND hwnd, WPARAM wParam, LPARAM lParam )
 {
  PDEV_BROADCAST_HDR lpdb = (PDEV_BROADCAST_HDR)lParam;
  TCHAR szMsg[80];

  switch(wParam )
   {
    case DBT_DEVICEARRIVAL:
      // Check whether a CD or DVD was inserted into a drive.
      if (lpdb -> dbch_devicetype == DBT_DEVTYP_VOLUME)
       {
        PDEV_BROADCAST_VOLUME lpdbv = (PDEV_BROADCAST_VOLUME)lpdb;

        if (lpdbv -> dbcv_flags & DBTF_MEDIA)
         {
          StringCchPrintf( szMsg, sizeof(szMsg)/sizeof(szMsg[0]), 
                           TEXT("Drive %c: Media has arrived.\n"), 
                           FirstDriveFromMask(lpdbv ->dbcv_unitmask) );

          MessageBox( hwnd, szMsg, TEXT("WM_DEVICECHANGE"), MB_OK );
         }
       }
      break;

    case DBT_DEVICEREMOVECOMPLETE:
      // Check whether a CD or DVD was removed from a drive.
      if (lpdb -> dbch_devicetype == DBT_DEVTYP_VOLUME)
       {
        PDEV_BROADCAST_VOLUME lpdbv = (PDEV_BROADCAST_VOLUME)lpdb;

        if (lpdbv -> dbcv_flags & DBTF_MEDIA)
         {
          StringCchPrintf( szMsg, sizeof(szMsg)/sizeof(szMsg[0]), 
                           TEXT("Drive %c: Media was removed.\n" ),
                           FirstDriveFromMask(lpdbv ->dbcv_unitmask) );

          MessageBox( hwnd, szMsg, TEXT("WM_DEVICECHANGE" ), MB_OK );
         }
       }
      break;

    default:
      /*
        Process other WM_DEVICECHANGE notifications for other 
        devices or reasons.
      */ 
      ;
   }
}

/*------------------------------------------------------------------
   FirstDriveFromMask( unitmask )

   Description
     Finds the first valid drive letter from a mask of drive letters.
     The mask must be in the format bit 0 = A, bit 1 = B, bit 2 = C, 
     and so on. A valid drive letter is defined when the 
     corresponding bit is set to 1.

   Returns the first drive letter that was found.
--------------------------------------------------------------------*/

char FirstDriveFromMask( ULONG unitmask )
 {
  char i;

  for (i = 0; i < 26; ++i)
   {
    if (unitmask & 0x1)
      break;
    unitmask = unitmask >> 1;
   }

  return( i + 'A' );
}
```



## <a name="related-topics"></a><span data-ttu-id="85340-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="85340-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85340-121">Événements de l’appareil</span><span class="sxs-lookup"><span data-stu-id="85340-121">Device Events</span></span>](device-events.md)
</dt> </dl>

 

 



