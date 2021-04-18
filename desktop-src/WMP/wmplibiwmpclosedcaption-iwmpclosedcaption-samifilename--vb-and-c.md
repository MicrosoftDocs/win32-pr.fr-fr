---
title: IWMPClosedCaption propriété SAMIFileName
description: La propriété SAMIFileName obtient ou définit le nom d’un fichier contenant les informations nécessaires pour le sous-titrage.
ms.assetid: c3162c5f-9d66-41d4-920c-ed9840742d9d
keywords:
- Propriété SAMIFileName lecteur Windows Media
- Propriété SAMIFileName lecteur Windows Media, interface IWMPClosedCaption
- Interface IWMPClosedCaption lecteur Windows Media, propriété SAMIFileName
topic_type:
- apiref
api_name:
- IWMPClosedCaption.SAMIFileName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d251f2bbf0c8839ab9a0005c69e1869c47af16ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540515"
---
# <a name="iwmpclosedcaptionsamifilename-property"></a><span data-ttu-id="11a7b-106">IWMPClosedCaption :: SAMIFileName, propriété</span><span class="sxs-lookup"><span data-stu-id="11a7b-106">IWMPClosedCaption::SAMIFileName property</span></span>

<span data-ttu-id="11a7b-107">La propriété **SAMIFileName** obtient ou définit le nom d’un fichier contenant les informations nécessaires pour le sous-titrage.</span><span class="sxs-lookup"><span data-stu-id="11a7b-107">The **SAMIFileName** property gets or sets the name of a file containing the information needed for closed captioning.</span></span>

## <a name="syntax"></a><span data-ttu-id="11a7b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="11a7b-108">Syntax</span></span>


```CSharp
public System.String SAMIFileName {get; set;}
```


```VB

Public Property SAMIFileName As System.String
```





## <a name="property-value"></a><span data-ttu-id="11a7b-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="11a7b-109">Property value</span></span>

<span data-ttu-id="11a7b-110">**System. String** qui est le nom du fichier sami (Synchronized Accessible Media Interchange).</span><span class="sxs-lookup"><span data-stu-id="11a7b-110">The **System.String** that is the name of the Synchronized Accessible Media Interchange (SAMI) file.</span></span>

## <a name="remarks"></a><span data-ttu-id="11a7b-111">Notes</span><span class="sxs-lookup"><span data-stu-id="11a7b-111">Remarks</span></span>

<span data-ttu-id="11a7b-112">Le fichier SAMI doit utiliser une extension de nom de fichier. SMI ou. sami.</span><span class="sxs-lookup"><span data-stu-id="11a7b-112">The SAMI file must use an .smi or .sami file name extension.</span></span>

<span data-ttu-id="11a7b-113">Si vous ne définissez pas de valeur à l’aide de **SAMIFileName**, cette propriété obtient une **chaîne** contenant le nom de fichier ou l’URL par défaut associés à l’élément multimédia en cours.</span><span class="sxs-lookup"><span data-stu-id="11a7b-113">If you do not set a value using **SAMIFileName**, this property gets a **string** containing the default file name or URL associated with the current media item.</span></span> <span data-ttu-id="11a7b-114">Cette association peut se produire lorsqu’un fichier SAMI est spécifié à l’aide du paramètre d’URL *sami* , ou automatiquement lorsque le fichier sami porte le même nom que le fichier multimédia numérique (à l’exception de l’extension de nom de fichier).</span><span class="sxs-lookup"><span data-stu-id="11a7b-114">This association can occur when a SAMI file is specified by using the *sami* URL parameter, or automatically when the SAMI file has the same name as the digital media file (except for the file name extension).</span></span> <span data-ttu-id="11a7b-115">Si aucun fichier SAMI par défaut n’est associé au média actuel, cette propriété obtient une chaîne de longueur nulle ("").</span><span class="sxs-lookup"><span data-stu-id="11a7b-115">If there is no default SAMI file associated with the current media, this property gets a zero-length string ("").</span></span>

<span data-ttu-id="11a7b-116">Une fois que vous avez défini une valeur à l’aide de **SAMIFileName**, cette valeur persiste jusqu’à ce que vous ayez défini une nouvelle valeur (ou jusqu’à ce qu’un nouvel élément multimédia soit ouvert à l’aide du paramètre URL sami).</span><span class="sxs-lookup"><span data-stu-id="11a7b-116">Once you set a value using **SAMIFileName**, that value persists until you set a new value (or until a new media item is opened using the sami URL parameter).</span></span> <span data-ttu-id="11a7b-117">Par conséquent, vous devez définir une nouvelle valeur pour cette propriété avant de lire chaque nouvel élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="11a7b-117">Therefore, you must set a new value for this property before you play each new media item.</span></span> <span data-ttu-id="11a7b-118">De cette façon, la nouvelle valeur pour **SAMIFileName** prend effet lors de l’ouverture de l’élément multimédia suivant (ou lors de l’appel de **AxWindowsMediaPlayer. Close** ).</span><span class="sxs-lookup"><span data-stu-id="11a7b-118">That way, the new value for **SAMIFileName** will take effect when the next media item is opened (or when **AxWindowsMediaPlayer.close** is called).</span></span> <span data-ttu-id="11a7b-119">La spécification d’une nouvelle valeur pour **SAMIFileName** n’a aucun effet sur le média actuel.</span><span class="sxs-lookup"><span data-stu-id="11a7b-119">Specifying a new value for **SAMIFileName** has no effect for the current media.</span></span>

<span data-ttu-id="11a7b-120">Pour faire en sorte que le lecteur Windows Media utilise le fichier SAMI par défaut associé à un élément multimédia particulier, définissez **SAMIFileName** sur une chaîne de longueur nulle ("") avant de lire l’élément multimédia suivant.</span><span class="sxs-lookup"><span data-stu-id="11a7b-120">To cause Windows Media Player to use the default SAMI file associated with a particular media item, set **SAMIFileName** to a zero-length string ("") before you play the next media item.</span></span>

## <a name="requirements"></a><span data-ttu-id="11a7b-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="11a7b-121">Requirements</span></span>



| <span data-ttu-id="11a7b-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="11a7b-122">Requirement</span></span> | <span data-ttu-id="11a7b-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="11a7b-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11a7b-124">Version</span><span class="sxs-lookup"><span data-stu-id="11a7b-124">Version</span></span><br/>   | <span data-ttu-id="11a7b-125">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="11a7b-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="11a7b-126">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="11a7b-126">Namespace</span></span><br/> | <span data-ttu-id="11a7b-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="11a7b-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="11a7b-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="11a7b-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="11a7b-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="11a7b-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11a7b-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="11a7b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11a7b-131">**Ajout de sous-titres à des médias numériques**</span><span class="sxs-lookup"><span data-stu-id="11a7b-131">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="11a7b-132">**AxWindowsMediaPlayer. Close**</span><span class="sxs-lookup"><span data-stu-id="11a7b-132">**AxWindowsMediaPlayer.close**</span></span>](axwmplib-axwindowsmediaplayer-close.md)
</dt> <dt>

[<span data-ttu-id="11a7b-133">**Interface IWMPClosedCaption (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="11a7b-133">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="11a7b-134">**Interface IWMPClosedCaption2 (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="11a7b-134">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





