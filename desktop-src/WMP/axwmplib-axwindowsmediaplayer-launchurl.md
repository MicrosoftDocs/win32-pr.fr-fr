---
title: Méthode AxWindowsMediaPlayer. launchURL
description: La méthode launchURL envoie une URL au navigateur par défaut de l’utilisateur à restituer. | Méthode AxWindowsMediaPlayer. launchURL
ms.assetid: 3e8dfdbb-b5ad-44ea-97a6-e860386b7fb4
keywords:
- méthode launchURL lecteur Windows Media
- méthode launchURL lecteur Windows Media, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer lecteur Windows Media, méthode launchURL
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.launchURL
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27fe8e544bb14b119785b26b9cb5be5cdad48015
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541599"
---
# <a name="axwindowsmediaplayerlaunchurl-method"></a><span data-ttu-id="79ae2-107">Méthode AxWindowsMediaPlayer. launchURL</span><span class="sxs-lookup"><span data-stu-id="79ae2-107">AxWindowsMediaPlayer.launchURL method</span></span>

<span data-ttu-id="79ae2-108">La méthode launchURL envoie une URL au navigateur par défaut de l’utilisateur à restituer.</span><span class="sxs-lookup"><span data-stu-id="79ae2-108">The launchURL method sends a URL to the user's default browser to be rendered.</span></span>

## <a name="syntax"></a><span data-ttu-id="79ae2-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="79ae2-109">Syntax</span></span>


```CSharp
public void launchURL(
  System.String bstrURL
);
```


```VB

Public Sub launchURL( _
  ByVal bstrURL As System.String _
)
```





## <a name="parameters"></a><span data-ttu-id="79ae2-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="79ae2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79ae2-111">*bstrURL*</span><span class="sxs-lookup"><span data-stu-id="79ae2-111">*bstrURL*</span></span> 
</dt> <dd>

<span data-ttu-id="79ae2-112">**System. String** qui correspond à l’URL à lancer.</span><span class="sxs-lookup"><span data-stu-id="79ae2-112">The **System.String** that is the URL to launch.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79ae2-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="79ae2-113">Return value</span></span>

<span data-ttu-id="79ae2-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="79ae2-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="79ae2-115">Notes</span><span class="sxs-lookup"><span data-stu-id="79ae2-115">Remarks</span></span>

<span data-ttu-id="79ae2-116">Cette méthode ouvre uniquement les pages Web à l’aide des protocoles HTTP ou HTTPs.</span><span class="sxs-lookup"><span data-stu-id="79ae2-116">This method only opens webpages using the HTTP or HTTPS protocols.</span></span>

## <a name="examples"></a><span data-ttu-id="79ae2-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="79ae2-117">Examples</span></span>

<span data-ttu-id="79ae2-118">L’exemple suivant crée un bouton qui, lorsque vous cliquez dessus, affiche le site Web Microsoft dans une nouvelle fenêtre de navigateur.</span><span class="sxs-lookup"><span data-stu-id="79ae2-118">The following example creates a button that, when clicked, displays the Microsoft website in a new browser window.</span></span> <span data-ttu-id="79ae2-119">L’objet AxWMPLib. AxWindowsMediaPlayer est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="79ae2-119">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
private void goToMS_Click(object sender, System.EventArgs e)
{
    // Open the Microsoft website. 
    player.launchURL("https://www.microsoft.com");
}
```


```VB

Public Sub goToMS_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles goToMS.Click

    &#39; Open the Microsoft website. 
    player.launchURL(&quot;https://www.microsoft.com&quot;)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="79ae2-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="79ae2-120">Requirements</span></span>



| <span data-ttu-id="79ae2-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="79ae2-121">Requirement</span></span> | <span data-ttu-id="79ae2-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="79ae2-122">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79ae2-123">Version</span><span class="sxs-lookup"><span data-stu-id="79ae2-123">Version</span></span><br/>   | <span data-ttu-id="79ae2-124">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="79ae2-124">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="79ae2-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="79ae2-125">Namespace</span></span><br/> | <span data-ttu-id="79ae2-126">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="79ae2-126">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="79ae2-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="79ae2-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="79ae2-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="79ae2-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79ae2-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79ae2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79ae2-130">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="79ae2-130">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





