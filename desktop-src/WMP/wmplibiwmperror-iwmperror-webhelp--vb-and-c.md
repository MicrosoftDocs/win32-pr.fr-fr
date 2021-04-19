---
title: IWMPError Webhelp, méthode
description: La méthode Webhelp ouvre la page d’aide Web du lecteur Windows Media pour afficher des informations supplémentaires sur la première erreur de la file d’attente des erreurs (index zéro). | IWMPError Webhelp, méthode
ms.assetid: 30fc765a-04b2-44e5-99d8-0b4720ccbb25
keywords:
- méthode Webhelp lecteur Windows Media
- méthode Webhelp lecteur Windows Media, interface IWMPError
- Interface IWMPError Windows Media Player, Webhelp, méthode
topic_type:
- apiref
api_name:
- IWMPError.webHelp
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c9b0cd48d45ac5e5e5d77d0150b8acdf13347e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533449"
---
# <a name="iwmperrorwebhelp-method"></a><span data-ttu-id="64141-107">IWMPError :: Webhelp, méthode</span><span class="sxs-lookup"><span data-stu-id="64141-107">IWMPError::webHelp method</span></span>

<span data-ttu-id="64141-108">La méthode **Webhelp** ouvre la page d’aide Web du lecteur Windows Media pour afficher des informations supplémentaires sur la première erreur de la file d’attente des erreurs (index zéro).</span><span class="sxs-lookup"><span data-stu-id="64141-108">The **webHelp** method launches the Windows Media Player Web Help page to display further information about the first error in the error queue (index zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="64141-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="64141-109">Syntax</span></span>


```CSharp
public void webHelp();
```


```VB

Public Sub webHelp()
Implements IWMPError.webHelp
```





## <a name="parameters"></a><span data-ttu-id="64141-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="64141-110">Parameters</span></span>

<span data-ttu-id="64141-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="64141-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="64141-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="64141-112">Return value</span></span>

<span data-ttu-id="64141-113">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="64141-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="64141-114">Notes</span><span class="sxs-lookup"><span data-stu-id="64141-114">Remarks</span></span>

<span data-ttu-id="64141-115">Les pages d’aide Web contiennent toujours les informations les plus récentes et les plus détaillées sur les erreurs du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="64141-115">The Web Help pages always contain the latest and most detailed information about Windows Media Player errors.</span></span> <span data-ttu-id="64141-116">Cette méthode transfère automatiquement les autres informations requises par l’aide Web, telles que la version du système d’exploitation utilisée.</span><span class="sxs-lookup"><span data-stu-id="64141-116">This method automatically transfers the other information needed by Web Help, such as the operating system version being used.</span></span>

<span data-ttu-id="64141-117">Pour accéder directement aux pages d’aide Web, utilisez le code d’erreur suivant et les liens du centre d’aide et de support :</span><span class="sxs-lookup"><span data-stu-id="64141-117">To access the Web Help pages directly, use the following error code and support center links:</span></span>

-   [<span data-ttu-id="64141-118">Informations de code d’erreur du lecteur Windows Media</span><span class="sxs-lookup"><span data-stu-id="64141-118">Windows Media Player Error Code Information</span></span>](https://support.microsoft.com/kb/886273)
-   [<span data-ttu-id="64141-119">Centre de solutions du lecteur Windows Media</span><span class="sxs-lookup"><span data-stu-id="64141-119">Windows Media Player Solution Center</span></span>](https://support.microsoft.com/ph/7763#tab0)

## <a name="examples"></a><span data-ttu-id="64141-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="64141-120">Examples</span></span>

<span data-ttu-id="64141-121">L’exemple suivant crée un bouton qui lance la page d’aide Web du lecteur Microsoft Windows Media dans le navigateur.</span><span class="sxs-lookup"><span data-stu-id="64141-121">The following example creates a button that launches the Microsoft Windows Media Player Web Help page in the browser.</span></span> <span data-ttu-id="64141-122">L’objet AxWMPLib. AxWindowsMediaPlayer est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="64141-122">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
private void webHelpButton_Click(object sender, System.EventArgs e)
{
    // Launch the Microsoft Windows Media Player Web Help page in the browser.
    player.Error.webHelp();
}
```


```VB

Public Sub webHelpButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles webHelpButton.Click

    &#39; Launch the Microsoft Windows Media Player Web Help page in the browser.
    player.Error.webHelp()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="64141-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="64141-123">Requirements</span></span>



| <span data-ttu-id="64141-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="64141-124">Requirement</span></span> | <span data-ttu-id="64141-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="64141-125">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64141-126">Version</span><span class="sxs-lookup"><span data-stu-id="64141-126">Version</span></span><br/>   | <span data-ttu-id="64141-127">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="64141-127">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="64141-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="64141-128">Namespace</span></span><br/> | <span data-ttu-id="64141-129">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="64141-129">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="64141-130">Assembly</span><span class="sxs-lookup"><span data-stu-id="64141-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="64141-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="64141-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64141-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64141-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64141-133">**Interface IWMPError (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="64141-133">**IWMPError Interface (VB and C#)**</span></span>](iwmperror--vb-and-c.md)
</dt> </dl>

 

 





