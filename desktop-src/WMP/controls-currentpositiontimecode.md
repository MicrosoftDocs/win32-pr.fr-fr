---
title: Controls. currentPositionTimecode
description: La propriété currentPositionTimecode spécifie ou récupère la position actuelle dans l’élément multimédia actuel à l’aide d’un format de code d’heure. Cette propriété prend actuellement en charge le code de temps SMPTE.
ms.assetid: 98d79756-c6cf-4dbc-936a-58229452451c
keywords:
- Controls. currentPositionTimecode Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentPositionTimecode
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e2a4ddeb0849a829ff7a16fd80ff4891cfe56c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528779"
---
# <a name="controlscurrentpositiontimecode"></a><span data-ttu-id="8c6ae-105">Controls. currentPositionTimecode</span><span class="sxs-lookup"><span data-stu-id="8c6ae-105">Controls.currentPositionTimecode</span></span>

<span data-ttu-id="8c6ae-106">La propriété **currentPositionTimecode** spécifie ou récupère la position actuelle dans l’élément multimédia actuel à l’aide d’un format de code d’heure.</span><span class="sxs-lookup"><span data-stu-id="8c6ae-106">The **currentPositionTimecode** property specifies or retrieves the current position in the current media item using a time code format.</span></span> <span data-ttu-id="8c6ae-107">Cette propriété prend actuellement en charge le code de temps SMPTE.</span><span class="sxs-lookup"><span data-stu-id="8c6ae-107">This property currently supports SMPTE time code.</span></span>

``` syntax
player.controls.currentPositionTimecode
      
```

## <a name="possible-values"></a><span data-ttu-id="8c6ae-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="8c6ae-108">Possible Values</span></span>

<span data-ttu-id="8c6ae-109">Cette propriété est une **chaîne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="8c6ae-109">This property is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c6ae-110">Notes</span><span class="sxs-lookup"><span data-stu-id="8c6ae-110">Remarks</span></span>

<span data-ttu-id="8c6ae-111">Le code temporel SMPTE offre un moyen standard d’identifier une image vidéo individuelle, ce qui est utile pour synchroniser la lecture.</span><span class="sxs-lookup"><span data-stu-id="8c6ae-111">SMPTE time code provides a standard way of identifying an individual video frame, which is useful for synchronizing playback.</span></span> <span data-ttu-id="8c6ae-112">Si un fichier multimédia numérique prend en charge le code temporel SMPTE, le lecteur Windows Media peut récupérer les informations de position du code en temps courant ou rechercher une image vidéo identifiée par une **chaîne** de code d’heure particulière.</span><span class="sxs-lookup"><span data-stu-id="8c6ae-112">If a digital media file supports SMPTE time code, Windows Media Player can retrieve the current time code position information or seek to a video frame identified by a particular time code **String**.</span></span>

<span data-ttu-id="8c6ae-113">Le code temporel SMPTE identifie une trame particulière en fonction du nombre d’heures, de minutes, de secondes et de frames qui le séparent d’une trame de référence particulière.</span><span class="sxs-lookup"><span data-stu-id="8c6ae-113">SMPTE time code identifies a particular frame by the number of hours, minutes, seconds, and frames that separate it from a particular reference frame the frame designated as time zero.</span></span> <span data-ttu-id="8c6ae-114">En règle générale, la trame de temps zéro est le début du fichier et une valeur de code temporel SMPTE particulière représente le temps écoulé depuis le début du fichier.</span><span class="sxs-lookup"><span data-stu-id="8c6ae-114">Usually the time zero frame is the start of the file and a particular SMPTE time code value represents the elapsed time since the start of the file.</span></span>

<span data-ttu-id="8c6ae-115">La **chaîne** de code d’heure est au \[ *format* \] *hh*:*mm*:*SS*.*FF* où \[ *Range* \] représente la plage, *hh* représente les heures, *mm* représente les minutes, *SS* représente les secondes et *FF* représente les images.</span><span class="sxs-lookup"><span data-stu-id="8c6ae-115">The time code **String** is in the format \[*range*\]*hh*:*mm*:*ss*.*ff* where \[*range*\] represents the range, *hh* represents hours, *mm* represents minutes, *ss* represents seconds, and *ff* represents frames.</span></span> <span data-ttu-id="8c6ae-116">Lorsque vous spécifiez une valeur à l’aide de **currentPositionTimecode**, vous devez inclure les huit chiffres en utilisant des zéros comme espaces réservés.</span><span class="sxs-lookup"><span data-stu-id="8c6ae-116">When specifying a value using **currentPositionTimecode**, you must include all eight digits using zeros as placeholders.</span></span>

<span data-ttu-id="8c6ae-117">Le \[  \] spécificateur de plage correspond au membre **wRange** de la structure de données d' **\_ extension du \_ \_ code temporel WMT** Windows Media format.</span><span class="sxs-lookup"><span data-stu-id="8c6ae-117">The \[*range*\] specifier corresponds to the **wRange** member of the Windows Media Format **WMT\_TIMECODE\_EXTENSION\_DATA** structure.</span></span> <span data-ttu-id="8c6ae-118">Pour plus d’informations sur les plages de codes de temps, consultez le kit de développement logiciel (SDK) Windows Media format.</span><span class="sxs-lookup"><span data-stu-id="8c6ae-118">For more information about time code ranges, see the Windows Media Format SDK.</span></span>

<span data-ttu-id="8c6ae-119">La spécification et la récupération de **currentPositionTimecode** sont prises en charge uniquement pour les fichiers qui contiennent des informations de code de temps SMPTE.</span><span class="sxs-lookup"><span data-stu-id="8c6ae-119">Specifying and retrieving **currentPositionTimecode** is only supported for files that contain SMPTE time code information.</span></span>

## <a name="examples"></a><span data-ttu-id="8c6ae-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="8c6ae-120">Examples</span></span>

<span data-ttu-id="8c6ae-121">L’exemple de code suivant spécifie **currentPositionTimecode** comme 1 heure, zéro minute, 30 secondes et 5 frames.</span><span class="sxs-lookup"><span data-stu-id="8c6ae-121">The following code example specifies **currentPositionTimecode** as 1 hour, zero minutes, 30 seconds, and 5 frames.</span></span> <span data-ttu-id="8c6ae-122">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="8c6ae-122">The **Player** object was created with ID = "Player".</span></span>


```
// Seek to a frame using SMPTE time code.
Player.controls.currentPositionTimecode = "[00000]01:00:30.05";

```



## <a name="requirements"></a><span data-ttu-id="8c6ae-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c6ae-123">Requirements</span></span>



| <span data-ttu-id="8c6ae-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8c6ae-124">Requirement</span></span> | <span data-ttu-id="8c6ae-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c6ae-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8c6ae-126">Version</span><span class="sxs-lookup"><span data-stu-id="8c6ae-126">Version</span></span><br/> | <span data-ttu-id="8c6ae-127">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="8c6ae-127">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="8c6ae-128">DLL</span><span class="sxs-lookup"><span data-stu-id="8c6ae-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="8c6ae-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c6ae-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c6ae-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c6ae-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c6ae-131">**Controls (objet)**</span><span class="sxs-lookup"><span data-stu-id="8c6ae-131">**Controls Object**</span></span>](controls-object.md)
</dt> </dl>

 

 





