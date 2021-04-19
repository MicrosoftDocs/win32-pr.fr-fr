---
title: Méthode IWMPNetwork getProxyBypassForLocal
description: La méthode getProxyBypassForLocal retourne une valeur qui indique si le serveur proxy est contourné si le serveur d’origine se trouve sur un réseau local.
ms.assetid: 150a05f3-6979-4a88-a617-472f07d38807
keywords:
- méthode getProxyBypassForLocal lecteur Windows Media
- méthode getProxyBypassForLocal lecteur Windows Media, interface IWMPNetwork
- Interface IWMPNetwork lecteur Windows Media, méthode getProxyBypassForLocal
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxyBypassForLocal
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b87b1f00432ec91dd4379a9fa5e31664437afe0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525247"
---
# <a name="iwmpnetworkgetproxybypassforlocal-method"></a><span data-ttu-id="3bfcb-106">IWMPNetwork :: getProxyBypassForLocal, méthode</span><span class="sxs-lookup"><span data-stu-id="3bfcb-106">IWMPNetwork::getProxyBypassForLocal method</span></span>

<span data-ttu-id="3bfcb-107">La méthode **getProxyBypassForLocal** retourne une valeur qui indique si le serveur proxy est contourné si le serveur d’origine se trouve sur un réseau local.</span><span class="sxs-lookup"><span data-stu-id="3bfcb-107">The **getProxyBypassForLocal** method returns a value indicating whether the proxy server is bypassed if the origin server is on a local network.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bfcb-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3bfcb-108">Syntax</span></span>


```CSharp
public System.Boolean getProxyBypassForLocal(
  System.String bstrProtocol
);
```


```VB

Public Function getProxyBypassForLocal( _
  ByVal bstrProtocol As System.String _
) As System.Boolean
Implements IWMPNetwork.getProxyBypassForLocal
```





## <a name="parameters"></a><span data-ttu-id="3bfcb-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3bfcb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bfcb-110">*bstrProtocol*</span><span class="sxs-lookup"><span data-stu-id="3bfcb-110">*bstrProtocol*</span></span> 
</dt> <dd>

<span data-ttu-id="3bfcb-111">**System. String** qui est le nom de protocole.</span><span class="sxs-lookup"><span data-stu-id="3bfcb-111">A **System.String** that is the protocol name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bfcb-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3bfcb-112">Return value</span></span>

<span data-ttu-id="3bfcb-113">Valeur **System. Boolean** qui indique si le serveur proxy est contourné.</span><span class="sxs-lookup"><span data-stu-id="3bfcb-113">A **System.Boolean** value that indicates whether the proxy server is bypassed.</span></span> <span data-ttu-id="3bfcb-114">La valeur est significative uniquement lorsque **IWMPNetwork. getProxySettings** retourne la valeur 2 (utiliser des paramètres manuels).</span><span class="sxs-lookup"><span data-stu-id="3bfcb-114">The value is meaningful only when **IWMPNetwork.getProxySettings** returns a value of 2 (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="3bfcb-115">Notes</span><span class="sxs-lookup"><span data-stu-id="3bfcb-115">Remarks</span></span>

<span data-ttu-id="3bfcb-116">Cette méthode échoue sauf si l’application appelante est en cours d’exécution sur l’ordinateur local ou sur l’intranet.</span><span class="sxs-lookup"><span data-stu-id="3bfcb-116">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="3bfcb-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="3bfcb-117">Examples</span></span>

<span data-ttu-id="3bfcb-118">L’exemple de code suivant utilise **getProxyBypassForLocal** pour indiquer si le lecteur Windows Media est configuré pour ignorer le serveur proxy pour les adresses locales.</span><span class="sxs-lookup"><span data-stu-id="3bfcb-118">The following code example uses **getProxyBypassForLocal** to display whether Windows Media Player is set to bypass the proxy server for local addresses.</span></span> <span data-ttu-id="3bfcb-119">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="3bfcb-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```VB
' Boolean values to hold the results of calls to getProxyBypassForLocal. 
Dim proxyBypassForLocalHTTP As Boolean = False
Dim proxyBypassForLocalMMS As Boolean = False

' Test whether the HTTP proxy settings are manual.
If (player.network.getProxySettings("HTTP") = 2) Then

    proxyBypassForLocalHTTP = player.network.getProxyBypassForLocal("HTTP")

End If

' Test whether the MMS proxy settings are manual.
If (player.network.getProxySettings("MMS") = 2) Then

    proxyBypassForLocalMMS = player.network.getProxyBypassForLocal("MMS")

End If

' Store the proxy bypass for local values in a string array and display them
' using a multi-line text box. Unavailable proxy bypass for local values will display
' as "undefined".
proxyInfo(0) = ("The current HTTP proxy bypass for local value: " + proxyBypassForLocalHTTP.ToString())
proxyInfo(1) = ("The current MMS proxy bypass for local value: " + proxyBypassForLocalMMS.ToString())
proxyBypassText.Lines = proxyInfo
```


```CSharp

// Boolean values to hold the results of calls to getProxyBypassForLocal. 
bool proxyBypassForLocalHTTP = false;
bool proxyBypassForLocalMMS = false;

// Test whether the HTTP proxy settings are manual.
if (player.network.getProxySettings(&quot;HTTP&quot;) == 2)
{
    proxyBypassForLocalHTTP = player.network.getProxyBypassForLocal(&quot;HTTP&quot;);
}

// Test whether the MMS proxy settings are manual.
if (player.network.getProxySettings(&quot;MMS&quot;) == 2)
{
   proxyBypassForLocalMMS = player.network.getProxyBypassForLocal(&quot;MMS&quot;);
}

// Store the proxy bypass for local values in a string array and display them
// using a multi-line text box. Unavailable proxy bypass for local values will display
// as &quot;undefined&quot;.
proxyInfo[0] = (&quot;The current HTTP proxy bypass for local value: &quot; + proxyBypassForLocalHTTP.ToString());
proxyInfo[1] = (&quot;The current MMS proxy bypass for local value: &quot; + proxyBypassForLocalMMS.ToString());
proxyBypassText.Lines = proxyInfo;
```





## <a name="requirements"></a><span data-ttu-id="3bfcb-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3bfcb-120">Requirements</span></span>



| <span data-ttu-id="3bfcb-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3bfcb-121">Requirement</span></span> | <span data-ttu-id="3bfcb-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="3bfcb-122">Value</span></span> |
|----------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bfcb-123">Version</span><span class="sxs-lookup"><span data-stu-id="3bfcb-123">Version</span></span><br/>   | <span data-ttu-id="3bfcb-124">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="3bfcb-124">Windows Media Player 9 Series or later</span></span><br/>                                             |
| <span data-ttu-id="3bfcb-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3bfcb-125">Namespace</span></span><br/> | <span data-ttu-id="3bfcb-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="3bfcb-126">**WMPLib**</span></span><br/>                                                                         |
| <span data-ttu-id="3bfcb-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="3bfcb-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3bfcb-128"><dt>Interop.WMPLib.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3bfcb-128"><dt>Interop.WMPLib.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bfcb-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3bfcb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bfcb-130">**Interface IWMPNetwork (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="3bfcb-130">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3bfcb-131">**IWMPNetwork. getProxySettings (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="3bfcb-131">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3bfcb-132">**IWMPNetwork. setProxyBypassForLocal (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="3bfcb-132">**IWMPNetwork.setProxyBypassForLocal (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxybypassforlocal--vb-and-c.md)
</dt> </dl>

 

 





