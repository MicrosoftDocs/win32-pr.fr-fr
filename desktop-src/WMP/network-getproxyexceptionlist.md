---
title: Méthode Network. getProxyExceptionList
description: La méthode getProxyExceptionList récupère la liste des exceptions du proxy.
ms.assetid: f81d8c0f-cc75-470c-9c24-ceaf8a4b6f97
keywords:
- méthode getProxyExceptionList lecteur Windows Media
- méthode getProxyExceptionList lecteur Windows Media, classe réseau
- Classe réseau lecteur Windows Media, méthode getProxyExceptionList
topic_type:
- apiref
api_name:
- Network.getProxyExceptionList
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34ace9bd569c1cc53a8f3d522703aee6154e68a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533194"
---
# <a name="networkgetproxyexceptionlist-method"></a><span data-ttu-id="e5252-106">Méthode Network. getProxyExceptionList</span><span class="sxs-lookup"><span data-stu-id="e5252-106">Network.getProxyExceptionList method</span></span>

<span data-ttu-id="e5252-107">La méthode **getProxyExceptionList** récupère la liste des exceptions du proxy.</span><span class="sxs-lookup"><span data-stu-id="e5252-107">The **getProxyExceptionList** method retrieves the proxy exception list.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5252-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e5252-108">Syntax</span></span>


```JScript
strRetVal = Network.getProxyExceptionList(
  protocol
)
```



## <a name="parameters"></a><span data-ttu-id="e5252-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e5252-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5252-110">*protocole* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e5252-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5252-111">**Chaîne** spécifiant le nom du protocole.</span><span class="sxs-lookup"><span data-stu-id="e5252-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="e5252-112">Pour obtenir la liste des protocoles pris en charge, consultez [protocoles et types de fichiers pris en charge](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="e5252-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5252-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e5252-113">Return value</span></span>

<span data-ttu-id="e5252-114">Cette méthode retourne une **chaîne** spécifiant une liste délimitée par des points-virgules des hôtes pour lesquels le serveur proxy est contourné.</span><span class="sxs-lookup"><span data-stu-id="e5252-114">This method returns a **String** specifying a semicolon-delimited list of hosts for which the proxy server is bypassed.</span></span> <span data-ttu-id="e5252-115">La valeur retournée est significative uniquement lorsque **getProxySettings** retourne une valeur de deux (utilisez des paramètres manuels).</span><span class="sxs-lookup"><span data-stu-id="e5252-115">The value returned is meaningful only when **getProxySettings** returns a value of two (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="e5252-116">Notes</span><span class="sxs-lookup"><span data-stu-id="e5252-116">Remarks</span></span>

<span data-ttu-id="e5252-117">Il s’agit d’une liste d’ordinateurs, de domaines et/ou d’adresses qui contournent le serveur proxy lorsque la partie hôte de l’URL cible correspond à une entrée de la liste.</span><span class="sxs-lookup"><span data-stu-id="e5252-117">This is a list of computers, domains, and/or addresses that will bypass the proxy server when the host portion of the target URL matches an entry in the list.</span></span>

<span data-ttu-id="e5252-118">Le \* caractère peut être utilisé comme caractère générique pour répertorier les entrées.</span><span class="sxs-lookup"><span data-stu-id="e5252-118">The \* character can be used as a wildcard for listing entries.</span></span> <span data-ttu-id="e5252-119">Par exemple, \* . com correspond à tous les ordinateurs hôtes du domaine com alors que 67. \* correspond à tous les hôtes de la classe 67 d’un sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="e5252-119">For example, \*.com would match all hosts in the com domain while 67.\* would match all hosts in the 67 class A subnet.</span></span>

<span data-ttu-id="e5252-120">Cette méthode échoue sauf si l’application appelante est en cours d’exécution sur l’ordinateur local ou sur l’intranet.</span><span class="sxs-lookup"><span data-stu-id="e5252-120">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="e5252-121">**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="e5252-121">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="e5252-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="e5252-122">Examples</span></span>

<span data-ttu-id="e5252-123">L’exemple JScript suivant utilise le *réseau*. **getProxyExceptionList** pour afficher les listes de proxys ignorés pour les protocoles MMS et http.</span><span class="sxs-lookup"><span data-stu-id="e5252-123">The following JScript example uses *Network*.**getProxyExceptionList** to display the lists of bypassed proxies for the MMS and HTTP protocols.</span></span> <span data-ttu-id="e5252-124">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="e5252-124">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy exception list for HTTP.
   var proxyExceptionListHTTP = Player.network.getProxyExceptionList("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy exception list for MMS.
   var proxyExceptionListMMS = Player.network.getProxyExceptionList("MMS");

// Display the proxy exception lists in the browser client area.
// Unavailable proxy exception lists will display as "undefined".
document.write("The current HTTP proxy exception list: " + proxyExceptionListHTTP);
document.write("<BR>");
document.write("The current MMS proxy exception list: " + proxyExceptionListMMS);

```



## <a name="requirements"></a><span data-ttu-id="e5252-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e5252-125">Requirements</span></span>



| <span data-ttu-id="e5252-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e5252-126">Requirement</span></span> | <span data-ttu-id="e5252-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="e5252-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e5252-128">Version</span><span class="sxs-lookup"><span data-stu-id="e5252-128">Version</span></span><br/> | <span data-ttu-id="e5252-129">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="e5252-129">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="e5252-130">DLL</span><span class="sxs-lookup"><span data-stu-id="e5252-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="e5252-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5252-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5252-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5252-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5252-133">**Objet réseau**</span><span class="sxs-lookup"><span data-stu-id="e5252-133">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="e5252-134">**Network. getProxySettings**</span><span class="sxs-lookup"><span data-stu-id="e5252-134">**Network.getProxySettings**</span></span>](network-getproxysettings.md)
</dt> </dl>

 

 





