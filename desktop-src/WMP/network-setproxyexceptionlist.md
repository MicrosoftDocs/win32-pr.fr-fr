---
title: Méthode Network. setProxyExceptionList
description: La méthode setProxyExceptionList spécifie la liste des exceptions du proxy. | Méthode Network. setProxyExceptionList
ms.assetid: c9eeb058-5ffb-4405-9bf2-776f120e2db4
keywords:
- méthode setProxyExceptionList lecteur Windows Media
- méthode setProxyExceptionList lecteur Windows Media, classe réseau
- Classe réseau lecteur Windows Media, méthode setProxyExceptionList
topic_type:
- apiref
api_name:
- Network.setProxyExceptionList
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1e48aa91ec4857181de5c607a586da42d6f2cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540151"
---
# <a name="networksetproxyexceptionlist-method"></a><span data-ttu-id="59583-107">Méthode Network. setProxyExceptionList</span><span class="sxs-lookup"><span data-stu-id="59583-107">Network.setProxyExceptionList method</span></span>

<span data-ttu-id="59583-108">La méthode **setProxyExceptionList** spécifie la liste des exceptions du proxy.</span><span class="sxs-lookup"><span data-stu-id="59583-108">The **setProxyExceptionList** method specifies the proxy exception list.</span></span>

## <a name="syntax"></a><span data-ttu-id="59583-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59583-109">Syntax</span></span>


```JScript
Network.setProxyExceptionList(
  protocol,
  list
)
```



## <a name="parameters"></a><span data-ttu-id="59583-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="59583-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59583-111">*protocole* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="59583-111">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59583-112">**Chaîne** spécifiant le nom du protocole.</span><span class="sxs-lookup"><span data-stu-id="59583-112">**String** specifying the protocol name.</span></span> <span data-ttu-id="59583-113">Pour obtenir la liste des protocoles pris en charge, consultez [protocoles et types de fichiers pris en charge](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="59583-113">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="59583-114">*liste* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="59583-114">*list* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59583-115">**Chaîne** spécifiant une liste délimitée par des points-virgules des hôtes pour lesquels le serveur proxy est contourné.</span><span class="sxs-lookup"><span data-stu-id="59583-115">**String** specifying a semicolon-delimited list of hosts for which the proxy server is bypassed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59583-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="59583-116">Return value</span></span>

<span data-ttu-id="59583-117">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="59583-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="59583-118">Notes</span><span class="sxs-lookup"><span data-stu-id="59583-118">Remarks</span></span>

<span data-ttu-id="59583-119">Il s’agit d’une liste d’ordinateurs, de domaines et/ou d’adresses qui contournent le serveur proxy lorsque la partie hôte de l’URL cible correspond à une entrée de la liste.</span><span class="sxs-lookup"><span data-stu-id="59583-119">This is a list of computers, domains, and/or addresses that will bypass the proxy server when the host portion of the target URL matches an entry in the list.</span></span>

<span data-ttu-id="59583-120">Le \* caractère peut être utilisé comme caractère générique pour répertorier les entrées.</span><span class="sxs-lookup"><span data-stu-id="59583-120">The \* character can be used as a wildcard for listing entries.</span></span> <span data-ttu-id="59583-121">Par exemple, \* . com correspond à tous les ordinateurs hôtes du domaine com, tandis que 67. \* correspond à tous les hôtes de la classe 67 d’un sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="59583-121">For example, \*.com would match all hosts in the com domain, while 67.\* would match all hosts in the 67 class A subnet.</span></span>

<span data-ttu-id="59583-122">Cette méthode n’a aucun effet, à moins que **getProxySettings** retourne la valeur 2 (utiliser des paramètres manuels).</span><span class="sxs-lookup"><span data-stu-id="59583-122">This method has no effect unless **getProxySettings** returns a value of 2 (use manual settings).</span></span>

<span data-ttu-id="59583-123">Cette méthode échoue sauf si l’application appelante est en cours d’exécution sur l’ordinateur local ou sur l’intranet.</span><span class="sxs-lookup"><span data-stu-id="59583-123">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="59583-124">**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="59583-124">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="59583-125">Exemples</span><span class="sxs-lookup"><span data-stu-id="59583-125">Examples</span></span>

<span data-ttu-id="59583-126">L’exemple JScript suivant utilise le *réseau*. **setProxyExceptionList** pour spécifier une liste d’hôtes pour lesquels le serveur proxy est contourné lors de l’utilisation du protocole MMS.</span><span class="sxs-lookup"><span data-stu-id="59583-126">The following JScript example uses *Network*.**setProxyExceptionList** to specify a list of hosts for which the proxy server is bypassed when using the MMS protocol.</span></span> <span data-ttu-id="59583-127">La nouvelle liste est récupérée à partir d’un élément de texte HTML avec ID = "XLIST".</span><span class="sxs-lookup"><span data-stu-id="59583-127">The new list is retrieved from an HTML TEXT element with ID = "XLIST".</span></span> <span data-ttu-id="59583-128">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="59583-128">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Store the user's new exception list.
   var proxyxlist = XLIST.value;

   // Set the exception list.
   Player.network.setProxyExceptionList("MMS", proxyxlist);
}

else

// Warn that the proxy settings must be set to 2.
alert("Proxy settings must be manual!");

```



## <a name="requirements"></a><span data-ttu-id="59583-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59583-129">Requirements</span></span>



| <span data-ttu-id="59583-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59583-130">Requirement</span></span> | <span data-ttu-id="59583-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="59583-131">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="59583-132">Version</span><span class="sxs-lookup"><span data-stu-id="59583-132">Version</span></span><br/> | <span data-ttu-id="59583-133">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="59583-133">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="59583-134">DLL</span><span class="sxs-lookup"><span data-stu-id="59583-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="59583-135"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59583-135"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59583-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59583-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59583-137">**Objet réseau**</span><span class="sxs-lookup"><span data-stu-id="59583-137">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





