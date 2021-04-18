---
title: IWMPNetwork propriété bufferingTime
description: La propriété bufferingTime obtient ou définit la durée en millisecondes allouée à la mise en mémoire tampon des données entrantes avant le début de la lecture.
ms.assetid: b5936b21-a17b-4801-a5fc-c6d6521e05aa
keywords:
- propriété bufferingTime lecteur Windows Media
- propriété bufferingTime lecteur Windows Media, interface IWMPNetwork
- Interface IWMPNetwork lecteur Windows Media, propriété bufferingTime
topic_type:
- apiref
api_name:
- IWMPNetwork.bufferingTime
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8594d53797b028dd74a8ef11cb8f2fa64b3654cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532724"
---
# <a name="iwmpnetworkbufferingtime-property"></a><span data-ttu-id="230fa-106">IWMPNetwork :: bufferingTime, propriété</span><span class="sxs-lookup"><span data-stu-id="230fa-106">IWMPNetwork::bufferingTime property</span></span>

<span data-ttu-id="230fa-107">La propriété **bufferingTime** obtient ou définit la durée en millisecondes allouée à la mise en mémoire tampon des données entrantes avant le début de la lecture.</span><span class="sxs-lookup"><span data-stu-id="230fa-107">The **bufferingTime** property gets or sets the amount of time in milliseconds allocated for buffering incoming data before playback begins.</span></span>

## <a name="syntax"></a><span data-ttu-id="230fa-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="230fa-108">Syntax</span></span>


```CSharp
public System.Int32 bufferingTime {get; set;}
```


```VB

Public Property bufferingTime As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="230fa-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="230fa-109">Property value</span></span>

<span data-ttu-id="230fa-110">**System. Int32** qui correspond au temps de mise en mémoire tampon en millisecondes, qui est compris entre zéro et 60 000 avec une valeur par défaut de 5 000.</span><span class="sxs-lookup"><span data-stu-id="230fa-110">A **System.Int32** that is the buffering time in milliseconds, which ranges from zero to 60,000 with a default value of 5,000.</span></span>

## <a name="examples"></a><span data-ttu-id="230fa-111">Exemples</span><span class="sxs-lookup"><span data-stu-id="230fa-111">Examples</span></span>

<span data-ttu-id="230fa-112">L’exemple de code suivant utilise **bufferingTime** pour spécifier le nombre de secondes allouées à la mise en mémoire tampon des données entrantes.</span><span class="sxs-lookup"><span data-stu-id="230fa-112">The following code example uses **bufferingTime** to specify the number of seconds allocated for buffering incoming data.</span></span> <span data-ttu-id="230fa-113">Une zone de texte permet à l’utilisateur d’entrer une nouvelle valeur pour **bufferingTime**, et la propriété est mise à jour en réponse à l’événement de clic d’un bouton.</span><span class="sxs-lookup"><span data-stu-id="230fa-113">A text box allows the user to enter a new value for **bufferingTime**, and the property is updated in response to the Click event of a button.</span></span> <span data-ttu-id="230fa-114">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="230fa-114">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setBufTime_Click(object sender, System.EventArgs e)
{
    // Retrieve input from the user and convert it to an integer.
    int newTime = System.Convert.ToInt32(bufText.Text);

    // Test whether the integer is within the valid range. 
    if (newTime >= 0 & newTime <= 60) 
    {
        // Set the new bufferingTime in miliseconds.
        player.network.bufferingTime = (newTime * 1000);
    }
    else
    {
        System.Windows.Forms.MessageBox.Show("Buffering time must be between 0 and 60.");
    }
}
```


```VB

Public Sub setBufTime_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setBufTime.Click

    &#39; Retrieve input from the user and convert it to an integer.
    Dim newTime As Integer = System.Convert.ToInt32(bufText.Text)

    &#39; Test whether the integer is within the valid range. 
    If (newTime >= 0 And newTime <= 60) Then

        &#39; Set the new bufferingTime in miliseconds.
        player.network.bufferingTime = (newTime * 1000)

    Else

        System.Windows.Forms.MessageBox.Show(&quot;Buffering time must be between 0 and 60.&quot;)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="230fa-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="230fa-115">Requirements</span></span>



| <span data-ttu-id="230fa-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="230fa-116">Requirement</span></span> | <span data-ttu-id="230fa-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="230fa-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="230fa-118">Version</span><span class="sxs-lookup"><span data-stu-id="230fa-118">Version</span></span><br/>   | <span data-ttu-id="230fa-119">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="230fa-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="230fa-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="230fa-120">Namespace</span></span><br/> | <span data-ttu-id="230fa-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="230fa-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="230fa-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="230fa-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="230fa-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="230fa-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="230fa-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="230fa-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="230fa-125">**Interface IWMPNetwork (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="230fa-125">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





