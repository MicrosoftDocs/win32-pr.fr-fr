---
title: Méthode Network. getProxyName
description: La méthode getProxyName récupère le nom du serveur proxy utilisé.
ms.assetid: 273b1f7d-84b7-4e50-9f80-9fd1978e7528
keywords:
- méthode getProxyName lecteur Windows Media
- méthode getProxyName lecteur Windows Media, classe réseau
- Classe réseau lecteur Windows Media, méthode getProxyName
topic_type:
- apiref
api_name:
- Network.getProxyName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a97e51508e9df9aeac85dbc01116e80e710dcb45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532643"
---
# <a name="networkgetproxyname-method"></a><span data-ttu-id="888ab-106">Méthode Network. getProxyName</span><span class="sxs-lookup"><span data-stu-id="888ab-106">Network.getProxyName method</span></span>

<span data-ttu-id="888ab-107">La méthode **getProxyName** récupère le nom du serveur proxy utilisé.</span><span class="sxs-lookup"><span data-stu-id="888ab-107">The **getProxyName** method retrieves the name of the proxy server being used.</span></span>

## <a name="syntax"></a><span data-ttu-id="888ab-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="888ab-108">Syntax</span></span>


```JScript
strRetVal = Network.getProxyName(
  protocol
)
```



## <a name="parameters"></a><span data-ttu-id="888ab-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="888ab-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="888ab-110">*protocole* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="888ab-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="888ab-111">**Chaîne** spécifiant le nom du protocole.</span><span class="sxs-lookup"><span data-stu-id="888ab-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="888ab-112">Pour obtenir la liste des protocoles pris en charge, consultez [protocoles et types de fichiers pris en charge](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="888ab-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="888ab-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="888ab-113">Return value</span></span>

<span data-ttu-id="888ab-114">Cette méthode retourne une **chaîne** contenant le nom du serveur proxy utilisé.</span><span class="sxs-lookup"><span data-stu-id="888ab-114">This method returns a **String** containing the name of the proxy server being used.</span></span> <span data-ttu-id="888ab-115">La valeur retournée est significative uniquement lorsque **getProxySettings** retourne la valeur 2 (utiliser des paramètres manuels).</span><span class="sxs-lookup"><span data-stu-id="888ab-115">The value returned is meaningful only when **getProxySettings** returns a value of 2 (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="888ab-116">Notes</span><span class="sxs-lookup"><span data-stu-id="888ab-116">Remarks</span></span>

<span data-ttu-id="888ab-117">Cette méthode échoue sauf si l’application appelante est en cours d’exécution sur l’ordinateur local ou sur l’intranet.</span><span class="sxs-lookup"><span data-stu-id="888ab-117">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="888ab-118">**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="888ab-118">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="888ab-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="888ab-119">Examples</span></span>

<span data-ttu-id="888ab-120">L’exemple JScript suivant utilise le *réseau*. **getProxyName** pour afficher les noms des serveurs proxy du lecteur Windows Media pour les protocoles HTTP et MMS.</span><span class="sxs-lookup"><span data-stu-id="888ab-120">The following JScript example uses *Network*.**getProxyName** to display the Windows Media Player proxy server names for the HTTP and MMS protocols.</span></span> <span data-ttu-id="888ab-121">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="888ab-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy server name for HTTP.
   var proxyNameHTTP = Player.network.getProxyName("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy server name for MMS.
   var proxyNameMMS = Player.network.getProxyName("MMS");

// Display the proxy server names in the browser client area.
// Unavailable proxy server names will display as "undefined".
document.write("The current HTTP proxy server name is: " + proxyNameHTTP);
document.write("<BR>");
document.write("The current MMS proxy server name is: " + proxyNameMMS);

```



## <a name="requirements"></a><span data-ttu-id="888ab-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="888ab-122">Requirements</span></span>



| <span data-ttu-id="888ab-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="888ab-123">Requirement</span></span> | <span data-ttu-id="888ab-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="888ab-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="888ab-125">Version</span><span class="sxs-lookup"><span data-stu-id="888ab-125">Version</span></span><br/> | <span data-ttu-id="888ab-126">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="888ab-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="888ab-127">DLL</span><span class="sxs-lookup"><span data-stu-id="888ab-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="888ab-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="888ab-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="888ab-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="888ab-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="888ab-130">**Objet réseau**</span><span class="sxs-lookup"><span data-stu-id="888ab-130">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="888ab-131">**Network. getProxySettings**</span><span class="sxs-lookup"><span data-stu-id="888ab-131">**Network.getProxySettings**</span></span>](network-getproxysettings.md)
</dt> </dl>

 

 





