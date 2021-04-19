---
title: Propriété Count IWMPCdromCollection
description: La propriété Count obtient le nombre de lecteurs CD et DVD disponibles sur le système.
ms.assetid: 1359ab7e-fbe3-461c-801b-7c986f6e5687
keywords:
- propriété Count Windows Media Player
- propriété Count lecteur Windows Media, interface IWMPCdromCollection
- IWMPCdromCollection interface Windows Media Player, propriété Count
topic_type:
- apiref
api_name:
- IWMPCdromCollection.count
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2da4d4d443c730d19c791a486fed4be0241b8c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532688"
---
# <a name="iwmpcdromcollectioncount-property"></a><span data-ttu-id="7a948-106">IWMPCdromCollection :: Count, propriété</span><span class="sxs-lookup"><span data-stu-id="7a948-106">IWMPCdromCollection::count property</span></span>

<span data-ttu-id="7a948-107">La propriété **Count** obtient le nombre de lecteurs CD et DVD disponibles sur le système.</span><span class="sxs-lookup"><span data-stu-id="7a948-107">The **count** property gets the number of available CD and DVD drives on the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a948-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7a948-108">Syntax</span></span>


```CSharp
public System.Int32 count {get; set;}
```


```VB

Public ReadOnly Property count As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="7a948-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="7a948-109">Property value</span></span>

<span data-ttu-id="7a948-110">**System. Int32** qui correspond au nombre de lecteurs disponibles.</span><span class="sxs-lookup"><span data-stu-id="7a948-110">A **System.Int32** that is the count of available drives.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a948-111">Notes</span><span class="sxs-lookup"><span data-stu-id="7a948-111">Remarks</span></span>

<span data-ttu-id="7a948-112">Pour récupérer la valeur de cette propriété, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="7a948-112">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="7a948-113">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="7a948-113">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="7a948-114">Les lecteurs de DVD sont comptabilisés exactement comme les lecteurs de CD.</span><span class="sxs-lookup"><span data-stu-id="7a948-114">DVD drives are counted exactly like CD drives.</span></span> <span data-ttu-id="7a948-115">Toutefois, le contrôle ActiveX du lecteur Windows Media ne prend en charge que les fonctionnalités DVD pour Windows XP ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="7a948-115">However, the Windows Media Player ActiveX control only supports DVD functionality for Windows XP or later.</span></span> <span data-ttu-id="7a948-116">En règle générale, les lecteurs de DVD peuvent lire des CD, mais les lecteurs de CD ne peuvent pas lire les DVD.</span><span class="sxs-lookup"><span data-stu-id="7a948-116">Typically, DVD drives can play CD media, but CD drives cannot play DVD media.</span></span>

## <a name="examples"></a><span data-ttu-id="7a948-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="7a948-117">Examples</span></span>

<span data-ttu-id="7a948-118">L’exemple suivant utilise Count pour afficher le nombre de lecteurs de CD et de DVD disponibles dans une boîte de message.</span><span class="sxs-lookup"><span data-stu-id="7a948-118">The following example uses count to display the number of available CD and DVD drives in a message box.</span></span> <span data-ttu-id="7a948-119">L’objet AxWMPLib. AxWindowsMediaPlayer est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="7a948-119">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Store the number of available drives.
int numDrives = player.cdromCollection.count;

// Display the number of drives as a string.
System.Windows.Forms.MessageBox.Show("Number of available CD and DVD drives:  " + numDrives.ToString());
```


```VB

' Store the number of available drives.
Dim numDrives As Integer = player.cdromCollection.count

&#39; Display the number of drives as a string.
System.Windows.Forms.MessageBox.Show(&quot;Number of available CD and DVD drives:  &quot; + numDrives.ToString())
```





## <a name="requirements"></a><span data-ttu-id="7a948-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7a948-120">Requirements</span></span>



| <span data-ttu-id="7a948-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7a948-121">Requirement</span></span> | <span data-ttu-id="7a948-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a948-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a948-123">Version</span><span class="sxs-lookup"><span data-stu-id="7a948-123">Version</span></span><br/>   | <span data-ttu-id="7a948-124">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="7a948-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="7a948-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7a948-125">Namespace</span></span><br/> | <span data-ttu-id="7a948-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="7a948-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="7a948-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="7a948-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="7a948-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="7a948-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a948-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a948-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a948-130">**Interface IWMPCdromCollection (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="7a948-130">**IWMPCdromCollection Interface (VB and C#)**</span></span>](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7a948-131">**IWMPSettings2. mediaAccessRights (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="7a948-131">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7a948-132">**IWMPSettings2. requestMediaAccessRights (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="7a948-132">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





