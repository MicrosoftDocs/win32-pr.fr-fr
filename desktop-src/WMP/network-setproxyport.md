---
title: Méthode Network. setProxyPort
description: La méthode setProxyPort spécifie le port du proxy à utiliser. | Méthode Network. setProxyPort
ms.assetid: 09cfce4a-191c-4596-b678-15d9328d5c53
keywords:
- méthode setProxyPort lecteur Windows Media
- méthode setProxyPort lecteur Windows Media, classe réseau
- Classe réseau lecteur Windows Media, méthode setProxyPort
topic_type:
- apiref
api_name:
- Network.setProxyPort
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2438688535e4727688ddbd5d67fd65cbed15864d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531793"
---
# <a name="networksetproxyport-method"></a><span data-ttu-id="c952a-107">Méthode Network. setProxyPort</span><span class="sxs-lookup"><span data-stu-id="c952a-107">Network.setProxyPort method</span></span>

<span data-ttu-id="c952a-108">La méthode **setProxyPort** spécifie le port du proxy à utiliser.</span><span class="sxs-lookup"><span data-stu-id="c952a-108">The **setProxyPort** method specifies the proxy port to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="c952a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c952a-109">Syntax</span></span>


```JScript
Network.setProxyPort(
  protocol,
  port
)
```



## <a name="parameters"></a><span data-ttu-id="c952a-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c952a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c952a-111">*protocole* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c952a-111">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c952a-112">**Chaîne** spécifiant le nom du protocole.</span><span class="sxs-lookup"><span data-stu-id="c952a-112">**String** specifying the protocol name.</span></span> <span data-ttu-id="c952a-113">Pour obtenir la liste des protocoles pris en charge, consultez [protocoles et types de fichiers pris en charge](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="c952a-113">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="c952a-114">*port* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c952a-114">*port* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c952a-115">**Nombre** (**long**) spécifiant le port du proxy à utiliser.</span><span class="sxs-lookup"><span data-stu-id="c952a-115">**Number** (**long**) specifying the proxy port to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c952a-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c952a-116">Return value</span></span>

<span data-ttu-id="c952a-117">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c952a-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c952a-118">Notes</span><span class="sxs-lookup"><span data-stu-id="c952a-118">Remarks</span></span>

<span data-ttu-id="c952a-119">Cette méthode n’a aucun effet, à moins que **getProxySettings** retourne la valeur 2 (utiliser des paramètres manuels).</span><span class="sxs-lookup"><span data-stu-id="c952a-119">This method has no effect unless **getProxySettings** returns a value of 2 (use manual settings).</span></span>

<span data-ttu-id="c952a-120">Cette méthode échoue sauf si l’application appelante est en cours d’exécution sur l’ordinateur local ou sur l’intranet.</span><span class="sxs-lookup"><span data-stu-id="c952a-120">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="c952a-121">**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="c952a-121">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="c952a-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="c952a-122">Examples</span></span>

<span data-ttu-id="c952a-123">L’exemple JScript suivant utilise le *réseau*. **setProxyPort** pour spécifier le numéro de port du proxy du lecteur Windows Media pour le protocole MMS.</span><span class="sxs-lookup"><span data-stu-id="c952a-123">The following JScript example uses *Network*.**setProxyPort** to specify the Windows Media Player proxy port number for the MMS protocol.</span></span> <span data-ttu-id="c952a-124">Le numéro de port est récupéré à partir d’un élément INPUT HTML avec ID = "PORT".</span><span class="sxs-lookup"><span data-stu-id="c952a-124">The port number is retrieved from an HTML INPUT element with ID = "PORT".</span></span> <span data-ttu-id="c952a-125">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="c952a-125">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Store the port number specified by the user.
   var portnumber = PORT.value;

   // Set the port number for the MMS protocol.
   Player.network.setProxyPort("MMS", portnumber);
}

else

// Warn that proxy settings must be set to 2.
alert("Proxy settings must be manual!");

```



## <a name="requirements"></a><span data-ttu-id="c952a-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c952a-126">Requirements</span></span>



| <span data-ttu-id="c952a-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c952a-127">Requirement</span></span> | <span data-ttu-id="c952a-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="c952a-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c952a-129">Version</span><span class="sxs-lookup"><span data-stu-id="c952a-129">Version</span></span><br/> | <span data-ttu-id="c952a-130">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="c952a-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="c952a-131">DLL</span><span class="sxs-lookup"><span data-stu-id="c952a-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="c952a-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c952a-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c952a-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c952a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c952a-134">**Objet réseau**</span><span class="sxs-lookup"><span data-stu-id="c952a-134">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





