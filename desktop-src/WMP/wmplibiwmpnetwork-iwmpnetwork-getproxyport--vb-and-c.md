---
title: Méthode IWMPNetwork getProxyPort
description: La méthode getProxyPort retourne le port proxy utilisé.
ms.assetid: fc94f3a9-458d-410c-98e9-a34be6e08c52
keywords:
- méthode getProxyPort lecteur Windows Media
- méthode getProxyPort lecteur Windows Media, interface IWMPNetwork
- Interface IWMPNetwork lecteur Windows Media, méthode getProxyPort
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxyPort
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46fb388c2740e709e75579c01d216af677a826c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541616"
---
# <a name="iwmpnetworkgetproxyport-method"></a><span data-ttu-id="f69b7-106">IWMPNetwork :: getProxyPort, méthode</span><span class="sxs-lookup"><span data-stu-id="f69b7-106">IWMPNetwork::getProxyPort method</span></span>

<span data-ttu-id="f69b7-107">La méthode **getProxyPort** retourne le port proxy utilisé.</span><span class="sxs-lookup"><span data-stu-id="f69b7-107">The **getProxyPort** method returns the proxy port being used.</span></span>

## <a name="syntax"></a><span data-ttu-id="f69b7-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f69b7-108">Syntax</span></span>


```CSharp
public System.Int32 getProxyPort(
  System.String bstrProtocol
);
```


```VB

Public Function getProxyPort( _
  ByVal bstrProtocol As System.String _
) As System.Int32
Implements IWMPNetwork.getProxyPort
```





## <a name="parameters"></a><span data-ttu-id="f69b7-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f69b7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f69b7-110">*bstrProtocol* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f69b7-110">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f69b7-111">**System. String** qui est le nom de protocole.</span><span class="sxs-lookup"><span data-stu-id="f69b7-111">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="f69b7-112">Pour obtenir la liste des protocoles pris en charge, consultez [protocoles et types de fichiers pris en charge](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="f69b7-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f69b7-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f69b7-113">Return value</span></span>

<span data-ttu-id="f69b7-114">**System. Int32** qui est le port proxy utilisé.</span><span class="sxs-lookup"><span data-stu-id="f69b7-114">A **System.Int32** that is the proxy port being used.</span></span> <span data-ttu-id="f69b7-115">La valeur est significative uniquement lorsque **IWMPNetwork. getProxySettings** retourne la valeur 2 (utiliser des paramètres manuels).</span><span class="sxs-lookup"><span data-stu-id="f69b7-115">The value is meaningful only when **IWMPNetwork.getProxySettings** returns a value of 2 (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="f69b7-116">Notes</span><span class="sxs-lookup"><span data-stu-id="f69b7-116">Remarks</span></span>

<span data-ttu-id="f69b7-117">Cette méthode échoue sauf si l’application appelante est en cours d’exécution sur l’ordinateur local ou sur l’intranet.</span><span class="sxs-lookup"><span data-stu-id="f69b7-117">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="f69b7-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="f69b7-118">Examples</span></span>

<span data-ttu-id="f69b7-119">L’exemple de code suivant utilise **getProxyPort** pour afficher les numéros de port du proxy du lecteur Windows Media actuels pour les protocoles MMS et http.</span><span class="sxs-lookup"><span data-stu-id="f69b7-119">The following code example uses **getProxyPort** to display the current Windows Media Player proxy port numbers for the MMS and HTTP protocols.</span></span> <span data-ttu-id="f69b7-120">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="f69b7-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Variables to hold the results of calls to getProxyPort. 
int proxyPortHTTP = 0;
int proxyPortMMS = 0;

// Test whether the HTTP proxy settings are manual.
if (player.network.getProxySettings("HTTP") == 2)
{
    proxyPortHTTP = player.network.getProxyPort("HTTP");
}

// Test whether the MMS proxy settings are manual.
if (player.network.getProxySettings("MMS") == 2)
{
    proxyPortMMS = player.network.getProxyPort("MMS");
}

// Store the proxy port numbers in a string array and display them using a multi-line
// text box. Unavailable proxy port numbers will display as "undefined".
proxyPorts[0] = ("The current HTTP proxy port is: " + proxyPortHTTP.ToString());
proxyPorts[1] = ("The current MMS proxy port is: " + proxyPortMMS.ToString());
proxyPortText.Lines = proxyPorts;
```


```VB

' Variables to hold the results of calls to getProxyPort. 
Dim proxyPortHTTP As Integer = 0
Dim proxyPortMMS As Integer = 0

&#39; Test whether the HTTP proxy settings are manual.
If (player.network.getProxySettings(&quot;HTTP&quot;) = 2) Then

    proxyPortHTTP = player.network.getProxyPort(&quot;HTTP&quot;)

End If

&#39; Test whether the MMS proxy settings are manual.
If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

    proxyPortMMS = player.network.getProxyPort(&quot;MMS&quot;)

End If

&#39; Store the proxy port numbers in a string array and display them using a multi-line
&#39; text box. Unavailable proxy port numbers will display as &quot;undefined&quot;.
proxyPorts(0) = (&quot;The current HTTP proxy port is: &quot; + proxyPortHTTP.ToString())
proxyPorts(1) = (&quot;The current MMS proxy port is: &quot; + proxyPortMMS.ToString())
proxyPortText.Lines = proxyPorts
```





## <a name="requirements"></a><span data-ttu-id="f69b7-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f69b7-121">Requirements</span></span>



| <span data-ttu-id="f69b7-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f69b7-122">Requirement</span></span> | <span data-ttu-id="f69b7-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="f69b7-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f69b7-124">Version</span><span class="sxs-lookup"><span data-stu-id="f69b7-124">Version</span></span><br/>   | <span data-ttu-id="f69b7-125">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="f69b7-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="f69b7-126">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f69b7-126">Namespace</span></span><br/> | <span data-ttu-id="f69b7-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="f69b7-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f69b7-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="f69b7-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f69b7-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f69b7-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f69b7-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f69b7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f69b7-131">**Interface IWMPNetwork (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="f69b7-131">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f69b7-132">**IWMPNetwork. getProxySettings (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="f69b7-132">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f69b7-133">**IWMPNetwork. setProxyPort (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="f69b7-133">**IWMPNetwork.setProxyPort (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxyport--vb-and-c.md)
</dt> </dl>

 

 





