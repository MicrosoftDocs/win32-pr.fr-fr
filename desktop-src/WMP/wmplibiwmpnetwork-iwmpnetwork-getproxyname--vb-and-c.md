---
title: Méthode IWMPNetwork getProxyName
description: La méthode getProxyName retourne le nom du serveur proxy utilisé.
ms.assetid: 69396b01-1da7-450c-b229-0cc4fb832ae9
keywords:
- méthode getProxyName lecteur Windows Media
- méthode getProxyName lecteur Windows Media, interface IWMPNetwork
- Interface IWMPNetwork lecteur Windows Media, méthode getProxyName
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxyName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e5e05b6552e5e6a922cf02037a0bfc4956bfc28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539551"
---
# <a name="iwmpnetworkgetproxyname-method"></a><span data-ttu-id="82663-106">IWMPNetwork :: getProxyName, méthode</span><span class="sxs-lookup"><span data-stu-id="82663-106">IWMPNetwork::getProxyName method</span></span>

<span data-ttu-id="82663-107">La méthode **getProxyName** retourne le nom du serveur proxy utilisé.</span><span class="sxs-lookup"><span data-stu-id="82663-107">The **getProxyName** method returns the name of the proxy server being used.</span></span>

## <a name="syntax"></a><span data-ttu-id="82663-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="82663-108">Syntax</span></span>


```CSharp
public System.String getProxyName(
  System.String bstrProtocol
);
```


```VB

Public Function getProxyName( _
  ByVal bstrProtocol As System.String _
) As System.String
Implements IWMPNetwork.getProxyName
```





## <a name="parameters"></a><span data-ttu-id="82663-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="82663-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82663-110">*bstrProtocol* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="82663-110">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82663-111">**System. String** qui est le nom de protocole.</span><span class="sxs-lookup"><span data-stu-id="82663-111">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="82663-112">Pour obtenir la liste des protocoles pris en charge, consultez [protocoles et types de fichiers pris en charge](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="82663-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82663-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="82663-113">Return value</span></span>

<span data-ttu-id="82663-114">**System. String** qui est le nom du serveur proxy utilisé.</span><span class="sxs-lookup"><span data-stu-id="82663-114">A **System.String** that is the name of the proxy server being used.</span></span> <span data-ttu-id="82663-115">La valeur est significative uniquement lorsque **IWMPNetwork. getProxySettings** retourne la valeur 2 (utiliser des paramètres manuels).</span><span class="sxs-lookup"><span data-stu-id="82663-115">The value is meaningful only when **IWMPNetwork.getProxySettings** returns a value of 2 (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="82663-116">Notes</span><span class="sxs-lookup"><span data-stu-id="82663-116">Remarks</span></span>

<span data-ttu-id="82663-117">Cette méthode échoue sauf si l’application appelante est en cours d’exécution sur l’ordinateur local ou sur l’intranet.</span><span class="sxs-lookup"><span data-stu-id="82663-117">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="82663-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="82663-118">Examples</span></span>

<span data-ttu-id="82663-119">L’exemple de code suivant utilise **getProxyName** pour afficher les noms des serveurs proxy du lecteur Windows Media pour les protocoles HTTP et MMS.</span><span class="sxs-lookup"><span data-stu-id="82663-119">The following code example uses **getProxyName** to display the Windows Media Player proxy server names for the HTTP and MMS protocols.</span></span> <span data-ttu-id="82663-120">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="82663-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// String values to hold the results of calls to getProxyExceptionList. 
string proxyNameHTTP = "";
string proxyNameMMS = "";

// Test whether the HTTP proxy settings are manual.
if (player.network.getProxySettings("HTTP") == 2)
{
    proxyNameHTTP = player.network.getProxyName("HTTP");
}

// Test whether the MMS proxy settings are manual.
if (player.network.getProxySettings("MMS") == 2)
{
    proxyNameMMS = player.network.getProxyName("MMS");
}

// Store the proxy server names in a string array and display them using a multi-line
// text box. Unavailable proxy server names will display as "undefined".
proxyNames[0] = ("The current HTTP proxy server name is: " + proxyNameHTTP);
proxyNames[1] = ("The current MMS proxy server name is: " + proxyNameMMS);
proxyNameText.Lines = proxyNames;
```


```VB

' String values to hold the results of calls to getProxyExceptionList. 
Dim proxyNameHTTP As String = &quot;&quot;
Dim proxyNameMMS As String = &quot;&quot;

&#39; Test whether the HTTP proxy settings are manual.
If (player.network.getProxySettings(&quot;HTTP&quot;) = 2) Then

    proxyNameHTTP = player.network.getProxyName(&quot;HTTP&quot;)

End If

&#39; Test whether the MMS proxy settings are manual.
If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

    proxyNameMMS = player.network.getProxyName(&quot;MMS&quot;)

End If

&#39; Store the proxy server names in a string array and display them using a multi-line
&#39; text box. Unavailable proxy server names will display as &quot;undefined&quot;.
proxyNames(0) = (&quot;The current HTTP proxy server name is: &quot; + proxyNameHTTP)
proxyNames(1) = (&quot;The current MMS proxy server name is: &quot; + proxyNameMMS)
proxyNameText.Lines = proxyNames
```





## <a name="requirements"></a><span data-ttu-id="82663-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="82663-121">Requirements</span></span>



| <span data-ttu-id="82663-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="82663-122">Requirement</span></span> | <span data-ttu-id="82663-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="82663-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82663-124">Version</span><span class="sxs-lookup"><span data-stu-id="82663-124">Version</span></span><br/>   | <span data-ttu-id="82663-125">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="82663-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="82663-126">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="82663-126">Namespace</span></span><br/> | <span data-ttu-id="82663-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="82663-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="82663-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="82663-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="82663-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="82663-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82663-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82663-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82663-131">**Interface IWMPNetwork (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="82663-131">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="82663-132">**IWMPNetwork. getProxySettings (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="82663-132">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="82663-133">**IWMPNetwork. setProxyName (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="82663-133">**IWMPNetwork.setProxyName (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxyname--vb-and-c.md)
</dt> </dl>

 

 





