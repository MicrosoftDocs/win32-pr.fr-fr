---
title: Méthode IWMPNetwork getProxyExceptionList
description: La méthode getProxyExceptionList retourne la liste des exceptions du proxy.
ms.assetid: 1b209d75-0fa7-420e-831c-160f3826cf3a
keywords:
- méthode getProxyExceptionList lecteur Windows Media
- méthode getProxyExceptionList lecteur Windows Media, interface IWMPNetwork
- Interface IWMPNetwork lecteur Windows Media, méthode getProxyExceptionList
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxyExceptionList
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 402e3b28d5423314b499213c9ddb02bca482d629
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528389"
---
# <a name="iwmpnetworkgetproxyexceptionlist-method"></a><span data-ttu-id="eb1e9-106">IWMPNetwork :: getProxyExceptionList, méthode</span><span class="sxs-lookup"><span data-stu-id="eb1e9-106">IWMPNetwork::getProxyExceptionList method</span></span>

<span data-ttu-id="eb1e9-107">La méthode **getProxyExceptionList** retourne la liste des exceptions du proxy.</span><span class="sxs-lookup"><span data-stu-id="eb1e9-107">The **getProxyExceptionList** method returns the proxy exception list.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb1e9-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb1e9-108">Syntax</span></span>


```CSharp
public System.String getProxyExceptionList(
  System.String bstrProtocol
);
```


```VB

Public Function getProxyExceptionList( _
  ByVal bstrProtocol As System.String _
) As System.String
Implements IWMPNetwork.getProxyExceptionList
```





## <a name="parameters"></a><span data-ttu-id="eb1e9-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eb1e9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb1e9-110">*bstrProtocol* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eb1e9-110">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb1e9-111">**System. String** qui est le nom de protocole.</span><span class="sxs-lookup"><span data-stu-id="eb1e9-111">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="eb1e9-112">Pour obtenir la liste des protocoles pris en charge, consultez [protocoles et types de fichiers pris en charge](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="eb1e9-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb1e9-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eb1e9-113">Return value</span></span>

