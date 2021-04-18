---
title: Méthode IWMPNetwork setProxyBypassForLocal
description: La méthode setProxyBypassForLocal spécifie si le serveur proxy est contourné si le serveur d’origine se trouve sur un réseau local.
ms.assetid: b308957a-0d7e-45be-8625-db198b276dad
keywords:
- méthode setProxyBypassForLocal lecteur Windows Media
- méthode setProxyBypassForLocal lecteur Windows Media, interface IWMPNetwork
- Interface IWMPNetwork lecteur Windows Media, méthode setProxyBypassForLocal
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxyBypassForLocal
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35f869125d43529a039804fe28c0f0dc493f481e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540298"
---
# <a name="iwmpnetworksetproxybypassforlocal-method"></a><span data-ttu-id="18f7f-106">IWMPNetwork :: setProxyBypassForLocal, méthode</span><span class="sxs-lookup"><span data-stu-id="18f7f-106">IWMPNetwork::setProxyBypassForLocal method</span></span>

<span data-ttu-id="18f7f-107">La méthode **setProxyBypassForLocal** spécifie si le serveur proxy est contourné si le serveur d’origine se trouve sur un réseau local.</span><span class="sxs-lookup"><span data-stu-id="18f7f-107">The **setProxyBypassForLocal** method specifies whether the proxy server is bypassed if the origin server is on a local network.</span></span>

## <a name="syntax"></a><span data-ttu-id="18f7f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="18f7f-108">Syntax</span></span>


```CSharp
public void setProxyBypassForLocal(
  System.String bstrProtocol,
  System.Boolean fBypassForLocal
);
```


```VB

Public Sub setProxyBypassForLocal( _
  ByVal bstrProtocol As System.String, _
  ByVal fBypassForLocal As System.Boolean _
)
Implements IWMPNetwork.setProxyBypassForLocal
```





## <a name="parameters"></a><span data-ttu-id="18f7f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="18f7f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18f7f-110">*bstrProtocol* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="18f7f-110">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18f7f-111">**System. String** qui est le nom de protocole.</span><span class="sxs-lookup"><span data-stu-id="18f7f-111">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="18f7f-112">Pour obtenir la liste des protocoles pris en charge, consultez [protocoles et types de fichiers pris en charge](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="18f7f-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="18f7f-113">*fBypassForLocal* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="18f7f-113">*fBypassForLocal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18f7f-114">Valeur **System. Boolean** qui indique si le serveur proxy est contourné.</span><span class="sxs-lookup"><span data-stu-id="18f7f-114">A **System.Boolean** value that indicates whether the proxy server is bypassed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18f7f-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="18f7f-115">Return value</span></span>

<span data-ttu-id="18f7f-116">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="18f7f-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="18f7f-117">Notes</span><span class="sxs-lookup"><span data-stu-id="18f7f-117">Remarks</span></span>

<span data-ttu-id="18f7f-118">Cette méthode n’a aucun effet, sauf si la valeur récupérée à partir de **IWMPNetwork. getProxySettings** est 2 (utiliser des paramètres manuels).</span><span class="sxs-lookup"><span data-stu-id="18f7f-118">This method has no effect unless the value retrieved from **IWMPNetwork.getProxySettings** is 2 (use manual settings).</span></span>

<span data-ttu-id="18f7f-119">Cette méthode échoue sauf si l’application appelante est en cours d’exécution sur l’ordinateur local ou sur l’intranet.</span><span class="sxs-lookup"><span data-stu-id="18f7f-119">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="18f7f-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="18f7f-120">Examples</span></span>

<span data-ttu-id="18f7f-121">L’exemple de code suivant utilise **setProxyBypassForLocal** pour spécifier si le serveur proxy du lecteur Windows Media est contourné, lors de l’utilisation du protocole MMS, si le serveur d’origine se trouve sur un réseau local.</span><span class="sxs-lookup"><span data-stu-id="18f7f-121">The following code example uses **setProxyBypassForLocal** to specify whether the Windows Media Player proxy server is bypassed, when using the MMS protocol, if the origin server is on a local network.</span></span> <span data-ttu-id="18f7f-122">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="18f7f-122">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Prepare a message, a caption and buttons for the user prompt.
string message = ("Bypass proxy server for local addresses?");
string caption = "Proxy Settings";
System.Windows.Forms.MessageBoxButtons buttons = System.Windows.Forms.MessageBoxButtons.YesNo;

// Test whether the proxy settings are manual.
if (player.network.getProxySettings("MMS") == 2)
{
    // Prompt the user for a setting. 
    System.Windows.Forms.DialogResult result = System.Windows.Forms.MessageBox.Show(message, caption, buttons);

    // Store the return value of the DialogResult in a boolean variable.
    bool proxybypass;
    
    if(result == System.Windows.Forms.DialogResult.Yes)
    {
        proxybypass = true;
    }
    else
    {
        proxybypass = false;
    }

    // Set the proxy bypass value according to the response.
    player.network.setProxyBypassForLocal("MMS", proxybypass);
}
else
{
    // Warn that proxy settings must be set to 2 (manual).
    System.Windows.Forms.MessageBox.Show("Proxy settings must be manual!");
}
```


```VB

' Prepare a message, a caption and buttons for the user prompt.
Dim message As String = &quot;Bypass proxy server for local addresses?&quot;
Dim caption As String = &quot;Proxy Settings&quot;
Dim buttons As System.Windows.Forms.MessageBoxButtons = System.Windows.Forms.MessageBoxButtons.YesNo

&#39; Test whether the proxy settings are manual.
If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

    &#39; Prompt the user for a setting. 
    Dim result As System.Windows.Forms.DialogResult = System.Windows.Forms.MessageBox.Show(message, caption, buttons)

    &#39; Store the return value of the DialogResult as a boolean.
    Dim proxybypass As Boolean

    If (result = System.Windows.Forms.DialogResult.Yes) Then

        proxybypass = True

    Else

        proxybypass = False

    End If

    &#39; Set the proxy bypass value according to the response.
    player.network.setProxyBypassForLocal(&quot;MMS&quot;, proxybypass)

Else

    &#39; Warn that proxy settings must be set to 2 (manual).
    System.Windows.Forms.MessageBox.Show(&quot;Proxy settings must be manual!&quot;)

End If
```





## <a name="requirements"></a><span data-ttu-id="18f7f-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="18f7f-123">Requirements</span></span>



| <span data-ttu-id="18f7f-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="18f7f-124">Requirement</span></span> | <span data-ttu-id="18f7f-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="18f7f-125">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18f7f-126">Version</span><span class="sxs-lookup"><span data-stu-id="18f7f-126">Version</span></span><br/>   | <span data-ttu-id="18f7f-127">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="18f7f-127">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="18f7f-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="18f7f-128">Namespace</span></span><br/> | <span data-ttu-id="18f7f-129">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="18f7f-129">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="18f7f-130">Assembly</span><span class="sxs-lookup"><span data-stu-id="18f7f-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="18f7f-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="18f7f-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18f7f-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18f7f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18f7f-133">**Interface IWMPNetwork (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="18f7f-133">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="18f7f-134">**IWMPNetwork. getProxyBypassForLocal (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="18f7f-134">**IWMPNetwork.getProxyBypassForLocal (VB and C#)**</span></span>](iwmpnetwork-getproxybypassforlocal--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="18f7f-135">**IWMPNetwork. getProxySettings (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="18f7f-135">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





