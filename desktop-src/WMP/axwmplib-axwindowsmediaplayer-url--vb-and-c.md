---
title: AxWindowsMediaPlayer. URL (propriété)
description: La propriété URL obtient ou définit le nom de l’élément multimédia à lire.
ms.assetid: 521a3b39-efd6-45a7-895b-a9ae69e0bf39
keywords:
- Propriété URL du lecteur Windows Media
- Propriété URL lecteur Windows Media, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer lecteur Windows Media, propriété URL
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.URL
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3ed9e601aa581e988bac1a233f06c4f5c552353
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541660"
---
# <a name="axwindowsmediaplayerurl-property"></a><span data-ttu-id="2c413-106">AxWindowsMediaPlayer. URL (propriété)</span><span class="sxs-lookup"><span data-stu-id="2c413-106">AxWindowsMediaPlayer.URL property</span></span>

<span data-ttu-id="2c413-107">La propriété URL obtient ou définit le nom de l’élément multimédia à lire.</span><span class="sxs-lookup"><span data-stu-id="2c413-107">The URL property gets or sets the name of the media item to play.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c413-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2c413-108">Syntax</span></span>


```CSharp
public System.String URL {get; set;}
```


```VB

Public Property URL As System.String
```





## <a name="property-value"></a><span data-ttu-id="2c413-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="2c413-109">Property value</span></span>

<span data-ttu-id="2c413-110">System. String qui est l’URL de l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="2c413-110">A System.String that is the URL of the media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c413-111">Notes</span><span class="sxs-lookup"><span data-stu-id="2c413-111">Remarks</span></span>

<span data-ttu-id="2c413-112">Cette propriété peut uniquement être définie sur une URL dans une zone de sécurité identique ou moins restrictive que la zone de sécurité du programme ou de la page Web appelante.</span><span class="sxs-lookup"><span data-stu-id="2c413-112">This property can only be set to a URL in a security zone that is the same or is less restrictive than the security zone of the calling program or webpage.</span></span>

<span data-ttu-id="2c413-113">Les applications qui ouvrent des éléments multimédias à partir d’un pare-feu offrent de meilleures performances si l’adresse est spécifiée à l’aide du nom DNS (Domain Name Server) au lieu de l’adresse IP.</span><span class="sxs-lookup"><span data-stu-id="2c413-113">Applications that open media items from behind a firewall will have better performance if the address is specified using the domain name server (DNS) name instead of the IP address.</span></span>

<span data-ttu-id="2c413-114">N’appelez pas cette méthode à partir du code du gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="2c413-114">Do not call this method from event handler code.</span></span> <span data-ttu-id="2c413-115">L’appel de l' **URL** à partir d’un gestionnaire d’événements peut donner des résultats inattendus.</span><span class="sxs-lookup"><span data-stu-id="2c413-115">Calling **URL** from an event handler may yield unexpected results.</span></span>

## <a name="examples"></a><span data-ttu-id="2c413-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="2c413-116">Examples</span></span>

<span data-ttu-id="2c413-117">L’exemple suivant permet à l’utilisateur de spécifier un fichier multimédia en entrant un chemin d’accès de fichier dans une zone de texte.</span><span class="sxs-lookup"><span data-stu-id="2c413-117">The following example allows the user to specify a media file by entering a file path in a text box.</span></span> <span data-ttu-id="2c413-118">Lorsqu’un utilisateur clique sur un bouton, la propriété URL est définie sur le fichier spécifié et le fichier est lu.</span><span class="sxs-lookup"><span data-stu-id="2c413-118">When a button is clicked, the URL property is set to the specified file and the file is played.</span></span> <span data-ttu-id="2c413-119">L’objet AxWMPLib. AxWindowsMediaPlayer est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="2c413-119">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
private void openMedia_Click(object sender, System.EventArgs e)
{
    // Set the URL property to the file path obtained from the text box. 
    player.URL = inputURL.Text;

    // Play the media file. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub openMedia_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles openMedia.Click

    &#39; Set the URL property to the file path obtained from the text box. 
    player.URL = inputURL.Text

    &#39; Play the media file. 
    player.Ctlcontrols.play()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="2c413-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2c413-120">Requirements</span></span>



| <span data-ttu-id="2c413-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2c413-121">Requirement</span></span> | <span data-ttu-id="2c413-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="2c413-122">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c413-123">Version</span><span class="sxs-lookup"><span data-stu-id="2c413-123">Version</span></span><br/>   | <span data-ttu-id="2c413-124">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="2c413-124">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="2c413-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2c413-125">Namespace</span></span><br/> | <span data-ttu-id="2c413-126">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="2c413-126">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="2c413-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="2c413-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2c413-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2c413-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c413-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c413-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c413-130">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="2c413-130">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





