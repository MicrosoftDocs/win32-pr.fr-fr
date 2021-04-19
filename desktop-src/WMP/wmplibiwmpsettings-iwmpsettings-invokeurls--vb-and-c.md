---
title: IWMPSettings propriété invokeURLs
description: La propriété invokeURLs obtient ou définit une valeur indiquant si les événements d’URL doivent lancer un navigateur Web.
ms.assetid: e16c968d-a1b7-4c3a-9c1a-5748ed44cdac
keywords:
- propriété invokeURLs lecteur Windows Media
- propriété invokeURLs lecteur Windows Media, interface IWMPSettings
- Interface IWMPSettings lecteur Windows Media, propriété invokeURLs
topic_type:
- apiref
api_name:
- IWMPSettings.invokeURLs
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbdd68d797b54f4e9365f381b2b5c705dffc419b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530367"
---
# <a name="iwmpsettingsinvokeurls-property"></a><span data-ttu-id="e5b11-106">IWMPSettings :: invokeURLs, propriété</span><span class="sxs-lookup"><span data-stu-id="e5b11-106">IWMPSettings::invokeURLs property</span></span>

<span data-ttu-id="e5b11-107">La propriété **invokeURLs** obtient ou définit une valeur indiquant si les événements d’URL doivent lancer un navigateur Web.</span><span class="sxs-lookup"><span data-stu-id="e5b11-107">The **invokeURLs** property gets or sets a value indicating whether URL events should launch a Web browser.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5b11-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e5b11-108">Syntax</span></span>


```CSharp
public System.Boolean invokeURLs {get; set;}
```


```VB

Public Property invokeURLs As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="e5b11-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="e5b11-109">Property value</span></span>

<span data-ttu-id="e5b11-110">Valeur **System. Boolean** indiquant si les événements d’URL doivent lancer un navigateur Web.</span><span class="sxs-lookup"><span data-stu-id="e5b11-110">A **System.Boolean** value indicating whether URL events should launch a Web browser.</span></span> <span data-ttu-id="e5b11-111">La valeur par défaut est **true**.</span><span class="sxs-lookup"><span data-stu-id="e5b11-111">The default is **true**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5b11-112">Notes</span><span class="sxs-lookup"><span data-stu-id="e5b11-112">Remarks</span></span>

<span data-ttu-id="e5b11-113">Les fichiers multimédias numériques et les flux peuvent contenir des commandes de script d’URL.</span><span class="sxs-lookup"><span data-stu-id="e5b11-113">Digital media files and streams can contain URL script commands.</span></span> <span data-ttu-id="e5b11-114">Lorsqu’une commande de script d’URL est envoyée au contrôle du lecteur Windows Media, elle est d’abord transmise au gestionnaire d’événements **\_ \_ ScriptCommandEvent AxWindowsMediaPlayer WMPOCXEvents** , quelle que soit la valeur récupérée par **invokeURLs**.</span><span class="sxs-lookup"><span data-stu-id="e5b11-114">When a URL script command is sent to the Windows Media Player control, it is passed first to the **AxWindowsMediaPlayer\_WMPOCXEvents\_ScriptCommandEvent** event handler regardless of the value retrieved by **invokeURLs**.</span></span> <span data-ttu-id="e5b11-115">Après la sortie de **\_ WMPOCXEvents \_ ScriptCommandEvent** , le lecteur Windows Media vérifie **invokeURLs** pour déterminer s’il faut lancer le navigateur Web par défaut avec l’URL.</span><span class="sxs-lookup"><span data-stu-id="e5b11-115">After **\_WMPOCXEvents\_ScriptCommandEvent** exits, Windows Media Player checks **invokeURLs** to determine whether to launch the default Web browser with the URL.</span></span> <span data-ttu-id="e5b11-116">Vous pouvez afficher des URL de manière sélective en les vérifiant dans **\_ WMPOCXEvents \_ ScriptCommandEvent** et en définissant **invokeURLs** comme vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="e5b11-116">You can selectively display URLs by checking them in **\_WMPOCXEvents\_ScriptCommandEvent** and setting **invokeURLs** as desired.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5b11-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e5b11-117">Requirements</span></span>



| <span data-ttu-id="e5b11-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e5b11-118">Requirement</span></span> | <span data-ttu-id="e5b11-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="e5b11-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5b11-120">Version</span><span class="sxs-lookup"><span data-stu-id="e5b11-120">Version</span></span><br/>   | <span data-ttu-id="e5b11-121">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="e5b11-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="e5b11-122">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e5b11-122">Namespace</span></span><br/> | <span data-ttu-id="e5b11-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="e5b11-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="e5b11-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="e5b11-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e5b11-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e5b11-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5b11-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5b11-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5b11-127">**Événement AxWindowsMediaPlayer. commande (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="e5b11-127">**AxWindowsMediaPlayer.ScriptCommand Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="e5b11-128">**Interface IWMPSettings (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="e5b11-128">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





