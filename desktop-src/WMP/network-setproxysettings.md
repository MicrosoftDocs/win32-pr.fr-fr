---
title: Méthode Network. Setproxysettings n'
description: La méthode Setproxysettings n’spécifie le paramètre de proxy pour un protocole donné.
ms.assetid: 473501c9-27ea-47ec-bc82-691804fbfb89
keywords:
- méthode Setproxysettings n’lecteur Windows Media
- méthode Setproxysettings n’lecteur Windows Media, classe réseau
- Classe réseau lecteur Windows Media, méthode Setproxysettings n'
topic_type:
- apiref
api_name:
- Network.setProxySettings
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b3f3da665b07f717449721c9fb43a8733cdb6c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525163"
---
# <a name="networksetproxysettings-method"></a><span data-ttu-id="f180a-106">Méthode Network. Setproxysettings n'</span><span class="sxs-lookup"><span data-stu-id="f180a-106">Network.setProxySettings method</span></span>

<span data-ttu-id="f180a-107">La méthode **setproxysettings n'** spécifie le paramètre de proxy pour un protocole donné.</span><span class="sxs-lookup"><span data-stu-id="f180a-107">The **setProxySettings** method specifies the proxy setting for a given protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="f180a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f180a-108">Syntax</span></span>


```JScript
Network.setProxySettings(
  protocol,
  setting
)
```



## <a name="parameters"></a><span data-ttu-id="f180a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f180a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f180a-110">*protocole* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f180a-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f180a-111">**Chaîne** spécifiant le nom du protocole.</span><span class="sxs-lookup"><span data-stu-id="f180a-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="f180a-112">Pour obtenir la liste des protocoles pris en charge, consultez [protocoles et types de fichiers pris en charge](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="f180a-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="f180a-113">*paramètre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f180a-113">*setting* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f180a-114">**Nombre** (**long**) contenant l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="f180a-114">**Number** (**long**) containing one of the following values.</span></span>



| <span data-ttu-id="f180a-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="f180a-115">Value</span></span> | <span data-ttu-id="f180a-116">Description</span><span class="sxs-lookup"><span data-stu-id="f180a-116">Description</span></span>                                                          |
|-------|----------------------------------------------------------------------|
| <span data-ttu-id="f180a-117">0</span><span class="sxs-lookup"><span data-stu-id="f180a-117">0</span></span>     | <span data-ttu-id="f180a-118">N’utilisez pas de serveur proxy.</span><span class="sxs-lookup"><span data-stu-id="f180a-118">Do not use a proxy server.</span></span>                                           |
| <span data-ttu-id="f180a-119">1</span><span class="sxs-lookup"><span data-stu-id="f180a-119">1</span></span>     | <span data-ttu-id="f180a-120">Utilisez les paramètres de proxy du navigateur actuel (valide uniquement pour HTTP).</span><span class="sxs-lookup"><span data-stu-id="f180a-120">Use the proxy settings of the current browser (only valid for HTTP).</span></span> |
| <span data-ttu-id="f180a-121">2</span><span class="sxs-lookup"><span data-stu-id="f180a-121">2</span></span>     | <span data-ttu-id="f180a-122">Utilisez les paramètres de proxy spécifiés manuellement.</span><span class="sxs-lookup"><span data-stu-id="f180a-122">Use the manually specified proxy settings.</span></span>                           |
| <span data-ttu-id="f180a-123">3</span><span class="sxs-lookup"><span data-stu-id="f180a-123">3</span></span>     | <span data-ttu-id="f180a-124">Détectez automatiquement les paramètres du proxy.</span><span class="sxs-lookup"><span data-stu-id="f180a-124">Auto-detect the proxy settings.</span></span>                                      |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f180a-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f180a-125">Return value</span></span>

<span data-ttu-id="f180a-126">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f180a-126">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f180a-127">Notes</span><span class="sxs-lookup"><span data-stu-id="f180a-127">Remarks</span></span>

<span data-ttu-id="f180a-128">Cette méthode échoue sauf si l’application appelante est en cours d’exécution sur l’ordinateur local ou sur l’intranet.</span><span class="sxs-lookup"><span data-stu-id="f180a-128">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="f180a-129">**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f180a-129">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="f180a-130">Exemples</span><span class="sxs-lookup"><span data-stu-id="f180a-130">Examples</span></span>

<span data-ttu-id="f180a-131">L’exemple suivant utilise JScript avec un élément HTML SELECT **pour permettre à l’utilisateur de spécifier le paramètre de proxy du lecteur Windows Media pour le protocole http. L’objet Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="f180a-131">The following example uses JScript with an HTML SELECT **element to allow the user to specify the Windows Media Player proxy setting for the HTTP protocol. The Player** object was created with ID = "Player".</span></span>


```JScript
<SELECT ID = HTTPsetproxy  NAME = "HTTPsetproxy"  LANGUAGE="JScript"
        onChange = "
                      /* Store the current selection.*/
                      var setting = this.value;

                      /* Change the proxy setting. */
                      Player.network.setProxySettings('HTTP', setting);
">

<OPTION VALUE=0>Do not use a proxy server
<OPTION VALUE=1>Use the browser settings
<OPTION VALUE=2>Use manual settings
<OPTION VALUE=3>Auto-detect settings

</SELECT>

```



## <a name="requirements"></a><span data-ttu-id="f180a-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f180a-132">Requirements</span></span>



| <span data-ttu-id="f180a-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f180a-133">Requirement</span></span> | <span data-ttu-id="f180a-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="f180a-134">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f180a-135">Version</span><span class="sxs-lookup"><span data-stu-id="f180a-135">Version</span></span><br/> | <span data-ttu-id="f180a-136">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="f180a-136">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="f180a-137">DLL</span><span class="sxs-lookup"><span data-stu-id="f180a-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="f180a-138"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f180a-138"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f180a-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f180a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f180a-140">**Objet réseau**</span><span class="sxs-lookup"><span data-stu-id="f180a-140">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





