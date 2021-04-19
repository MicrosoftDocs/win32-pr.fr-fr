---
title: IWMPControls3 propriété currentPositionTimecode
description: La propriété currentPositionTimecode obtient ou définit la position actuelle dans l’élément multimédia actuel à l’aide d’un format de code d’heure. Cette propriété prend actuellement en charge le code de temps SMPTE.
ms.assetid: 035b812c-e976-4b4e-b4e5-820653257732
keywords:
- propriété currentPositionTimecode lecteur Windows Media
- propriété currentPositionTimecode lecteur Windows Media, interface IWMPControls3
- Interface IWMPControls3 lecteur Windows Media, propriété currentPositionTimecode
topic_type:
- apiref
api_name:
- IWMPControls3.currentPositionTimecode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7660e6dc2690c310cf06f64e38190dc1cb3f24ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544047"
---
# <a name="iwmpcontrols3currentpositiontimecode-property"></a><span data-ttu-id="cb034-107">IWMPControls3 :: currentPositionTimecode, propriété</span><span class="sxs-lookup"><span data-stu-id="cb034-107">IWMPControls3::currentPositionTimecode property</span></span>

<span data-ttu-id="cb034-108">La propriété **currentPositionTimecode** obtient ou définit la position actuelle dans l’élément multimédia actuel à l’aide d’un format de code d’heure.</span><span class="sxs-lookup"><span data-stu-id="cb034-108">The **currentPositionTimecode** property gets or sets the current position in the current media item using a time code format.</span></span> <span data-ttu-id="cb034-109">Cette propriété prend actuellement en charge le code de temps SMPTE.</span><span class="sxs-lookup"><span data-stu-id="cb034-109">This property currently supports SMPTE time code.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb034-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cb034-110">Syntax</span></span>


```CSharp
public System.String currentPositionTimecode {get; set;}
```


```VB

Public Property currentPositionTimecode As System.String
```





## <a name="property-value"></a><span data-ttu-id="cb034-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="cb034-111">Property value</span></span>

<span data-ttu-id="cb034-112">**System. String** qui est le code de temps SMPTE.</span><span class="sxs-lookup"><span data-stu-id="cb034-112">A **System.String** that is the SMPTE time code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb034-113">Notes</span><span class="sxs-lookup"><span data-stu-id="cb034-113">Remarks</span></span>

<span data-ttu-id="cb034-114">Le code temporel SMPTE offre un moyen standard d’identifier une image vidéo individuelle, ce qui est utile pour synchroniser la lecture.</span><span class="sxs-lookup"><span data-stu-id="cb034-114">SMPTE time code provides a standard way of identifying an individual video frame, which is useful for synchronizing playback.</span></span> <span data-ttu-id="cb034-115">Si un fichier multimédia numérique prend en charge le code temporel SMPTE, le lecteur Windows Media peut récupérer les informations de position du code en temps courant ou rechercher une image vidéo identifiée par un code de temps particulier.</span><span class="sxs-lookup"><span data-stu-id="cb034-115">If a digital media file supports SMPTE time code, Windows Media Player can retrieve the current time code position information or seek to a video frame identified by a particular time code.</span></span>

<span data-ttu-id="cb034-116">Le code temporel SMPTE identifie une trame particulière en fonction du nombre d’heures, de minutes, de secondes et de frames qui le séparent d’une trame de référence particulière.</span><span class="sxs-lookup"><span data-stu-id="cb034-116">SMPTE time code identifies a particular frame by the number of hours, minutes, seconds, and frames that separate it from a particular reference frame the frame designated as time zero.</span></span> <span data-ttu-id="cb034-117">En règle générale, la trame de temps zéro est le début du fichier et une valeur de code temporel SMPTE particulière représente le temps écoulé depuis le début du fichier.</span><span class="sxs-lookup"><span data-stu-id="cb034-117">Usually the time zero frame is the start of the file and a particular SMPTE time code value represents the elapsed time since the start of the file.</span></span>

