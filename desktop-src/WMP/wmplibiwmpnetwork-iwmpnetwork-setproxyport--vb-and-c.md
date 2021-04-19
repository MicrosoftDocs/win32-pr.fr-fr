---
title: Méthode IWMPNetwork setProxyPort
description: La méthode setProxyPort spécifie le port du proxy à utiliser. | Méthode IWMPNetwork setProxyPort
ms.assetid: df4b33f6-52b5-437f-ade2-0d08ca2878a9
keywords:
- méthode setProxyPort lecteur Windows Media
- méthode setProxyPort lecteur Windows Media, interface IWMPNetwork
- Interface IWMPNetwork lecteur Windows Media, méthode setProxyPort
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxyPort
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d171fa1afc129dd1d13c1d9d12d71c4370cba9a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533424"
---
# <a name="iwmpnetworksetproxyport-method"></a><span data-ttu-id="c90db-107">IWMPNetwork :: setProxyPort, méthode</span><span class="sxs-lookup"><span data-stu-id="c90db-107">IWMPNetwork::setProxyPort method</span></span>

<span data-ttu-id="c90db-108">La méthode **setProxyPort** spécifie le port du proxy à utiliser.</span><span class="sxs-lookup"><span data-stu-id="c90db-108">The **setProxyPort** method specifies the proxy port to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="c90db-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c90db-109">Syntax</span></span>


```CSharp
public void setProxyPort(
  System.String bstrProtocol,
  System.Int32 lProxyPort
);
```


```VB

Public Sub setProxyPort( _
  ByVal bstrProtocol As System.String, _
  ByVal lProxyPort As System.Int32 _
)
Implements IWMPNetwork.setProxyPort
```





## <a name="parameters"></a><span data-ttu-id="c90db-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c90db-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c90db-111">*bstrProtocol* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c90db-111">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c90db-112">**System. String** qui est le nom de protocole.</span><span class="sxs-lookup"><span data-stu-id="c90db-112">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="c90db-113">Pour obtenir la liste des protocoles pris en charge, consultez [protocoles et types de fichiers pris en charge](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="c90db-113">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="c90db-114">*lProxyPort* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c90db-114">*lProxyPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c90db-115">**System. Int32** qui est le port proxy à utiliser.</span><span class="sxs-lookup"><span data-stu-id="c90db-115">A **System.Int32** that is the proxy port to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c90db-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c90db-116">Return value</span></span>

<span data-ttu-id="c90db-117">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c90db-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c90db-118">Notes</span><span class="sxs-lookup"><span data-stu-id="c90db-118">Remarks</span></span>

<span data-ttu-id="c90db-119">Cette méthode n’a aucun effet, sauf si la valeur récupérée à partir de **IWMPNetwork. getProxySettings** est 2 (utiliser des paramètres manuels).</span><span class="sxs-lookup"><span data-stu-id="c90db-119">This method has no effect unless the value retrieved from **IWMPNetwork.getProxySettings** is 2 (use manual settings).</span></span>

<span data-ttu-id="c90db-120">Cette méthode échoue sauf si l’application appelante est en cours d’exécution sur l’ordinateur local ou sur l’intranet.</span><span class="sxs-lookup"><span data-stu-id="c90db-120">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="c90db-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="c90db-121">Examples</span></span>

<span data-ttu-id="c90db-122">L’exemple de code suivant utilise **setProxyPort** pour spécifier le numéro de port du proxy du lecteur Windows Media pour le protocole MMS.</span><span class="sxs-lookup"><span data-stu-id="c90db-122">The following code example uses **setProxyPort** to specify the Windows Media Player proxy port number for the MMS protocol.</span></span> <span data-ttu-id="c90db-123">Le numéro de port est récupéré à partir d’une zone de texte lorsque l’utilisateur clique sur un bouton.</span><span class="sxs-lookup"><span data-stu-id="c90db-123">The port number is retrieved from a text box when a button is clicked.</span></span> <span data-ttu-id="c90db-124">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="c90db-124">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setProxyPort_Click(object sender, System.EventArgs e)
{
    // Test whether proxy settings are manual.
    if (player.network.getProxySettings("MMS") == 2)
    {
        // Store the user's new proxy port number.
        int portnumber = System.Convert.ToInt32(portText.Text);

        // Set the proxy port.
        player.network.setProxyPort("MMS", portnumber);
    }
    else
    {
        // Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show("Proxy settings must be manual!");
    }
}
```


```VB

Public Sub setProxyPort_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setProxyPort.Click

    &#39; Test whether proxy settings are manual.
    If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

        &#39; Store the user&#39;s new proxy port number.
        Dim portnumber As Integer = System.Convert.ToInt32(portText.Text)

        &#39; Set the proxy port.
        player.network.setProxyPort(&quot;MMS&quot;, portnumber)

    Else

        &#39; Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show(&quot;Proxy settings must be manual!&quot;)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="c90db-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c90db-125">Requirements</span></span>



| <span data-ttu-id="c90db-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c90db-126">Requirement</span></span> | <span data-ttu-id="c90db-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="c90db-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c90db-128">Version</span><span class="sxs-lookup"><span data-stu-id="c90db-128">Version</span></span><br/>   | <span data-ttu-id="c90db-129">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="c90db-129">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="c90db-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c90db-130">Namespace</span></span><br/> | <span data-ttu-id="c90db-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="c90db-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="c90db-132">Assembly</span><span class="sxs-lookup"><span data-stu-id="c90db-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c90db-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c90db-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c90db-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c90db-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c90db-135">**Interface IWMPNetwork (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="c90db-135">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c90db-136">**IWMPNetwork. getProxyPort (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="c90db-136">**IWMPNetwork.getProxyPort (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxyport--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c90db-137">**IWMPNetwork. getProxySettings (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="c90db-137">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





