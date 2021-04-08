---
title: Définition du format d’heure
description: Définition du format d’heure
ms.assetid: c670d47e-30fc-4637-b468-b6a415605dca
keywords:
- MCI_SET message de commande
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6bc48faa36fea49b0aba749476c998572ebf400
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842186"
---
# <a name="setting-the-time-format"></a><span data-ttu-id="49fa8-104">Définition du format d’heure</span><span class="sxs-lookup"><span data-stu-id="49fa8-104">Setting the Time Format</span></span>

<span data-ttu-id="49fa8-105">Utilisez le message de commande [**\_ Set MCI**](mci-set.md) avec la [**structure \_ Set \_ PARMS de MCI**](mci-set-parms.md) pour définir le format d’heure d’un appareil ouvert.</span><span class="sxs-lookup"><span data-stu-id="49fa8-105">Use the [**MCI\_SET**](mci-set.md) command message along with the [**MCI\_SET\_PARMS**](mci-set-parms.md) structure to set the time format for an open device.</span></span> <span data-ttu-id="49fa8-106">Définissez le membre **dwTimeFormat** sur l’une des constantes suivantes.</span><span class="sxs-lookup"><span data-stu-id="49fa8-106">Set the **dwTimeFormat** member to one of the following constants.</span></span>



| <span data-ttu-id="49fa8-107">Constante</span><span class="sxs-lookup"><span data-stu-id="49fa8-107">Constant</span></span>                   | <span data-ttu-id="49fa8-108">Format de l’heure</span><span class="sxs-lookup"><span data-stu-id="49fa8-108">Time format</span></span>                                          |
|----------------------------|------------------------------------------------------|
| <span data-ttu-id="49fa8-109">\_octets au format MCI \_</span><span class="sxs-lookup"><span data-stu-id="49fa8-109">MCI\_FORMAT\_BYTES</span></span>         | <span data-ttu-id="49fa8-110">Octets (dans les fichiers de format PCM modulé en code Pulse \[ \] )</span><span class="sxs-lookup"><span data-stu-id="49fa8-110">Bytes (in pulse code modulated \[PCM\] format files)</span></span> |
| <span data-ttu-id="49fa8-111">FORMAT MCI en \_ \_ millisecondes</span><span class="sxs-lookup"><span data-stu-id="49fa8-111">MCI\_FORMAT\_MILLISECONDS</span></span>  | <span data-ttu-id="49fa8-112">Millisecondes</span><span class="sxs-lookup"><span data-stu-id="49fa8-112">Milliseconds</span></span>                                         |
| <span data-ttu-id="49fa8-113">FORMAT MCI ( \_ \_ MSF)</span><span class="sxs-lookup"><span data-stu-id="49fa8-113">MCI\_FORMAT\_MSF</span></span>           | <span data-ttu-id="49fa8-114">Minute/seconde/image</span><span class="sxs-lookup"><span data-stu-id="49fa8-114">Minute/second/frame</span></span>                                  |
| <span data-ttu-id="49fa8-115">\_exemples de format MCI \_</span><span class="sxs-lookup"><span data-stu-id="49fa8-115">MCI\_FORMAT\_SAMPLES</span></span>       | <span data-ttu-id="49fa8-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="49fa8-116">Samples</span></span>                                              |
| <span data-ttu-id="49fa8-117">\_Format MCI \_ SMPTE \_ 24</span><span class="sxs-lookup"><span data-stu-id="49fa8-117">MCI\_FORMAT\_SMPTE\_24</span></span>     | <span data-ttu-id="49fa8-118">SMPTE, 24 Frame</span><span class="sxs-lookup"><span data-stu-id="49fa8-118">SMPTE, 24 frame</span></span>                                      |
| <span data-ttu-id="49fa8-119">\_Format MCI \_ SMPTE \_ 25</span><span class="sxs-lookup"><span data-stu-id="49fa8-119">MCI\_FORMAT\_SMPTE\_25</span></span>     | <span data-ttu-id="49fa8-120">SMPTE, 25 frame</span><span class="sxs-lookup"><span data-stu-id="49fa8-120">SMPTE, 25 frame</span></span>                                      |
| <span data-ttu-id="49fa8-121">FORMAT MCI, \_ \_ SMPTE \_ 30</span><span class="sxs-lookup"><span data-stu-id="49fa8-121">MCI\_FORMAT\_SMPTE\_30</span></span>     | <span data-ttu-id="49fa8-122">SMPTE, 30 Frame</span><span class="sxs-lookup"><span data-stu-id="49fa8-122">SMPTE, 30 frame</span></span>                                      |
| <span data-ttu-id="49fa8-123">\_Format MCI \_ \_ 30DROP SMPTE</span><span class="sxs-lookup"><span data-stu-id="49fa8-123">MCI\_FORMAT\_SMPTE\_30DROP</span></span> | <span data-ttu-id="49fa8-124">SMPTE, 30 images</span><span class="sxs-lookup"><span data-stu-id="49fa8-124">SMPTE, 30 frame drop</span></span>                                 |
| <span data-ttu-id="49fa8-125">\_format MCI \_ TMSF</span><span class="sxs-lookup"><span data-stu-id="49fa8-125">MCI\_FORMAT\_TMSF</span></span>          | <span data-ttu-id="49fa8-126">Suivi/minute/seconde/image</span><span class="sxs-lookup"><span data-stu-id="49fa8-126">Track/minute/second/frame</span></span>                            |
| <span data-ttu-id="49fa8-127">MCI \_ Seq \_ format \_ SONGPTR</span><span class="sxs-lookup"><span data-stu-id="49fa8-127">MCI\_SEQ\_FORMAT\_SONGPTR</span></span>  | <span data-ttu-id="49fa8-128">Pointeur de chanson MIDI</span><span class="sxs-lookup"><span data-stu-id="49fa8-128">MIDI song pointer</span></span>                                    |



 

<span data-ttu-id="49fa8-129">L’exemple suivant définit le format d’heure sur millisecondes sur l’appareil spécifié par la variable wDeviceID à l’aide de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="49fa8-129">The following example sets the time format to milliseconds on the device specified by the wDeviceID variable using the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span>


```C++
UINT wDeviceID; 
MCI_SET_PARMS mciSetParms; 

// Set time format to milliseconds. 

mciSetParms.dwTimeFormat = MCI_FORMAT_MILLISECONDS; 
if( mciSendCommand(wDeviceID, MCI_SET, MCI_SET_TIME_FORMAT, 
                  (DWORD) &mciSetParms)) 
{
    // Error, unable to set time format. 
    return FALSE; 
}
else 
{
    // Time format set successfully. 
    return TRUE; 
}
```



 

 