<span data-ttu-id="cb034-118">Le code d’heure est au format \[  \] *hh*:*mm*:*SS*.*FF* où \[ *Range* \] représente la plage, HH représente les heures, *mm* représente les minutes, *SS* représente les secondes et *FF* représente les images.</span><span class="sxs-lookup"><span data-stu-id="cb034-118">The time code is in the format \[*range*\]*hh*:*mm*:*ss*.*ff* where \[*range*\] represents the range, hh represents hours, *mm* represents minutes, *ss* represents seconds, and *ff* represents frames.</span></span> <span data-ttu-id="cb034-119">Lorsque vous définissez une valeur pour **currentPositionTimecode**, vous devez inclure les huit chiffres, en utilisant des zéros comme espaces réservés.</span><span class="sxs-lookup"><span data-stu-id="cb034-119">When setting a value for **currentPositionTimecode**, you must include all eight digits, using zeros as placeholders.</span></span>

<span data-ttu-id="cb034-120">\[*plage* \] correspond au membre **wRange** de la structure de données d' **\_ extension du \_ code \_ temporel WMT** Windows Media format.</span><span class="sxs-lookup"><span data-stu-id="cb034-120">\[*range*\] corresponds to the **wRange** member of the Windows Media Format **WMT\_TIMECODE\_EXTENSION\_DATA** structure.</span></span> <span data-ttu-id="cb034-121">Pour plus d’informations sur les plages de codes de temps, consultez le kit de développement logiciel (SDK) Windows Media format.</span><span class="sxs-lookup"><span data-stu-id="cb034-121">For more information about time code ranges, see the Windows Media Format SDK.</span></span>

<span data-ttu-id="cb034-122">La définition et l’obtention de **currentPositionTimecode** sont prises en charge uniquement pour les fichiers qui contiennent des informations de code de temps SMPTE.</span><span class="sxs-lookup"><span data-stu-id="cb034-122">Setting and getting **currentPositionTimecode** is supported only for files that contain SMPTE time code information.</span></span>

## <a name="examples"></a><span data-ttu-id="cb034-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="cb034-123">Examples</span></span>

<span data-ttu-id="cb034-124">L’exemple de code suivant spécifie **currentPositionTimecode** comme 1 heure, zéro minute, 30 secondes et 5 frames.</span><span class="sxs-lookup"><span data-stu-id="cb034-124">The following code example specifies **currentPositionTimecode** as 1 hour, zero minutes, 30 seconds, and 5 frames.</span></span> <span data-ttu-id="cb034-125">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="cb034-125">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Cast the interface returned by player.Ctlcontrols to an IWMPControls3 interface
// so that you can use the currentPositionTimecode property.
WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

// Seek to a frame using SMPTE time code.
controls.currentPositionTimecode = "[00000]01:00:30.05";
```


```VB

' Cast the interface returned by player.Ctlcontrols to an IWMPControls3 interface
&#39; so that you can use the currentPositionTimecode property.
Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

&#39; Seek to a frame using SMPTE time code.
Controls.currentPositionTimecode = &quot;[00000]01:00:30.05&quot;
```





## <a name="requirements"></a><span data-ttu-id="cb034-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cb034-126">Requirements</span></span>



| <span data-ttu-id="cb034-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cb034-127">Requirement</span></span> | <span data-ttu-id="cb034-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb034-128">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb034-129">Version</span><span class="sxs-lookup"><span data-stu-id="cb034-129">Version</span></span><br/>   | <span data-ttu-id="cb034-130">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="cb034-130">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="cb034-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="cb034-131">Namespace</span></span><br/> | <span data-ttu-id="cb034-132">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="cb034-132">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="cb034-133">Assembly</span><span class="sxs-lookup"><span data-stu-id="cb034-133">Assembly</span></span><br/>  | <dl> <span data-ttu-id="cb034-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="cb034-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb034-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb034-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb034-136">**Interface IWMPControls3 (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="cb034-136">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





