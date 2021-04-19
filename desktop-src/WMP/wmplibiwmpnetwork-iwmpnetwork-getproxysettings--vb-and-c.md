---
title: Méthode IWMPNetwork getProxySettings
description: La méthode getProxySettings retourne des informations sur les paramètres de proxy pour un protocole.
ms.assetid: eda4829a-4869-4557-8fe9-8061a1e0f586
keywords:
- méthode getProxySettings lecteur Windows Media
- méthode getProxySettings lecteur Windows Media, interface IWMPNetwork
- Interface IWMPNetwork lecteur Windows Media, méthode getProxySettings
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxySettings
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d970160c07c90e84585c87ed1abf740fbe3c6318
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533134"
---
# <a name="iwmpnetworkgetproxysettings-method"></a><span data-ttu-id="727f4-106">IWMPNetwork :: getProxySettings, méthode</span><span class="sxs-lookup"><span data-stu-id="727f4-106">IWMPNetwork::getProxySettings method</span></span>

<span data-ttu-id="727f4-107">La méthode **getProxySettings** retourne des informations sur les paramètres de proxy pour un protocole.</span><span class="sxs-lookup"><span data-stu-id="727f4-107">The **getProxySettings** method returns information about the proxy settings for a protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="727f4-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="727f4-108">Syntax</span></span>


```CSharp
public System.Int32 getProxySettings(
  System.String bstrProtocol
);
```


```VB

Public Function getProxySettings( _
  ByVal bstrProtocol As System.String _
) As System.Int32
Implements IWMPNetwork.getProxySettings
```





## <a name="parameters"></a><span data-ttu-id="727f4-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="727f4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="727f4-110">*bstrProtocol* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="727f4-110">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="727f4-111">**System. String** qui est le nom de protocole.</span><span class="sxs-lookup"><span data-stu-id="727f4-111">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="727f4-112">Pour obtenir la liste des protocoles pris en charge, consultez [protocoles et types de fichiers pris en charge](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="727f4-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="727f4-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="727f4-113">Return value</span></span>

<span data-ttu-id="727f4-114">**System. Int32** qui est l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="727f4-114">A **System.Int32** that is one of the following values.</span></span>



| <span data-ttu-id="727f4-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="727f4-115">Value</span></span> | <span data-ttu-id="727f4-116">Description</span><span class="sxs-lookup"><span data-stu-id="727f4-116">Description</span></span>                                                                      |
|-------|----------------------------------------------------------------------------------|
| <span data-ttu-id="727f4-117">0</span><span class="sxs-lookup"><span data-stu-id="727f4-117">0</span></span>     | <span data-ttu-id="727f4-118">Aucun serveur proxy n’est utilisé.</span><span class="sxs-lookup"><span data-stu-id="727f4-118">A proxy server is not being used.</span></span>                                                |
| <span data-ttu-id="727f4-119">1</span><span class="sxs-lookup"><span data-stu-id="727f4-119">1</span></span>     | <span data-ttu-id="727f4-120">Les paramètres de proxy pour le navigateur actuel sont utilisés (valides uniquement pour le protocole HTTP).</span><span class="sxs-lookup"><span data-stu-id="727f4-120">The proxy settings for the current browser are being used (valid only for HTTP).</span></span> |
| <span data-ttu-id="727f4-121">2</span><span class="sxs-lookup"><span data-stu-id="727f4-121">2</span></span>     | <span data-ttu-id="727f4-122">Les paramètres de proxy spécifiés manuellement sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="727f4-122">The manually specified proxy settings are being used.</span></span>                            |
| <span data-ttu-id="727f4-123">3</span><span class="sxs-lookup"><span data-stu-id="727f4-123">3</span></span>     | <span data-ttu-id="727f4-124">Les paramètres de proxy sont détectés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="727f4-124">The proxy settings are being auto-detected.</span></span>                                      |



 

## <a name="remarks"></a><span data-ttu-id="727f4-125">Notes</span><span class="sxs-lookup"><span data-stu-id="727f4-125">Remarks</span></span>

<span data-ttu-id="727f4-126">Cette méthode échoue sauf si l’application appelante est en cours d’exécution sur l’ordinateur local ou sur l’intranet.</span><span class="sxs-lookup"><span data-stu-id="727f4-126">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="727f4-127">Exemples</span><span class="sxs-lookup"><span data-stu-id="727f4-127">Examples</span></span>

<span data-ttu-id="727f4-128">L’exemple de code suivant utilise **getProxySettings** pour afficher un message qui fournit des informations sur les paramètres de proxy actuels du lecteur, dans une étiquette.</span><span class="sxs-lookup"><span data-stu-id="727f4-128">The following code example uses **getProxySettings** to display a message, which gives information about the current proxy settings of the Player, in a label.</span></span> <span data-ttu-id="727f4-129">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="727f4-129">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Retrieve a number representing the current proxy settings.
int proxySetting = player.network.getProxySettings("MMS");

// Display the message that corresponds to the current settings.
switch(proxySetting)
{
    case 0:
    proxySettingsLabel.Text = "A proxy server is not being used";
    break;

    case 1: 
    proxySettingsLabel.Text = "The proxy settings for the current browser are being used.";
    break;

    case 2:
    proxySettingsLabel.Text = "The manually specified proxy settings are being used.";
    break;

    case 3:
    proxySettingsLabel.Text = "The proxy settings are being auto-detected.";
    break;

    default:
    proxySettingsLabel.Text = "Unable to determine proxy setting, try again.";
    break;
}
```


```VB

' Retrieve a number representing the current proxy settings.
Dim proxySetting As Integer = player.network.getProxySettings(&quot;MMS&quot;)

&#39; Display the message that corresponds to the current settings.
Select Case proxySetting

    Case 0
        proxySettingsLabel.Text = &quot;A proxy server is not being used&quot;

    Case 1
        proxySettingsLabel.Text = &quot;The proxy settings for the current browser are being used.&quot;

    Case 2
        proxySettingsLabel.Text = &quot;The manually specified proxy settings are being used.&quot;

    Case 3
        proxySettingsLabel.Text = &quot;The proxy settings are being auto-detected.&quot;

    Case Else
        proxySettingsLabel.Text = &quot;Unable to determine proxy setting, try again.&quot;

End Select
```





## <a name="requirements"></a><span data-ttu-id="727f4-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="727f4-130">Requirements</span></span>



| <span data-ttu-id="727f4-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="727f4-131">Requirement</span></span> | <span data-ttu-id="727f4-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="727f4-132">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="727f4-133">Version</span><span class="sxs-lookup"><span data-stu-id="727f4-133">Version</span></span><br/>   | <span data-ttu-id="727f4-134">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="727f4-134">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="727f4-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="727f4-135">Namespace</span></span><br/> | <span data-ttu-id="727f4-136">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="727f4-136">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="727f4-137">Assembly</span><span class="sxs-lookup"><span data-stu-id="727f4-137">Assembly</span></span><br/>  | <dl> <span data-ttu-id="727f4-138"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="727f4-138"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="727f4-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="727f4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="727f4-140">**Interface IWMPNetwork (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="727f4-140">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="727f4-141">**IWMPNetwork. Setproxysettings n' (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="727f4-141">**IWMPNetwork.setProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxysettings--vb-and-c.md)
</dt> </dl>

 

 





