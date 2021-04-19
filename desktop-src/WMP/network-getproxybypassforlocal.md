---
title: Méthode Network. getProxyBypassForLocal
description: La méthode getProxyBypassForLocal récupère une valeur qui indique si le serveur proxy est contourné si le serveur d’origine se trouve sur un réseau local.
ms.assetid: e5217d56-da22-4424-94b0-400369410b47
keywords:
- méthode getProxyBypassForLocal lecteur Windows Media
- méthode getProxyBypassForLocal lecteur Windows Media, classe réseau
- Classe réseau lecteur Windows Media, méthode getProxyBypassForLocal
topic_type:
- apiref
api_name:
- Network.getProxyBypassForLocal
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c60b9248cd5a893496c2de88c5a5370dfb7bf82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523588"
---
# <a name="networkgetproxybypassforlocal-method"></a><span data-ttu-id="6e49a-106">Méthode Network. getProxyBypassForLocal</span><span class="sxs-lookup"><span data-stu-id="6e49a-106">Network.getProxyBypassForLocal method</span></span>

<span data-ttu-id="6e49a-107">La méthode **getProxyBypassForLocal** récupère une valeur qui indique si le serveur proxy est contourné si le serveur d’origine se trouve sur un réseau local.</span><span class="sxs-lookup"><span data-stu-id="6e49a-107">The **getProxyBypassForLocal** method retrieves a value indicating whether the proxy server is bypassed if the origin server is on a local network.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e49a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6e49a-108">Syntax</span></span>


```JScript
bRetVal = Network.getProxyBypassForLocal(
  protocol
)
```



## <a name="parameters"></a><span data-ttu-id="6e49a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6e49a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e49a-110">*protocole* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6e49a-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e49a-111">**Chaîne** spécifiant le nom du protocole.</span><span class="sxs-lookup"><span data-stu-id="6e49a-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="6e49a-112">Pour obtenir la liste des protocoles pris en charge, consultez [protocoles et types de fichiers pris en charge](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="6e49a-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e49a-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6e49a-113">Return value</span></span>

<span data-ttu-id="6e49a-114">Cette méthode retourne une **valeur booléenne** indiquant si le serveur proxy est contourné.</span><span class="sxs-lookup"><span data-stu-id="6e49a-114">This method returns a **Boolean** indicating whether the proxy server is bypassed.</span></span> <span data-ttu-id="6e49a-115">La valeur retournée est significative uniquement lorsque **getProxySettings** retourne une valeur de deux (utilisez des paramètres manuels).</span><span class="sxs-lookup"><span data-stu-id="6e49a-115">The value returned is meaningful only when **getProxySettings** returns a value of two (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="6e49a-116">Notes</span><span class="sxs-lookup"><span data-stu-id="6e49a-116">Remarks</span></span>

<span data-ttu-id="6e49a-117">Cette méthode échoue sauf si l’application appelante est en cours d’exécution sur l’ordinateur local ou sur l’intranet.</span><span class="sxs-lookup"><span data-stu-id="6e49a-117">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="6e49a-118">**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="6e49a-118">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="6e49a-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="6e49a-119">Examples</span></span>

<span data-ttu-id="6e49a-120">L’exemple JScript suivant utilise le *réseau*. **getProxyBypassForLocal** pour afficher si le lecteur Windows Media est configuré pour ignorer le serveur proxy pour les adresses locales.</span><span class="sxs-lookup"><span data-stu-id="6e49a-120">The following JScript example uses *Network*.**getProxyBypassForLocal** to display whether Windows Media Player is set to bypass the proxy server for local addresses.</span></span> <span data-ttu-id="6e49a-121">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="6e49a-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy bypass for local value for HTTP.
   var proxyBypassForLocalHTTP = Player.network.getProxyBypassForLocal("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy bypass for local value for MMS.
   var proxyBypassForLocalMMS = Player.network.getProxyBypassForLocal("MMS");

// Display the proxy bypass for local values in the browser client area.
// Unavailable proxy bypass for local values will display as "undefined".
document.write("The current HTTP proxy bypass for local value: " + proxyBypassForLocalHTTP);
document.write("<BR>");
document.write("The current MMS proxy bypass for local value: " + proxyBypassForLocalMMS);

```



## <a name="requirements"></a><span data-ttu-id="6e49a-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6e49a-122">Requirements</span></span>



| <span data-ttu-id="6e49a-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6e49a-123">Requirement</span></span> | <span data-ttu-id="6e49a-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="6e49a-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6e49a-125">Version</span><span class="sxs-lookup"><span data-stu-id="6e49a-125">Version</span></span><br/> | <span data-ttu-id="6e49a-126">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="6e49a-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="6e49a-127">DLL</span><span class="sxs-lookup"><span data-stu-id="6e49a-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="6e49a-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e49a-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e49a-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e49a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e49a-130">**Objet réseau**</span><span class="sxs-lookup"><span data-stu-id="6e49a-130">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="6e49a-131">**Network. getProxySettings**</span><span class="sxs-lookup"><span data-stu-id="6e49a-131">**Network.getProxySettings**</span></span>](network-getproxysettings.md)
</dt> </dl>

 

 





