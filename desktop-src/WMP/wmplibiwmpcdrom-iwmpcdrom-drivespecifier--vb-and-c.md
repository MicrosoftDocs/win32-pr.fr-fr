---
title: IWMPCdrom propriété driveSpecifier
description: La propriété driveSpecifier obtient la lettre du lecteur de CD ou de DVD.
ms.assetid: 8865232a-08a3-447b-a6d6-2bfda3a689e1
keywords:
- propriété driveSpecifier lecteur Windows Media
- propriété driveSpecifier lecteur Windows Media, interface IWMPCdrom
- Interface IWMPCdrom lecteur Windows Media, propriété driveSpecifier
topic_type:
- apiref
api_name:
- IWMPCdrom.driveSpecifier
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0a6c439523d90824da708700d48274f5a2e5ef4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533358"
---
# <a name="iwmpcdromdrivespecifier-property"></a><span data-ttu-id="d74b5-106">IWMPCdrom ::d propriété riveSpecifier</span><span class="sxs-lookup"><span data-stu-id="d74b5-106">IWMPCdrom::driveSpecifier property</span></span>

<span data-ttu-id="d74b5-107">La propriété **driveSpecifier** obtient la lettre du lecteur de CD ou de DVD.</span><span class="sxs-lookup"><span data-stu-id="d74b5-107">The **driveSpecifier** property gets the CD or DVD drive letter.</span></span>

## <a name="syntax"></a><span data-ttu-id="d74b5-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d74b5-108">Syntax</span></span>


```CSharp
public System.String driveSpecifier {get; set;}
```


```VB

Public ReadOnly Property driveSpecifier As System.String
```





## <a name="property-value"></a><span data-ttu-id="d74b5-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="d74b5-109">Property value</span></span>

<span data-ttu-id="d74b5-110">**System. String** qui correspond à la lettre de lecteur.</span><span class="sxs-lookup"><span data-stu-id="d74b5-110">A **System.String** that is the drive letter.</span></span>

## <a name="remarks"></a><span data-ttu-id="d74b5-111">Notes</span><span class="sxs-lookup"><span data-stu-id="d74b5-111">Remarks</span></span>

<span data-ttu-id="d74b5-112">En règle générale, les lecteurs de DVD peuvent lire des CD, mais les lecteurs de CD ne peuvent pas lire les DVD.</span><span class="sxs-lookup"><span data-stu-id="d74b5-112">Typically, DVD drives can play CD media, but CD drives cannot play DVD media.</span></span>

<span data-ttu-id="d74b5-113">Cette propriété obtient une lettre de lecteur pour un index de lecteur de base zéro dans la plage Récupérée à l’aide de **IWMPCdromCollection. Count**.</span><span class="sxs-lookup"><span data-stu-id="d74b5-113">This property gets a drive letter for a zero-based drive index within the range retrieved using **IWMPCdromCollection.count**.</span></span> <span data-ttu-id="d74b5-114">La valeur récupérée prend la forme *x*:, où *x* représente la lettre de lecteur.</span><span class="sxs-lookup"><span data-stu-id="d74b5-114">The value retrieved takes the form *X*:, where *X* represents the drive letter.</span></span>

<span data-ttu-id="d74b5-115">Pour récupérer la valeur de cette propriété, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="d74b5-115">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="d74b5-116">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="d74b5-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d74b5-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="d74b5-117">Examples</span></span>

<span data-ttu-id="d74b5-118">L’exemple suivant utilise **driveSpecifier** pour créer une chaîne qui contient une liste de lecteurs de CD et DVD disponibles et qui affiche cette chaîne dans une boîte de message.</span><span class="sxs-lookup"><span data-stu-id="d74b5-118">The following example uses **driveSpecifier** to build a string that contains a list of available CD and DVD drives and displays that string in a message box.</span></span> <span data-ttu-id="d74b5-119">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="d74b5-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// String that will contain the list of drive specifiers.
string MyDriveSpecifiers = "Drive letters found:  ";

// Store the number of available drives.
int numDrives = player.cdromCollection.count;

// Loop through the available drives. 
for (int i = 0; i < numDrives; i++)
{
    MyDriveSpecifiers += player.cdromCollection.Item(i).driveSpecifier;
    MyDriveSpecifiers += " ";
}

// Display the list of drive specifiers in a message box.
System.Windows.Forms.MessageBox.Show(MyDriveSpecifiers);
```


```VB

'  String that will contain the list of drive specifiers.
Dim MyDriveSpecifiers As String = &quot;Drive letters found:  &quot;

&#39;  Store the number of available drives.
Dim numDrives = player.cdromCollection.count

&#39;  Loop through the available drives. 
For i As Integer = 0 To (numDrives - 1)
    MyDriveSpecifiers += player.cdromCollection.Item(i).driveSpecifier
    MyDriveSpecifiers += &quot; &quot;
Next i

&#39;  Display the list of drive specifiers in a message box.
System.Windows.Forms.MessageBox.Show(MyDriveSpecifiers)
```





## <a name="requirements"></a><span data-ttu-id="d74b5-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d74b5-120">Requirements</span></span>



| <span data-ttu-id="d74b5-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d74b5-121">Requirement</span></span> | <span data-ttu-id="d74b5-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="d74b5-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d74b5-123">Version</span><span class="sxs-lookup"><span data-stu-id="d74b5-123">Version</span></span><br/>   | <span data-ttu-id="d74b5-124">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="d74b5-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="d74b5-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d74b5-125">Namespace</span></span><br/> | <span data-ttu-id="d74b5-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="d74b5-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="d74b5-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="d74b5-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d74b5-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="d74b5-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d74b5-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d74b5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d74b5-130">**Interface IWMPCdrom (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="d74b5-130">**IWMPCdrom Interface (VB and C#)**</span></span>](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d74b5-131">**IWMPCdromCollection. Count (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="d74b5-131">**IWMPCdromCollection.count (VB and C#)**</span></span>](wmplibiwmpcdromcollection-iwmpcdromcollection-count--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d74b5-132">**IWMPSettings2. mediaAccessRights (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="d74b5-132">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d74b5-133">**IWMPSettings2. requestMediaAccessRights (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="d74b5-133">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





