---
title: IWMPSettings propriété defaultFrame
description: La propriété defaultFrame obtient ou définit le nom du frame utilisé pour afficher une URL qui est reçue dans un \_ \_ événement ScriptCommandEvent WMPOCXEvents.
ms.assetid: 92c775ac-5ff1-4d21-b21d-491bc48a033f
keywords:
- propriété defaultFrame lecteur Windows Media
- propriété defaultFrame lecteur Windows Media, interface IWMPSettings
- Interface IWMPSettings lecteur Windows Media, propriété defaultFrame
topic_type:
- apiref
api_name:
- IWMPSettings.defaultFrame
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28539640214165ab5b2808762ed854b19b434311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525398"
---
# <a name="iwmpsettingsdefaultframe-property"></a><span data-ttu-id="ac3be-106">IWMPSettings ::d propriété efaultFrame</span><span class="sxs-lookup"><span data-stu-id="ac3be-106">IWMPSettings::defaultFrame property</span></span>

<span data-ttu-id="ac3be-107">La propriété **defaultFrame** obtient ou définit le nom du frame utilisé pour afficher une URL qui est reçue dans un événement **\_ ScriptCommandEvent WMPOCXEvents \_** .</span><span class="sxs-lookup"><span data-stu-id="ac3be-107">The **defaultFrame** property gets or sets the name of the frame used to display a URL that is received in an **AxWindowsMediaPlayer\_WMPOCXEvents\_ScriptCommandEvent** event.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac3be-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ac3be-108">Syntax</span></span>


```CSharp
public System.String defaultFrame {get; set;}
```


```VB

Public Property defaultFrame As System.String
```





## <a name="property-value"></a><span data-ttu-id="ac3be-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="ac3be-109">Property value</span></span>

<span data-ttu-id="ac3be-110">**System. String** qui est la valeur de l’attribut Name de l’élément **Frame** cible.</span><span class="sxs-lookup"><span data-stu-id="ac3be-110">A **System.String** that is the value of the name attribute of the target **FRAME** element.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac3be-111">Notes</span><span class="sxs-lookup"><span data-stu-id="ac3be-111">Remarks</span></span>

<span data-ttu-id="ac3be-112">Si un frame cible est spécifié dans l’événement **\_ WMPOCXEvents \_ ScriptCommandEvent** lui-même, cette propriété est ignorée.</span><span class="sxs-lookup"><span data-stu-id="ac3be-112">If a target frame is specified in the **\_WMPOCXEvents\_ScriptCommandEvent** event itself, this property is ignored.</span></span>

<span data-ttu-id="ac3be-113">Cette propriété est ignorée lors de l’utilisation de l’applet Java de Netscape Navigator.</span><span class="sxs-lookup"><span data-stu-id="ac3be-113">This property is ignored when using the Netscape Navigator Java applet.</span></span> <span data-ttu-id="ac3be-114">Dans Netscape Navigator, chaque commande de script d’URL reçue affiche l’URL dans une nouvelle fenêtre de navigateur, quelle que soit la valeur de **defaultFrame**.</span><span class="sxs-lookup"><span data-stu-id="ac3be-114">In Netscape Navigator, each URL script command received will display the URL in a new browser window, regardless of the value of **defaultFrame**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac3be-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ac3be-115">Requirements</span></span>



| <span data-ttu-id="ac3be-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ac3be-116">Requirement</span></span> | <span data-ttu-id="ac3be-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac3be-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac3be-118">Version</span><span class="sxs-lookup"><span data-stu-id="ac3be-118">Version</span></span><br/>   | <span data-ttu-id="ac3be-119">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="ac3be-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="ac3be-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ac3be-120">Namespace</span></span><br/> | <span data-ttu-id="ac3be-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="ac3be-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="ac3be-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="ac3be-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ac3be-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ac3be-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac3be-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac3be-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac3be-125">**Événement AxWindowsMediaPlayer. commande (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="ac3be-125">**AxWindowsMediaPlayer.ScriptCommand Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="ac3be-126">**Interface IWMPSettings (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="ac3be-126">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





