---
title: Méthode Network. setProxyBypassForLocal
description: La méthode setProxyBypassForLocal spécifie une valeur qui indique si le serveur proxy est contourné si le serveur d’origine se trouve sur un réseau local.
ms.assetid: 3023a561-f3b7-45c8-a432-baadd795aaa6
keywords:
- méthode setProxyBypassForLocal lecteur Windows Media
- méthode setProxyBypassForLocal lecteur Windows Media, classe réseau
- Classe réseau lecteur Windows Media, méthode setProxyBypassForLocal
topic_type:
- apiref
api_name:
- Network.setProxyBypassForLocal
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9426c310c8977317cf5a8415fd19966b8dfc8fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532654"
---
# <a name="networksetproxybypassforlocal-method"></a><span data-ttu-id="c0534-106">Méthode Network. setProxyBypassForLocal</span><span class="sxs-lookup"><span data-stu-id="c0534-106">Network.setProxyBypassForLocal method</span></span>

<span data-ttu-id="c0534-107">La méthode **setProxyBypassForLocal** spécifie une valeur qui indique si le serveur proxy est contourné si le serveur d’origine se trouve sur un réseau local.</span><span class="sxs-lookup"><span data-stu-id="c0534-107">The **setProxyBypassForLocal** method specifies a value indicating whether the proxy server is bypassed if the origin server is on a local network.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0534-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0534-108">Syntax</span></span>


```JScript
Network.setProxyBypassForLocal(
  protocol,
  bypass
)
```



## <a name="parameters"></a><span data-ttu-id="c0534-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c0534-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0534-110">*protocole* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c0534-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0534-111">**Chaîne** spécifiant le nom du protocole.</span><span class="sxs-lookup"><span data-stu-id="c0534-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="c0534-112">Pour obtenir la liste des protocoles pris en charge, consultez [protocoles et types de fichiers pris en charge](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="c0534-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0534-113">*Ignorer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c0534-113">*bypass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0534-114">**Valeur booléenne** qui spécifie si le serveur proxy est contourné.</span><span class="sxs-lookup"><span data-stu-id="c0534-114">**Boolean** specifying whether the proxy server is bypassed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0534-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c0534-115">Return value</span></span>

<span data-ttu-id="c0534-116">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c0534-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0534-117">Notes</span><span class="sxs-lookup"><span data-stu-id="c0534-117">Remarks</span></span>

<span data-ttu-id="c0534-118">Cette méthode n’a aucun effet, à moins que **getProxySettings** retourne la valeur 2 (utiliser des paramètres manuels).</span><span class="sxs-lookup"><span data-stu-id="c0534-118">This method has no effect unless **getProxySettings** returns a value of 2 (use manual settings).</span></span>

<span data-ttu-id="c0534-119">Cette méthode échoue sauf si l’application appelante est en cours d’exécution sur l’ordinateur local ou sur l’intranet.</span><span class="sxs-lookup"><span data-stu-id="c0534-119">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="c0534-120">**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="c0534-120">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="c0534-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="c0534-121">Examples</span></span>

<span data-ttu-id="c0534-122">L’exemple JScript suivant utilise le *réseau*. **setProxyBypassForLocal** pour spécifier si le serveur proxy du lecteur Windows Media est contourné, lors de l’utilisation du protocole MMS, si le serveur d’origine se trouve sur un réseau local.</span><span class="sxs-lookup"><span data-stu-id="c0534-122">The following JScript example uses *Network*.**setProxyBypassForLocal** to specify whether the Windows Media Player proxy server is bypassed, when using the MMS protocol, if the origin server is on a local network.</span></span> <span data-ttu-id="c0534-123">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="c0534-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Prompt the user for a setting. Store the response in a variable.
   var proxybypass = confirm("Bypass proxy server for local addresses? \n OK = Yes \n Cancel = No");

   // Set the proxy bypass value using the user input.
   Player.network.setProxyBypassForLocal("MMS", proxybypass);
}

else

// Warn that proxy settings must be set to 2.
alert("Proxy settings must be manual!");

```



## <a name="requirements"></a><span data-ttu-id="c0534-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0534-124">Requirements</span></span>



| <span data-ttu-id="c0534-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0534-125">Requirement</span></span> | <span data-ttu-id="c0534-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0534-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c0534-127">Version</span><span class="sxs-lookup"><span data-stu-id="c0534-127">Version</span></span><br/> | <span data-ttu-id="c0534-128">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="c0534-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="c0534-129">DLL</span><span class="sxs-lookup"><span data-stu-id="c0534-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="c0534-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0534-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0534-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0534-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0534-132">**Objet réseau**</span><span class="sxs-lookup"><span data-stu-id="c0534-132">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





