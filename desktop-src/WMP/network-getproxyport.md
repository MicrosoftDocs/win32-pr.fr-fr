---
title: Méthode Network. getProxyPort
description: La méthode getProxyPort récupère le port proxy utilisé.
ms.assetid: 76771750-3763-4029-b194-d8567b5f365e
keywords:
- méthode getProxyPort lecteur Windows Media
- méthode getProxyPort lecteur Windows Media, classe réseau
- Classe réseau lecteur Windows Media, méthode getProxyPort
topic_type:
- apiref
api_name:
- Network.getProxyPort
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3114b2188c0ccb0f6c260df33461fb117e7851e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523533"
---
# <a name="networkgetproxyport-method"></a><span data-ttu-id="47cca-106">Méthode Network. getProxyPort</span><span class="sxs-lookup"><span data-stu-id="47cca-106">Network.getProxyPort method</span></span>

<span data-ttu-id="47cca-107">La méthode **getProxyPort** récupère le port proxy utilisé.</span><span class="sxs-lookup"><span data-stu-id="47cca-107">The **getProxyPort** method retrieves the proxy port being used.</span></span>

## <a name="syntax"></a><span data-ttu-id="47cca-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="47cca-108">Syntax</span></span>


```JScript
retVal = Network.getProxyPort(
  protocol
)
```



## <a name="parameters"></a><span data-ttu-id="47cca-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="47cca-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47cca-110">*protocole* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="47cca-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47cca-111">**Chaîne** spécifiant le nom du protocole.</span><span class="sxs-lookup"><span data-stu-id="47cca-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="47cca-112">Pour obtenir la liste des protocoles pris en charge, consultez [protocoles et types de fichiers pris en charge](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="47cca-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47cca-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="47cca-113">Return value</span></span>

<span data-ttu-id="47cca-114">Cette méthode retourne un **nombre** (**long**) contenant le port proxy utilisé.</span><span class="sxs-lookup"><span data-stu-id="47cca-114">This method returns a **Number** (**long**) containing the proxy port being used.</span></span> <span data-ttu-id="47cca-115">La valeur retournée est significative uniquement lorsque **getProxySettings** retourne une valeur de deux (utilisez des paramètres manuels).</span><span class="sxs-lookup"><span data-stu-id="47cca-115">The value returned is meaningful only when **getProxySettings** returns a value of two (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="47cca-116">Notes</span><span class="sxs-lookup"><span data-stu-id="47cca-116">Remarks</span></span>

<span data-ttu-id="47cca-117">Cette méthode échoue sauf si l’application appelante est en cours d’exécution sur l’ordinateur local ou sur l’intranet.</span><span class="sxs-lookup"><span data-stu-id="47cca-117">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="47cca-118">**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="47cca-118">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="47cca-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="47cca-119">Examples</span></span>

<span data-ttu-id="47cca-120">L’exemple JScript suivant utilise le *réseau*. **getProxyPort** pour afficher les numéros de port du proxy du lecteur Windows Media actuels pour les protocoles MMS et http.</span><span class="sxs-lookup"><span data-stu-id="47cca-120">The following JScript example uses *Network*.**getProxyPort** to display the current Windows Media Player proxy port numbers for the MMS and HTTP protocols.</span></span> <span data-ttu-id="47cca-121">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="47cca-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy port number for HTTP.
   var proxyPortHTTP = Player.network.getProxyPort("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy port number for MMS.
   var proxyPortMMS = Player.network.getProxyPort("MMS");

// Display the port numbers in the browser client area.
// Unavailable port numbers will display as "undefined".
document.write("The current HTTP proxy port is: " + proxyPortHTTP);
document.write("<BR>");
document.write("The current MMS proxy port is: " + proxyPortMMS);

```



## <a name="requirements"></a><span data-ttu-id="47cca-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="47cca-122">Requirements</span></span>



| <span data-ttu-id="47cca-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="47cca-123">Requirement</span></span> | <span data-ttu-id="47cca-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="47cca-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="47cca-125">Version</span><span class="sxs-lookup"><span data-stu-id="47cca-125">Version</span></span><br/> | <span data-ttu-id="47cca-126">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="47cca-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="47cca-127">DLL</span><span class="sxs-lookup"><span data-stu-id="47cca-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="47cca-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47cca-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47cca-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47cca-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47cca-130">**Objet réseau**</span><span class="sxs-lookup"><span data-stu-id="47cca-130">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="47cca-131">**Network. getProxySettings**</span><span class="sxs-lookup"><span data-stu-id="47cca-131">**Network.getProxySettings**</span></span>](network-getproxysettings.md)
</dt> </dl>

 

 





