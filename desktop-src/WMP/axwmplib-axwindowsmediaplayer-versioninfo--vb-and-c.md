---
title: AxWindowsMediaPlayer. versionInfo, propriété
description: La propriété versionInfo obtient une valeur qui spécifie la version du lecteur Windows Media.
ms.assetid: e128bec5-1ae9-4710-800e-4f97df362909
keywords:
- propriété versionInfo lecteur Windows Media
- propriété versionInfo lecteur Windows Media, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer lecteur Windows Media, propriété versionInfo
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.versionInfo
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2f759c2aedb19e21c4b7d90f3634141e4c37ec8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543276"
---
# <a name="axwindowsmediaplayerversioninfo-property"></a><span data-ttu-id="c0775-106">AxWindowsMediaPlayer. versionInfo, propriété</span><span class="sxs-lookup"><span data-stu-id="c0775-106">AxWindowsMediaPlayer.versionInfo property</span></span>

<span data-ttu-id="c0775-107">La propriété versionInfo obtient une valeur qui spécifie la version du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c0775-107">The versionInfo property gets a value that specifies the version of the Windows Media Player.</span></span>

<span data-ttu-id="c0775-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="c0775-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0775-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0775-109">Syntax</span></span>


```CSharp
public System.String versionInfo {get;}
```


```VB

Public ReadOnly Property versionInfo As System.String
```





## <a name="property-value"></a><span data-ttu-id="c0775-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="c0775-110">Property value</span></span>

<span data-ttu-id="c0775-111">System. String qui correspond aux informations de version au format suivant : «*X*. 0,0. *Yyyy*"où *X* représente le numéro de version principale et *yyyy* représente le numéro de Build.</span><span class="sxs-lookup"><span data-stu-id="c0775-111">A System.String that is the version information in the following format: "*X*.0.0.*YYYY*" where *X* represents the major version number and *YYYY* represents the build number.</span></span>

## <a name="examples"></a><span data-ttu-id="c0775-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="c0775-112">Examples</span></span>

<span data-ttu-id="c0775-113">L’exemple suivant crée un bouton qui, lorsque vous cliquez dessus, affiche une boîte de message contenant les informations de version pour le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c0775-113">The following example creates a button that, when clicked, displays a message box containing the version information for Windows Media Player.</span></span> <span data-ttu-id="c0775-114">L’objet AxWMPLib. AxWindowsMediaPlayer est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="c0775-114">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
private void showVersion_Click(object sender, System.EventArgs e)
{
    // Build the message containing the version info. 
    string message = ("Windows Media Player Version: " + player.versionInfo);

    // Display the message. 
    System.Windows.Forms.MessageBox.Show(message);
}
```


```VB

Public Sub showVersion_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles showVersion.Click

    &#39; Build the message containing the version info. 
    Dim message As String = (&quot;Windows Media Player Version: &quot; + player.versionInfo)

    &#39; Display the message. 
    System.Windows.Forms.MessageBox.Show(message)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="c0775-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0775-115">Requirements</span></span>



| <span data-ttu-id="c0775-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0775-116">Requirement</span></span> | <span data-ttu-id="c0775-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0775-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0775-118">Version</span><span class="sxs-lookup"><span data-stu-id="c0775-118">Version</span></span><br/>   | <span data-ttu-id="c0775-119">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="c0775-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="c0775-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c0775-120">Namespace</span></span><br/> | <span data-ttu-id="c0775-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="c0775-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="c0775-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="c0775-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c0775-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c0775-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0775-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0775-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0775-125">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="c0775-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





