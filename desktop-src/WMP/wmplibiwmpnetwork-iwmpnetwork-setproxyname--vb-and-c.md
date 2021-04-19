---
title: Méthode IWMPNetwork setProxyName
description: La méthode setProxyName spécifie le nom du serveur proxy à utiliser. | Méthode IWMPNetwork setProxyName
ms.assetid: a3b0f53a-d81a-4e6d-9cac-7047433246ae
keywords:
- méthode setProxyName lecteur Windows Media
- méthode setProxyName lecteur Windows Media, interface IWMPNetwork
- Interface IWMPNetwork lecteur Windows Media, méthode setProxyName
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxyName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86c9759f37dd4c0e171c09afaea4dfde0993c7f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541555"
---
# <a name="iwmpnetworksetproxyname-method"></a><span data-ttu-id="22839-107">IWMPNetwork :: setProxyName, méthode</span><span class="sxs-lookup"><span data-stu-id="22839-107">IWMPNetwork::setProxyName method</span></span>

<span data-ttu-id="22839-108">La méthode **setProxyName** spécifie le nom du serveur proxy à utiliser.</span><span class="sxs-lookup"><span data-stu-id="22839-108">The **setProxyName** method specifies the name of the proxy server to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="22839-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="22839-109">Syntax</span></span>


```CSharp
public void setProxyName(
  System.String bstrProtocol,
  System.String bstrProxyName
);
```


```VB

Public Sub setProxyName( _
  ByVal bstrProtocol As System.String, _
  ByVal bstrProxyName As System.String _
)
Implements IWMPNetwork.setProxyName
```





## <a name="parameters"></a><span data-ttu-id="22839-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="22839-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22839-111">*bstrProtocol* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="22839-111">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22839-112">**System. String** qui est le nom de protocole.</span><span class="sxs-lookup"><span data-stu-id="22839-112">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="22839-113">Pour obtenir la liste des protocoles pris en charge, consultez [protocoles et types de fichiers pris en charge](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="22839-113">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="22839-114">*bstrProxyName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="22839-114">*bstrProxyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22839-115">**System. String** qui est le nom du serveur proxy à utiliser.</span><span class="sxs-lookup"><span data-stu-id="22839-115">A **System.String** that is the name of the proxy server to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22839-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="22839-116">Return value</span></span>

<span data-ttu-id="22839-117">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="22839-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="22839-118">Notes</span><span class="sxs-lookup"><span data-stu-id="22839-118">Remarks</span></span>

<span data-ttu-id="22839-119">Cette méthode n’a aucun effet, sauf si la valeur récupérée à partir de **IWMPNetwork. getProxySettings** est 2 (utiliser des paramètres manuels).</span><span class="sxs-lookup"><span data-stu-id="22839-119">This method has no effect unless the value retrieved from **IWMPNetwork.getProxySettings** is 2 (use manual settings).</span></span>

<span data-ttu-id="22839-120">Cette méthode échoue sauf si l’application appelante est en cours d’exécution sur l’ordinateur local ou sur l’intranet.</span><span class="sxs-lookup"><span data-stu-id="22839-120">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="22839-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="22839-121">Examples</span></span>

<span data-ttu-id="22839-122">L’exemple de code suivant utilise **setProxyName** pour spécifier le nom du serveur proxy du lecteur Windows Media pour le protocole MMS.</span><span class="sxs-lookup"><span data-stu-id="22839-122">The following code example uses **setProxyName** to specify the name of the Windows Media Player proxy server for the MMS protocol.</span></span> <span data-ttu-id="22839-123">Le nouveau nom est récupéré à partir d’une zone de texte lorsque l’utilisateur clique sur un bouton.</span><span class="sxs-lookup"><span data-stu-id="22839-123">The new name is retrieved from a text box when a button is clicked.</span></span> <span data-ttu-id="22839-124">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="22839-124">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setProxyName_Click(object sender, System.EventArgs e)
{
    // Test whether proxy settings are manual.
    if (player.network.getProxySettings("MMS") == 2)
    {
        // Store the user's new proxy name.
        string proxyname = nameText.Text;

        // Set the proxy name.
        player.network.setProxyName("MMS", proxyname);
    }
    else
    {
        // Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show("Proxy settings must be manual!");
    }
}
```


```VB

Public Sub setProxyName_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setProxyName.Click

    &#39; Test whether proxy settings are manual.
    If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

        &#39; Store the user&#39;s new proxy name.
        Dim proxyname As String = nameText.Text

        &#39; Set the proxy name.
        player.network.setProxyName(&quot;MMS&quot;, proxyname)

    Else

        &#39; Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show(&quot;Proxy settings must be manual!&quot;)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="22839-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="22839-125">Requirements</span></span>



| <span data-ttu-id="22839-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="22839-126">Requirement</span></span> | <span data-ttu-id="22839-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="22839-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22839-128">Version</span><span class="sxs-lookup"><span data-stu-id="22839-128">Version</span></span><br/>   | <span data-ttu-id="22839-129">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="22839-129">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="22839-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="22839-130">Namespace</span></span><br/> | <span data-ttu-id="22839-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="22839-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="22839-132">Assembly</span><span class="sxs-lookup"><span data-stu-id="22839-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="22839-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="22839-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22839-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22839-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22839-135">**Interface IWMPNetwork (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="22839-135">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="22839-136">**IWMPNetwork. getProxyName (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="22839-136">**IWMPNetwork.getProxyName (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxyname--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="22839-137">**IWMPNetwork. getProxySettings (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="22839-137">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