<span data-ttu-id="eb1e9-114">**System. String** qui est une liste délimitée par des points-virgules des hôtes pour lesquels le serveur proxy est contourné.</span><span class="sxs-lookup"><span data-stu-id="eb1e9-114">A **System.String** that is a semicolon-delimited list of hosts for which the proxy server is bypassed.</span></span> <span data-ttu-id="eb1e9-115">La valeur est significative uniquement lorsque **IWMPNetwork. getProxySettings** retourne la valeur 2 (utiliser des paramètres manuels).</span><span class="sxs-lookup"><span data-stu-id="eb1e9-115">The value is meaningful only when **IWMPNetwork.getProxySettings** returns a value of 2 (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="eb1e9-116">Notes</span><span class="sxs-lookup"><span data-stu-id="eb1e9-116">Remarks</span></span>

<span data-ttu-id="eb1e9-117">Il s’agit d’une liste d’ordinateurs, de domaines et/ou d’adresses qui contournent le serveur proxy lorsque la partie hôte de l’URL cible correspond à une entrée de la liste.</span><span class="sxs-lookup"><span data-stu-id="eb1e9-117">This is a list of computers, domains, and/or addresses that will bypass the proxy server when the host portion of the target URL matches an entry in the list.</span></span>

<span data-ttu-id="eb1e9-118">Le \* caractère peut être utilisé comme caractère générique pour répertorier les entrées.</span><span class="sxs-lookup"><span data-stu-id="eb1e9-118">The \* character can be used as a wildcard character for listing entries.</span></span> <span data-ttu-id="eb1e9-119">Par exemple, \* . com correspond à tous les ordinateurs hôtes du domaine com, tandis que 67. \* correspond à tous les hôtes de la classe 67 d’un sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="eb1e9-119">For example, \*.com would match all hosts in the com domain, while 67.\* would match all hosts in the 67 class A subnet.</span></span>

<span data-ttu-id="eb1e9-120">Cette méthode échoue sauf si l’application appelante est en cours d’exécution sur l’ordinateur local ou sur l’intranet.</span><span class="sxs-lookup"><span data-stu-id="eb1e9-120">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="eb1e9-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="eb1e9-121">Examples</span></span>

<span data-ttu-id="eb1e9-122">L’exemple de code suivant utilise **getProxyExceptionList** pour indiquer si le lecteur Windows Media est configuré pour ignorer le serveur proxy pour les adresses locales.</span><span class="sxs-lookup"><span data-stu-id="eb1e9-122">The following code example uses **getProxyExceptionList** to display whether Windows Media Player is set to bypass the proxy server for local addresses.</span></span> <span data-ttu-id="eb1e9-123">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="eb1e9-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// String values to hold the results of calls to getProxyExceptionList. 
string proxyExceptionListHTTP = "";
string proxyExceptionListMMS = "";

// Test whether the HTTP proxy settings are manual.
if (player.network.getProxySettings("HTTP") == 2)
{
    proxyExceptionListHTTP = player.network.getProxyExceptionList("HTTP");
}

// Test whether the MMS proxy settings are manual.
if (player.network.getProxySettings("MMS") == 2)
{
    proxyExceptionListMMS = player.network.getProxyExceptionList("MMS");
}

// Store the proxy exception lists in a string array and display them
// using a multi-line text box. Unavailable exception lists will display
// as "undefined".
proxyExList[0] = ("The current HTTP proxy exception list: " + proxyExceptionListHTTP);
proxyExList[1] = ("The current MMS proxy exception list: " + proxyExceptionListMMS);
proxyExceptionListText.Lines = proxyExList;
```


```VB

' String values to hold the results of calls to getProxyExceptionList. 
Dim proxyExceptionListHTTP As String = &quot;&quot;
Dim proxyExceptionListMMS As String = &quot;&quot;

&#39; Test whether the HTTP proxy settings are manual.
If (player.network.getProxySettings(&quot;HTTP&quot;) = 2) Then

    proxyExceptionListHTTP = player.network.getProxyExceptionList(&quot;HTTP&quot;)

End If

&#39; Test whether the MMS proxy settings are manual.
If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

    proxyExceptionListMMS = player.network.getProxyExceptionList(&quot;MMS&quot;)

End If

&#39; Store the proxy exception lists in a string array and display them
&#39; using a multi-line text box. Unavailable exception lists will display
&#39; as &quot;undefined&quot;.
proxyExList(0) = (&quot;The current HTTP proxy exception list: &quot; + proxyExceptionListHTTP)
proxyExList(1) = (&quot;The current MMS proxy exception list: &quot; + proxyExceptionListMMS)
proxyExceptionList.Lines = proxyExList
```





## <a name="requirements"></a><span data-ttu-id="eb1e9-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb1e9-124">Requirements</span></span>



| <span data-ttu-id="eb1e9-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb1e9-125">Requirement</span></span> | <span data-ttu-id="eb1e9-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb1e9-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb1e9-127">Version</span><span class="sxs-lookup"><span data-stu-id="eb1e9-127">Version</span></span><br/>   | <span data-ttu-id="eb1e9-128">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="eb1e9-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="eb1e9-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="eb1e9-129">Namespace</span></span><br/> | <span data-ttu-id="eb1e9-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="eb1e9-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="eb1e9-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="eb1e9-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="eb1e9-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="eb1e9-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb1e9-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb1e9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb1e9-134">**Interface IWMPNetwork (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="eb1e9-134">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="eb1e9-135">**IWMPNetwork. getProxySettings (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="eb1e9-135">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="eb1e9-136">**IWMPNetwork. setProxyExceptionList (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="eb1e9-136">**IWMPNetwork.setProxyExceptionList (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxyexceptionlist--vb-and-c.md)
</dt> </dl>

 

 





