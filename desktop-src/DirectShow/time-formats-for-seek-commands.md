---
description: Formats d’heure pour les commandes de recherche
ms.assetid: d9c1b860-f75f-4886-95d6-c62e9e5b69eb
title: Formats d’heure pour les commandes de recherche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de8217873a9443c2b56c60523f95a6fe599ee045
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530327"
---
# <a name="time-formats-for-seek-commands"></a><span data-ttu-id="70b8f-103">Formats d’heure pour les commandes de recherche</span><span class="sxs-lookup"><span data-stu-id="70b8f-103">Time Formats For Seek Commands</span></span>

<span data-ttu-id="70b8f-104">La plupart des méthodes de l’interface **IMediaSeeking** ont des paramètres qui expriment les valeurs de position, telles que la position actuelle ou la position d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="70b8f-104">Many of the methods in the **IMediaSeeking** interface have parameters that express position values, such as current position or stop position.</span></span> <span data-ttu-id="70b8f-105">Par défaut, ces paramètres sont exprimés en unités de nanosecondes de 100, également appelées « temps de référence ».</span><span class="sxs-lookup"><span data-stu-id="70b8f-105">By default, these parameters are expressed in units of 100 nanoseconds, also called reference time.</span></span> <span data-ttu-id="70b8f-106">Tout filtre pouvant être cherché doit prendre en charge la recherche par temps de référence.</span><span class="sxs-lookup"><span data-stu-id="70b8f-106">Any filter that can seek must support seeking by reference time.</span></span> <span data-ttu-id="70b8f-107">Certains filtres peuvent également rechercher à l’aide d’autres unités de temps, telles que la recherche d’un numéro de séquence particulier, ou la recherche d’un décalage d’octet donné dans un flux.</span><span class="sxs-lookup"><span data-stu-id="70b8f-107">Some filters can seek using other units of time as well, such as seeking to a particular frame number, or seeking to a given byte offset within a stream.</span></span> <span data-ttu-id="70b8f-108">Chacune de ces unités de temps est appelée un format d’heure et est définie par un identificateur global unique (GUID).</span><span class="sxs-lookup"><span data-stu-id="70b8f-108">Each of these time units is called a time format, and is defined by a globally unique identifier (GUID).</span></span> <span data-ttu-id="70b8f-109">Pour obtenir la liste des formats d’heure définis par DirectShow, consultez [**GUID Format GUID**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="70b8f-109">For a list of the time formats that are defined by DirectShow, see [**Time Format GUIDs**](time-format-guids.md).</span></span> <span data-ttu-id="70b8f-110">Les tiers peuvent également définir des GUID pour des formats d’heure personnalisés.</span><span class="sxs-lookup"><span data-stu-id="70b8f-110">Third parties can also define GUIDs for custom time formats.</span></span>

<span data-ttu-id="70b8f-111">Pour déterminer si les filtres actuellement dans le graphique de filtre prennent en charge un format d’heure particulier, appelez la méthode [**IMediaSeeking :: IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) .</span><span class="sxs-lookup"><span data-stu-id="70b8f-111">To determine whether the filters currently in the filter graph support a particular time format, call the [**IMediaSeeking::IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) method.</span></span> <span data-ttu-id="70b8f-112">La méthode retourne S \_ OK si le format est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="70b8f-112">The method returns S\_OK if the format is supported.</span></span> <span data-ttu-id="70b8f-113">Sinon, elle retourne S \_ false ou un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="70b8f-113">Otherwise, it returns S\_FALSE or an error code.</span></span> <span data-ttu-id="70b8f-114">Si un format est pris en charge, vous pouvez basculer vers ce format en appelant la méthode [**IMediaSeeking :: SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) .</span><span class="sxs-lookup"><span data-stu-id="70b8f-114">If a format is supported, you can switch to that format by calling the [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) method.</span></span> <span data-ttu-id="70b8f-115">Si la méthode **SetTimeFormat** est réussie, les commandes Seek suivantes sont exprimées à l’aide du nouveau format d’heure.</span><span class="sxs-lookup"><span data-stu-id="70b8f-115">If the **SetTimeFormat** method succeeds, subsequent seek commands are expressed using the new time format.</span></span>

<span data-ttu-id="70b8f-116">L’exemple suivant vérifie si le graphique prend en charge la recherche par numéro de frame.</span><span class="sxs-lookup"><span data-stu-id="70b8f-116">The follow example checks whether the graph supports seeking by frame number.</span></span> <span data-ttu-id="70b8f-117">Si c’est le cas, il cherche à tramer le numéro 20 :</span><span class="sxs-lookup"><span data-stu-id="70b8f-117">If so, it seeks to frame number 20:</span></span>


```C++
hr = pSeek->IsFormatSupported(&TIME_FORMAT_FRAME);
if (hr == S_OK)
{
    hr = pSeek->SetTimeFormat(&TIME_FORMAT_FRAME);
    if (SUCCEEDED(hr))
    {
        // Seek to frame number 20.
        LONGLONG rtNow = 20;
        hr = pSeek->SetPositions(
            &rtNow, AM_SEEKING_AbsolutePositioning, 
            0, AM_SEEKING_NoPositioning);
    }
}
```



<span data-ttu-id="70b8f-118">Notez que les formats d’heure s’appliquent uniquement aux commandes Seek.</span><span class="sxs-lookup"><span data-stu-id="70b8f-118">Note that time formats only apply to seek commands.</span></span> <span data-ttu-id="70b8f-119">Ils n’affectent pas la lecture des graphiques ou d’autres actions.</span><span class="sxs-lookup"><span data-stu-id="70b8f-119">They do not affect graph playback or other actions.</span></span>

 

 



