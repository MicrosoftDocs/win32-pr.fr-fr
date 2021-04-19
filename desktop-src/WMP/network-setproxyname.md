---
title: Méthode Network. setProxyName
description: La méthode setProxyName spécifie le nom du serveur proxy à utiliser. | Méthode Network. setProxyName
ms.assetid: dbcb2a00-4387-42af-8055-61d78d021ec7
keywords:
- méthode setProxyName lecteur Windows Media
- méthode setProxyName lecteur Windows Media, classe réseau
- Classe réseau lecteur Windows Media, méthode setProxyName
topic_type:
- apiref
api_name:
- Network.setProxyName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a34546a395d48e939c71a806d8125150fca0ff4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545530"
---
# <a name="networksetproxyname-method"></a><span data-ttu-id="05068-107">Méthode Network. setProxyName</span><span class="sxs-lookup"><span data-stu-id="05068-107">Network.setProxyName method</span></span>

<span data-ttu-id="05068-108">La méthode **setProxyName** spécifie le nom du serveur proxy à utiliser.</span><span class="sxs-lookup"><span data-stu-id="05068-108">The **setProxyName** method specifies the name of the proxy server to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="05068-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="05068-109">Syntax</span></span>


```JScript
Network.setProxyName(
  protocol,
  name
)
```



## <a name="parameters"></a><span data-ttu-id="05068-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="05068-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05068-111">*protocole* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="05068-111">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05068-112">**Chaîne** spécifiant le nom du protocole.</span><span class="sxs-lookup"><span data-stu-id="05068-112">**String** specifying the protocol name.</span></span> <span data-ttu-id="05068-113">Pour obtenir la liste des protocoles pris en charge, consultez [protocoles et types de fichiers pris en charge](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="05068-113">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="05068-114">*nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="05068-114">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05068-115">**Chaîne** spécifiant le nom du serveur proxy à utiliser.</span><span class="sxs-lookup"><span data-stu-id="05068-115">**String** specifying the name of the proxy server to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05068-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="05068-116">Return value</span></span>

<span data-ttu-id="05068-117">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="05068-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="05068-118">Notes</span><span class="sxs-lookup"><span data-stu-id="05068-118">Remarks</span></span>

<span data-ttu-id="05068-119">Cette méthode n’a aucun effet, à moins que **getProxySettings** retourne la valeur 2 (utiliser des paramètres manuels).</span><span class="sxs-lookup"><span data-stu-id="05068-119">This method has no effect unless **getProxySettings** returns a value of 2 (use manual settings).</span></span>

<span data-ttu-id="05068-120">Cette méthode échoue sauf si l’application appelante est en cours d’exécution sur l’ordinateur local ou sur l’intranet.</span><span class="sxs-lookup"><span data-stu-id="05068-120">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="05068-121">**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="05068-121">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="05068-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="05068-122">Examples</span></span>

<span data-ttu-id="05068-123">L’exemple JScript suivant utilise le *réseau*. **setProxyName** pour spécifier le nom du serveur proxy du lecteur Windows Media pour le protocole MMS.</span><span class="sxs-lookup"><span data-stu-id="05068-123">The following JScript example uses *Network*.**setProxyName** to specify the name of the Windows Media Player proxy server for the MMS protocol.</span></span> <span data-ttu-id="05068-124">Le nouveau nom est récupéré à partir d’un élément de texte HTML avec ID = "NAME".</span><span class="sxs-lookup"><span data-stu-id="05068-124">The new name is retrieved from an HTML TEXT element with ID = "NAME".</span></span> <span data-ttu-id="05068-125">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="05068-125">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Store the new proxy server name specified by the user.
   var proxyname = NAME.value;

   // Set the proxy server name.
   Player.network.setProxyName("MMS", proxyname);
}

else

// Warn that proxy settings must be set to 2.
alert("Proxy settings must be manual!");

```



## <a name="requirements"></a><span data-ttu-id="05068-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="05068-126">Requirements</span></span>



| <span data-ttu-id="05068-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05068-127">Requirement</span></span> | <span data-ttu-id="05068-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="05068-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="05068-129">Version</span><span class="sxs-lookup"><span data-stu-id="05068-129">Version</span></span><br/> | <span data-ttu-id="05068-130">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="05068-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="05068-131">DLL</span><span class="sxs-lookup"><span data-stu-id="05068-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="05068-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05068-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05068-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05068-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05068-134">**Objet réseau**</span><span class="sxs-lookup"><span data-stu-id="05068-134">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





