---
title: Méthode EJECT IWMPCdrom
description: La méthode EJECT éjecte le CD ou DVD du lecteur. | Méthode EJECT IWMPCdrom
ms.assetid: c0a69252-fd79-452c-bc61-3c3e8bcaaf48
keywords:
- méthode EJECT lecteur Windows Media
- méthode EJECT lecteur Windows Media, interface IWMPCdrom
- Interface IWMPCdrom lecteur Windows Media, méthode EJECT
topic_type:
- apiref
api_name:
- IWMPCdrom.eject
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8ca2403b86b648e98861d91a21db80ddb64aac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538127"
---
# <a name="iwmpcdromeject-method"></a><span data-ttu-id="f44fd-107">IWMPCdrom :: EJECT, méthode</span><span class="sxs-lookup"><span data-stu-id="f44fd-107">IWMPCdrom::eject method</span></span>

<span data-ttu-id="f44fd-108">La méthode **EJECT** éjecte le CD ou DVD du lecteur.</span><span class="sxs-lookup"><span data-stu-id="f44fd-108">The **eject** method ejects the CD or DVD from the drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="f44fd-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f44fd-109">Syntax</span></span>


```CSharp
public void eject();
```


```VB

Public Sub eject()
Implements IWMPCdrom.eject
```





## <a name="parameters"></a><span data-ttu-id="f44fd-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f44fd-110">Parameters</span></span>

<span data-ttu-id="f44fd-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="f44fd-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f44fd-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f44fd-112">Return value</span></span>

<span data-ttu-id="f44fd-113">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f44fd-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f44fd-114">Notes</span><span class="sxs-lookup"><span data-stu-id="f44fd-114">Remarks</span></span>

<span data-ttu-id="f44fd-115">Si le loquet du lecteur est ouvert, cette méthode ferme la porte.</span><span class="sxs-lookup"><span data-stu-id="f44fd-115">If the drive door is open, this method closes the door.</span></span>

<span data-ttu-id="f44fd-116">Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="f44fd-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="f44fd-117">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="f44fd-117">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="f44fd-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="f44fd-118">Examples</span></span>

<span data-ttu-id="f44fd-119">L’exemple suivant utilise **EJECT** pour ouvrir la porte du lecteur de CD ou de DVD dont l’index est égal à zéro en réponse à l’événement de clic d’un bouton.</span><span class="sxs-lookup"><span data-stu-id="f44fd-119">The following example uses **eject** to open the door of the CD or DVD drive that has the index of zero in response to the Click event of a button.</span></span> <span data-ttu-id="f44fd-120">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="f44fd-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void ejectButton_Click(object o, System.EventArgs args)
{
    player.cdromCollection.Item(0).eject();
}
```


```VB

Public Sub ejectButton_Click(ByVal o As Object, ByVal args As System.EventArgs) Handles ejectButton.Click

    player.cdromCollection.Item(0).eject()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="f44fd-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f44fd-121">Requirements</span></span>



| <span data-ttu-id="f44fd-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f44fd-122">Requirement</span></span> | <span data-ttu-id="f44fd-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="f44fd-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f44fd-124">Version</span><span class="sxs-lookup"><span data-stu-id="f44fd-124">Version</span></span><br/>   | <span data-ttu-id="f44fd-125">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="f44fd-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="f44fd-126">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f44fd-126">Namespace</span></span><br/> | <span data-ttu-id="f44fd-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="f44fd-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f44fd-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="f44fd-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f44fd-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f44fd-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f44fd-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f44fd-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f44fd-131">**AxWindowsMediaPlayer. lecture (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="f44fd-131">**AxWindowsMediaPlayer.playState (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-playstate--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f44fd-132">**Interface IWMPCdrom (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="f44fd-132">**IWMPCdrom Interface (VB and C#)**</span></span>](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f44fd-133">**IWMPSettings2. mediaAccessRights (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="f44fd-133">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f44fd-134">**IWMPSettings2. requestMediaAccessRights (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="f44fd-134">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





