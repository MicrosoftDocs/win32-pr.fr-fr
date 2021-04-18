---
title: Network. bufferingTime
description: La propriété bufferingTime spécifie ou récupère la durée (en millisecondes) allouée à la mise en mémoire tampon des données entrantes avant le début de la diffusion.
ms.assetid: b52b7f44-6be1-4299-94da-c37d758795af
keywords:
- Lecteur Windows Media Network. bufferingTime
topic_type:
- apiref
api_name:
- Network.bufferingTime
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27b805173403268afff473db427b58193382afe6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540371"
---
# <a name="networkbufferingtime"></a><span data-ttu-id="d0d00-104">Network. bufferingTime</span><span class="sxs-lookup"><span data-stu-id="d0d00-104">Network.bufferingTime</span></span>

<span data-ttu-id="d0d00-105">La propriété **bufferingTime** spécifie ou récupère la durée (en millisecondes) allouée à la mise en mémoire tampon des données entrantes avant le début de la diffusion.</span><span class="sxs-lookup"><span data-stu-id="d0d00-105">The **bufferingTime** property specifies or retrieves the amount of time in milliseconds allocated for buffering incoming data before playing begins.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0d00-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d0d00-106">Syntax</span></span>

<span data-ttu-id="d0d00-107">*lecteur*. *réseau*. **bufferingTime**</span><span class="sxs-lookup"><span data-stu-id="d0d00-107">*player*.*network*.**bufferingTime**</span></span>

## <a name="possible-values"></a><span data-ttu-id="d0d00-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="d0d00-108">Possible Values</span></span>

<span data-ttu-id="d0d00-109">Cette propriété est un **nombre** en lecture/écriture (**long**) compris entre zéro et 60 000 avec une valeur par défaut de 5 000.</span><span class="sxs-lookup"><span data-stu-id="d0d00-109">This property is a read/write **Number** (**long**) ranging from zero to 60,000 with a default value of 5,000.</span></span>

## <a name="examples"></a><span data-ttu-id="d0d00-110">Exemples</span><span class="sxs-lookup"><span data-stu-id="d0d00-110">Examples</span></span>

<span data-ttu-id="d0d00-111">L’exemple JScript suivant utilise le *réseau*. **bufferingTime** pour spécifier le nombre de secondes allouées à la mise en mémoire tampon des données entrantes.</span><span class="sxs-lookup"><span data-stu-id="d0d00-111">The following JScript example uses *Network*.**bufferingTime** to specify the number of seconds allocated for buffering incoming data.</span></span> <span data-ttu-id="d0d00-112">Les informations sont récupérées à partir d’un élément d’entrée de texte HTML créé avec ID = "bufText".</span><span class="sxs-lookup"><span data-stu-id="d0d00-112">The information is retrieved from an HTML TEXT INPUT element created with ID = "bufText".</span></span> <span data-ttu-id="d0d00-113">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="d0d00-113">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create a BUTTON element to change the bufferingTime value. -->
<INPUT TYPE = "BUTTON" NAME = "bufTime" ID = "bufTime" 
       VALUE = "Change Buffer Time"

    onClick = "
       /* Test whether the user entered a valid value. */
       if (bufText.value >= 0 & bufText.value <= 60) 
           Player.network.bufferingTime = bufText.value * 1000;
       else
           alert('Buffering time must be between 0 and 60.');
">

```



## <a name="requirements"></a><span data-ttu-id="d0d00-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d0d00-114">Requirements</span></span>



| <span data-ttu-id="d0d00-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d0d00-115">Requirement</span></span> | <span data-ttu-id="d0d00-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0d00-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d0d00-117">Version</span><span class="sxs-lookup"><span data-stu-id="d0d00-117">Version</span></span><br/> | <span data-ttu-id="d0d00-118">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="d0d00-118">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="d0d00-119">DLL</span><span class="sxs-lookup"><span data-stu-id="d0d00-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="d0d00-120"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0d00-120"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0d00-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0d00-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0d00-122">**Objet réseau**</span><span class="sxs-lookup"><span data-stu-id="d0d00-122">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





