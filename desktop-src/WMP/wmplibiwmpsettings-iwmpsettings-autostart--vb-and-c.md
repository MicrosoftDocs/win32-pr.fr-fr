---
title: IWMPSettings propriété AutoStart
description: La propriété AutoStart obtient ou définit une valeur indiquant si l’élément multimédia actuel commence à être lu automatiquement.
ms.assetid: 01a1cb78-9951-478a-8ea3-1ae06164beab
keywords:
- propriété de démarrage automatique lecteur Windows Media
- propriété de démarrage automatique lecteur Windows Media, interface IWMPSettings
- Interface IWMPSettings lecteur Windows Media, propriété AutoStart
topic_type:
- apiref
api_name:
- IWMPSettings.autoStart
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaf6c1fb43107df11462737286e26fa7801360d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526571"
---
# <a name="iwmpsettingsautostart-property"></a><span data-ttu-id="0a6e8-106">IWMPSettings :: AutoStart, propriété</span><span class="sxs-lookup"><span data-stu-id="0a6e8-106">IWMPSettings::autoStart property</span></span>

<span data-ttu-id="0a6e8-107">La propriété **AutoStart** obtient ou définit une valeur indiquant si l’élément multimédia actuel commence à être lu automatiquement.</span><span class="sxs-lookup"><span data-stu-id="0a6e8-107">The **autoStart** property gets or sets a value indicating whether the current media item begins playing automatically.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a6e8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0a6e8-108">Syntax</span></span>


```CSharp
public System.Boolean autoStart {get; set;}
```


```VB

Public Property autoStart As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="0a6e8-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="0a6e8-109">Property value</span></span>

<span data-ttu-id="0a6e8-110">Valeur **System. Boolean** qui indique si l’élément multimédia actuel commence à être lu automatiquement.</span><span class="sxs-lookup"><span data-stu-id="0a6e8-110">A **System.Boolean** value that indicates whether the current media item begins playing automatically.</span></span> <span data-ttu-id="0a6e8-111">La valeur par défaut est **true**.</span><span class="sxs-lookup"><span data-stu-id="0a6e8-111">The default is **true**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a6e8-112">Notes</span><span class="sxs-lookup"><span data-stu-id="0a6e8-112">Remarks</span></span>

<span data-ttu-id="0a6e8-113">Si **AutoStart** est défini sur **true**, l’élément multimédia commence à s’exécuter quand **AxWindowsMediaPlayer. URL**, **AxWindowsMediaPlayer. currentPlaylist** ou **AxWindowsMediaPlayer. currentMedia** est défini.</span><span class="sxs-lookup"><span data-stu-id="0a6e8-113">If **autoStart** is set to **true**, the media item will begin playing when **AxWindowsMediaPlayer.URL**, **AxWindowsMediaPlayer.currentPlaylist**, or **AxWindowsMediaPlayer.currentMedia** is set.</span></span> <span data-ttu-id="0a6e8-114">Dans le cas contraire, l’élément multimédia ne démarre pas tant que la méthode **IWMPControls. Play** n’est pas appelée.</span><span class="sxs-lookup"><span data-stu-id="0a6e8-114">Otherwise, the media item will not start playing until the **IWMPControls.play** method is called.</span></span>

<span data-ttu-id="0a6e8-115">À moins que vous n’ayez défini **AutoStart** sur **true** juste avant de spécifier un élément multimédia, vous ne devez pas compter sur ce paramètre en remplacement de l’utilisation de la méthode **IWMPControls. Play** .</span><span class="sxs-lookup"><span data-stu-id="0a6e8-115">Unless you set **autoStart** to **true** immediately before specifying a media item, you should not rely on this setting as a substitute for using the **IWMPControls.play** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a6e8-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a6e8-116">Requirements</span></span>



| <span data-ttu-id="0a6e8-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0a6e8-117">Requirement</span></span> | <span data-ttu-id="0a6e8-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="0a6e8-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a6e8-119">Version</span><span class="sxs-lookup"><span data-stu-id="0a6e8-119">Version</span></span><br/>   | <span data-ttu-id="0a6e8-120">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="0a6e8-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="0a6e8-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0a6e8-121">Namespace</span></span><br/> | <span data-ttu-id="0a6e8-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="0a6e8-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="0a6e8-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="0a6e8-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="0a6e8-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="0a6e8-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a6e8-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a6e8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a6e8-126">**AxWindowsMediaPlayer. currentMedia (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="0a6e8-126">**AxWindowsMediaPlayer.currentMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0a6e8-127">**AxWindowsMediaPlayer. currentPlaylist (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="0a6e8-127">**AxWindowsMediaPlayer.currentPlaylist (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0a6e8-128">**AxWindowsMediaPlayer. URL (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="0a6e8-128">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0a6e8-129">**IWMPControls. Play (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="0a6e8-129">**IWMPControls.play (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0a6e8-130">**Interface IWMPSettings (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="0a6e8-130">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





