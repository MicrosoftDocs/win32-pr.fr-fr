---
title: Méthode Network. getProxySettings
description: La méthode getProxySettings récupère le paramètre de proxy pour un protocole donné.
ms.assetid: a7b21eab-93e1-458b-aab0-60fd298cce44
keywords:
- méthode getProxySettings lecteur Windows Media
- méthode getProxySettings lecteur Windows Media, classe réseau
- Classe réseau lecteur Windows Media, méthode getProxySettings
topic_type:
- apiref
api_name:
- Network.getProxySettings
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44a306fca1e671e7e5b3a89c0da952e5c81ba20e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530965"
---
# <a name="networkgetproxysettings-method"></a><span data-ttu-id="4f01b-106">Méthode Network. getProxySettings</span><span class="sxs-lookup"><span data-stu-id="4f01b-106">Network.getProxySettings method</span></span>

<span data-ttu-id="4f01b-107">La méthode **getProxySettings** récupère le paramètre de proxy pour un protocole donné.</span><span class="sxs-lookup"><span data-stu-id="4f01b-107">The **getProxySettings** method retrieves the proxy setting for a given protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f01b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4f01b-108">Syntax</span></span>


```JScript
retVal = Network.getProxySettings(
  protocol
)
```



## <a name="parameters"></a><span data-ttu-id="4f01b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4f01b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f01b-110">*protocole* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4f01b-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f01b-111">**Chaîne** spécifiant le nom du protocole.</span><span class="sxs-lookup"><span data-stu-id="4f01b-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="4f01b-112">Pour obtenir la liste des protocoles pris en charge, consultez [protocoles et types de fichiers pris en charge](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="4f01b-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f01b-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4f01b-113">Return value</span></span>

<span data-ttu-id="4f01b-114">Cette méthode retourne un **nombre** (**long**) contenant l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="4f01b-114">This method returns a **Number** (**long**) containing one of the following values.</span></span>



| <span data-ttu-id="4f01b-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f01b-115">Value</span></span> | <span data-ttu-id="4f01b-116">Description</span><span class="sxs-lookup"><span data-stu-id="4f01b-116">Description</span></span>                                                                      |
|-------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4f01b-117">0</span><span class="sxs-lookup"><span data-stu-id="4f01b-117">0</span></span>     | <span data-ttu-id="4f01b-118">Aucun serveur proxy n’est utilisé.</span><span class="sxs-lookup"><span data-stu-id="4f01b-118">A proxy server is not being used.</span></span>                                                |
| <span data-ttu-id="4f01b-119">1</span><span class="sxs-lookup"><span data-stu-id="4f01b-119">1</span></span>     | <span data-ttu-id="4f01b-120">Les paramètres de proxy du navigateur actuel sont utilisés (valides uniquement pour HTTP).</span><span class="sxs-lookup"><span data-stu-id="4f01b-120">The proxy settings for the current browser are being used (only valid for HTTP).</span></span> |
| <span data-ttu-id="4f01b-121">2</span><span class="sxs-lookup"><span data-stu-id="4f01b-121">2</span></span>     | <span data-ttu-id="4f01b-122">Les paramètres de proxy spécifiés manuellement sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="4f01b-122">The manually specified proxy settings are being used.</span></span>                            |
| <span data-ttu-id="4f01b-123">3</span><span class="sxs-lookup"><span data-stu-id="4f01b-123">3</span></span>     | <span data-ttu-id="4f01b-124">Les paramètres de proxy sont détectés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="4f01b-124">The proxy settings are being auto-detected.</span></span>                                      |



 

## <a name="remarks"></a><span data-ttu-id="4f01b-125">Notes</span><span class="sxs-lookup"><span data-stu-id="4f01b-125">Remarks</span></span>

<span data-ttu-id="4f01b-126">Cette méthode échoue sauf si l’application appelante est en cours d’exécution sur l’ordinateur local ou sur l’intranet.</span><span class="sxs-lookup"><span data-stu-id="4f01b-126">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="4f01b-127">**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="4f01b-127">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="4f01b-128">Exemples</span><span class="sxs-lookup"><span data-stu-id="4f01b-128">Examples</span></span>

<span data-ttu-id="4f01b-129">L’exemple JScript suivant utilise le *réseau*. **getProxySettings** pour afficher un message qui donne des informations sur les paramètres de proxy actuels du lecteur, dans la fenêtre du navigateur.</span><span class="sxs-lookup"><span data-stu-id="4f01b-129">The following JScript example uses *Network*.**getProxySettings** to display a message, which gives information about the current proxy settings of the Player, in the browser window.</span></span> <span data-ttu-id="4f01b-130">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="4f01b-130">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Retrieve a number representing the current proxy settings.
var proxySetting = Player.network.getProxySettings("MMS");

// Display the message the corresponds to the current settings.
switch(proxySetting){

   case 0:
     document.write("A proxy server is not being used");
     break;

   case 1: 
     document.write("The proxy settings for the current browser are being used.");
     break;

   case 2:
     document.write("The manually specified proxy settings are being used.");
     break;

case 3:
     document.write("The proxy settings are being auto-detected.");
     break;

   default:
     document.write("Unable to determine proxy setting, try again.");
}

```



## <a name="requirements"></a><span data-ttu-id="4f01b-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f01b-131">Requirements</span></span>



| <span data-ttu-id="4f01b-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4f01b-132">Requirement</span></span> | <span data-ttu-id="4f01b-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f01b-133">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4f01b-134">Version</span><span class="sxs-lookup"><span data-stu-id="4f01b-134">Version</span></span><br/> | <span data-ttu-id="4f01b-135">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="4f01b-135">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="4f01b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="4f01b-136">DLL</span></span><br/>     | <dl> <span data-ttu-id="4f01b-137"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f01b-137"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f01b-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f01b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f01b-139">**Objet réseau**</span><span class="sxs-lookup"><span data-stu-id="4f01b-139">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





