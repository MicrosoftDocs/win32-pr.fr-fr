---
title: Méthode AxWindowsMediaPlayer. newMedia
description: La méthode newMedia retourne une interface IWMPMedia pour un nouvel élément multimédia.
ms.assetid: d10a517e-b4da-4f0b-9d51-9d387578d7dd
keywords:
- méthode newMedia lecteur Windows Media
- méthode newMedia lecteur Windows Media, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer lecteur Windows Media, méthode newMedia
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.newMedia
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 093a4e2b8181aac9148686108ad2c5c318a4d0cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540333"
---
# <a name="axwindowsmediaplayernewmedia-method"></a><span data-ttu-id="4da00-106">Méthode AxWindowsMediaPlayer. newMedia</span><span class="sxs-lookup"><span data-stu-id="4da00-106">AxWindowsMediaPlayer.newMedia method</span></span>

<span data-ttu-id="4da00-107">La méthode newMedia retourne une interface IWMPMedia pour un nouvel élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="4da00-107">The newMedia method returns an IWMPMedia interface for a new media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="4da00-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4da00-108">Syntax</span></span>


```CSharp
public IWMPMedia newMedia(
  System.String bstrURL
);
```


```VB

Public Function newMedia( _
  ByVal bstrURL As System.String _
) As IWMPMedia
```





## <a name="parameters"></a><span data-ttu-id="4da00-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4da00-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4da00-110">*bstrURL*</span><span class="sxs-lookup"><span data-stu-id="4da00-110">*bstrURL*</span></span> 
</dt> <dd>

<span data-ttu-id="4da00-111">**System. String** qui est l’URL du fichier multimédia numérique utilisé pour initialiser le nouvel élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="4da00-111">A **System.String** that is the URL of the digital media file that is used to initialize the new media item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4da00-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4da00-112">Return value</span></span>

<span data-ttu-id="4da00-113">Interface WMPLib. IWMPMedia qui représente l’élément multimédia nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="4da00-113">A WMPLib.IWMPMedia interface that represents the newly created media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="4da00-114">Notes</span><span class="sxs-lookup"><span data-stu-id="4da00-114">Remarks</span></span>

<span data-ttu-id="4da00-115">Le paramètre *du bstrURL* ne doit pas être une chaîne de longueur nulle ("") ou null.</span><span class="sxs-lookup"><span data-stu-id="4da00-115">The *bstrURL* parameter must not be a zero-length string ("") or null.</span></span>

## <a name="requirements"></a><span data-ttu-id="4da00-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4da00-116">Requirements</span></span>



| <span data-ttu-id="4da00-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4da00-117">Requirement</span></span> | <span data-ttu-id="4da00-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="4da00-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4da00-119">Version</span><span class="sxs-lookup"><span data-stu-id="4da00-119">Version</span></span><br/>   | <span data-ttu-id="4da00-120">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="4da00-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="4da00-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4da00-121">Namespace</span></span><br/> | <span data-ttu-id="4da00-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="4da00-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="4da00-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="4da00-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4da00-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4da00-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4da00-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4da00-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4da00-126">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="4da00-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4da00-127">**Interface IWMPMedia (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="4da00-127">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





