---
title: AxWindowsMediaPlayer. Close, méthode
description: La méthode Close ferme le fichier multimédia numérique en cours, arrête la lecture dans le lecteur Windows Media et libère les ressources du lecteur Windows Media.
ms.assetid: 3e555086-c31c-42d7-b671-0fd824f66641
keywords:
- méthode Close lecteur Windows Media
- méthode Close lecteur Windows Media, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer lecteur Windows Media, méthode Close
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.close
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1dc0c93e449e9ef1b00af7fb073068078f0fcc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535948"
---
# <a name="axwindowsmediaplayerclose-method"></a><span data-ttu-id="507ac-106">AxWindowsMediaPlayer. Close, méthode</span><span class="sxs-lookup"><span data-stu-id="507ac-106">AxWindowsMediaPlayer.close method</span></span>

<span data-ttu-id="507ac-107">La méthode Close ferme le fichier multimédia numérique en cours, arrête la lecture dans le lecteur Windows Media et libère les ressources du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="507ac-107">The close method closes the current digital media file, stops playback in Windows Media Player and releases Windows Media Player resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="507ac-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="507ac-108">Syntax</span></span>


```CSharp
public void close();
```


```VB

Public Sub close()
```





## <a name="parameters"></a><span data-ttu-id="507ac-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="507ac-109">Parameters</span></span>

<span data-ttu-id="507ac-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="507ac-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="507ac-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="507ac-111">Return value</span></span>

<span data-ttu-id="507ac-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="507ac-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="507ac-113">Notes</span><span class="sxs-lookup"><span data-stu-id="507ac-113">Remarks</span></span>

<span data-ttu-id="507ac-114">Cette méthode ferme le fichier multimédia numérique en cours, et non le lecteur Windows Media lui-même.</span><span class="sxs-lookup"><span data-stu-id="507ac-114">This method closes the current digital media file, not Windows Media Player itself.</span></span>

## <a name="examples"></a><span data-ttu-id="507ac-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="507ac-115">Examples</span></span>

<span data-ttu-id="507ac-116">L’exemple suivant crée un bouton qui, lorsque vous cliquez dessus, arrête la lecture dans le lecteur Windows Media et libère les ressources en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="507ac-116">The following example creates a button that, when clicked, stops playback in Windows Media Player and releases the resources in use.</span></span> <span data-ttu-id="507ac-117">L’objet AxWMPLib. AxWindowsMediaPlayer est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="507ac-117">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
private void closeIt_Click(object sender, System.EventArgs e)
{
    // Close the Player. 
    player.close();
}
```


```VB

Public Sub closeIt_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles closeIt.Click

    &#39; Close the Player. 
    player.close()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="507ac-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="507ac-118">Requirements</span></span>



| <span data-ttu-id="507ac-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="507ac-119">Requirement</span></span> | <span data-ttu-id="507ac-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="507ac-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="507ac-121">Version</span><span class="sxs-lookup"><span data-stu-id="507ac-121">Version</span></span><br/>   | <span data-ttu-id="507ac-122">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="507ac-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="507ac-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="507ac-123">Namespace</span></span><br/> | <span data-ttu-id="507ac-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="507ac-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="507ac-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="507ac-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="507ac-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="507ac-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="507ac-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="507ac-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="507ac-128">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="507ac-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





