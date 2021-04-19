---
title: Méthode IWMPNetwork setProxyExceptionList
description: La méthode setProxyExceptionList spécifie la liste des exceptions du proxy. | Méthode IWMPNetwork setProxyExceptionList
ms.assetid: a7a5e9ad-f71f-431e-9a53-b56456778104
keywords:
- méthode setProxyExceptionList lecteur Windows Media
- méthode setProxyExceptionList lecteur Windows Media, interface IWMPNetwork
- Interface IWMPNetwork lecteur Windows Media, méthode setProxyExceptionList
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxyExceptionList
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dad011dee8e1199e6111be60acfec41d85d1e58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537925"
---
# <a name="iwmpnetworksetproxyexceptionlist-method"></a><span data-ttu-id="c313c-107">IWMPNetwork :: setProxyExceptionList, méthode</span><span class="sxs-lookup"><span data-stu-id="c313c-107">IWMPNetwork::setProxyExceptionList method</span></span>

<span data-ttu-id="c313c-108">La méthode **setProxyExceptionList** spécifie la liste des exceptions du proxy.</span><span class="sxs-lookup"><span data-stu-id="c313c-108">The **setProxyExceptionList** method specifies the proxy exception list.</span></span>

## <a name="syntax"></a><span data-ttu-id="c313c-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c313c-109">Syntax</span></span>


```CSharp
public void setProxyExceptionList(
  System.String bstrProtocol,
  System.String pbstrExceptionList
);
```


```VB

Public Sub setProxyExceptionList( _
  ByVal bstrProtocol As System.String, _
  ByVal pbstrExceptionList As System.String _
)
Implements IWMPNetwork.setProxyExceptionList
```





## <a name="parameters"></a><span data-ttu-id="c313c-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c313c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c313c-111">*bstrProtocol* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c313c-111">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c313c-112">**System. String** qui est le nom de protocole.</span><span class="sxs-lookup"><span data-stu-id="c313c-112">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="c313c-113">Pour obtenir la liste des protocoles pris en charge, consultez [protocoles et types de fichiers pris en charge](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="c313c-113">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="c313c-114">*pbstrExceptionList* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c313c-114">*pbstrExceptionList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c313c-115">**System. String** qui est une liste délimitée par des points-virgules des hôtes pour lesquels le serveur proxy est contourné.</span><span class="sxs-lookup"><span data-stu-id="c313c-115">A **System.String** that is a semicolon-delimited list of hosts for which the proxy server is bypassed.</span></span> <span data-ttu-id="c313c-116">Les espaces de début et de fin ne doivent pas être présents.</span><span class="sxs-lookup"><span data-stu-id="c313c-116">Leading and trailing spaces should not be present.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c313c-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c313c-117">Return value</span></span>

<span data-ttu-id="c313c-118">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c313c-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c313c-119">Notes</span><span class="sxs-lookup"><span data-stu-id="c313c-119">Remarks</span></span>

<span data-ttu-id="c313c-120">Il s’agit d’une liste d’ordinateurs, de domaines et/ou d’adresses qui contournent le serveur proxy lorsque la partie hôte de l’URL cible correspond à une entrée de la liste.</span><span class="sxs-lookup"><span data-stu-id="c313c-120">This is a list of computers, domains, and/or addresses that will bypass the proxy server when the host portion of the target URL matches an entry in the list.</span></span>

<span data-ttu-id="c313c-121">Le \* caractère peut être utilisé comme caractère générique pour répertorier les entrées.</span><span class="sxs-lookup"><span data-stu-id="c313c-121">The \* character can be used as a wildcard character for listing entries.</span></span> <span data-ttu-id="c313c-122">Par exemple, \* . com correspond à tous les ordinateurs hôtes du domaine com, tandis que 67. \* correspond à tous les hôtes de la classe 67 d’un sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="c313c-122">For example, \*.com would match all hosts in the com domain, while 67.\* would match all hosts in the 67 class A subnet.</span></span>

<span data-ttu-id="c313c-123">Cette méthode n’a aucun effet, sauf si la valeur récupérée à partir de **IWMPNetwork. getProxySettings** est 2 (utiliser des paramètres manuels).</span><span class="sxs-lookup"><span data-stu-id="c313c-123">This method has no effect unless the value retrieved from **IWMPNetwork.getProxySettings** is 2 (use manual settings).</span></span>

<span data-ttu-id="c313c-124">Cette méthode échoue sauf si l’application appelante est en cours d’exécution sur l’ordinateur local ou sur l’intranet.</span><span class="sxs-lookup"><span data-stu-id="c313c-124">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="c313c-125">Exemples</span><span class="sxs-lookup"><span data-stu-id="c313c-125">Examples</span></span>

<span data-ttu-id="c313c-126">L’exemple de code suivant utilise **setProxyExceptionList** pour spécifier une liste d’hôtes pour lesquels le serveur proxy est contourné lors de l’utilisation du protocole MMS.</span><span class="sxs-lookup"><span data-stu-id="c313c-126">The following code example uses **setProxyExceptionList** to specify a list of hosts for which the proxy server is bypassed when using the MMS protocol.</span></span> <span data-ttu-id="c313c-127">La nouvelle liste est récupérée à partir d’une zone de texte lorsque l’utilisateur clique sur un bouton.</span><span class="sxs-lookup"><span data-stu-id="c313c-127">The new list is retrieved from a text box when a button is clicked.</span></span> <span data-ttu-id="c313c-128">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="c313c-128">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setExList_Click(object sender, System.EventArgs e)
{
    // Test whether proxy settings are manual.
    if (player.network.getProxySettings("MMS") == 2)
    {
        // Store the user's new exception list.
        string proxyxlist = exListText.Text;

        // Set the exception list.
        player.network.setProxyExceptionList("MMS", proxyxlist);
    }
    else
    {
        // Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show("Proxy settings must be manual!");
    }
}
```


```VB

Public Sub setExList_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setExList.Click

    &#39; Test whether proxy settings are manual.
    If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

        &#39; Store the user&#39;s new exception list.
        Dim proxyxlist As String = exListText.Text

        &#39; Set the exception list.
        player.network.setProxyExceptionList(&quot;MMS&quot;, proxyxlist)

    Else

        &#39; Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show(&quot;Proxy settings must be manual!&quot;)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="c313c-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c313c-129">Requirements</span></span>



| <span data-ttu-id="c313c-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c313c-130">Requirement</span></span> | <span data-ttu-id="c313c-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="c313c-131">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c313c-132">Version</span><span class="sxs-lookup"><span data-stu-id="c313c-132">Version</span></span><br/>   | <span data-ttu-id="c313c-133">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="c313c-133">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="c313c-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c313c-134">Namespace</span></span><br/> | <span data-ttu-id="c313c-135">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="c313c-135">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="c313c-136">Assembly</span><span class="sxs-lookup"><span data-stu-id="c313c-136">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c313c-137"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c313c-137"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c313c-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c313c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c313c-139">**Interface IWMPNetwork (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="c313c-139">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c313c-140">**IWMPNetwork. getProxyExceptionList (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="c313c-140">**IWMPNetwork.getProxyExceptionList (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxyexceptionlist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c313c-141">**IWMPNetwork. getProxySettings (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="c313c-141">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





