---
title: Player. versionInfo
description: La propriété versionInfo récupère une valeur de chaîne spécifiant la version du lecteur Windows Media.
ms.assetid: 4b644de2-fcb9-407b-9eea-3eb683a17150
keywords:
- Lecteur Windows Media Player. versionInfo
topic_type:
- apiref
api_name:
- Player.versionInfo
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b44a94fa2df6d5e7d46108ec971fd84481688eb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535945"
---
# <a name="playerversioninfo"></a><span data-ttu-id="cd916-104">Player. versionInfo</span><span class="sxs-lookup"><span data-stu-id="cd916-104">Player.versionInfo</span></span>

<span data-ttu-id="cd916-105">La propriété **VERSIONINFO** récupère une valeur de chaîne spécifiant la version du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="cd916-105">The **versionInfo** property retrieves a String value specifying the version of the Windows Media Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd916-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cd916-106">Syntax</span></span>

<span data-ttu-id="cd916-107">*lecteur* . **VERSIONINFO**</span><span class="sxs-lookup"><span data-stu-id="cd916-107">*player* .**versionInfo**</span></span>

## <a name="possible-values"></a><span data-ttu-id="cd916-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="cd916-108">Possible Values</span></span>

<span data-ttu-id="cd916-109">Cette propriété est une **chaîne** en lecture seule au format suivant : «*X*. 0,0. *Yyyy*"où *X* représente le numéro de version principale et *yyyy* représente le numéro de Build.</span><span class="sxs-lookup"><span data-stu-id="cd916-109">This property is a read-only **String** in the following format: "*X*.0.0.*YYYY*" where *X* represents the major version number and *YYYY* represents the build number.</span></span>

## <a name="examples"></a><span data-ttu-id="cd916-110">Exemples</span><span class="sxs-lookup"><span data-stu-id="cd916-110">Examples</span></span>

<span data-ttu-id="cd916-111">L’exemple suivant crée un élément bouton HTML qui, lorsque vous cliquez dessus, affiche une boîte de message contenant les informations de version pour le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="cd916-111">The following example creates an HTML BUTTON element that, when clicked, displays a message box containing the version information for Windows Media Player.</span></span> <span data-ttu-id="cd916-112">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="cd916-112">The **Player** object was created with ID = "Player".</span></span>


```
<INPUT TYPE = "BUTTON"  ID = "VERSION"  VALUE = "Show Version"
    onClick = "
        /* Build the message containing the version info. */
        var message = 'Windows Media Player Version: ';
        message += '\n';
        message += Player.versionInfo;
 
        /* Display the message box. */
        alert(message);
">

```



## <a name="requirements"></a><span data-ttu-id="cd916-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cd916-113">Requirements</span></span>



| <span data-ttu-id="cd916-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cd916-114">Requirement</span></span> | <span data-ttu-id="cd916-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd916-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cd916-116">Version</span><span class="sxs-lookup"><span data-stu-id="cd916-116">Version</span></span><br/> | <span data-ttu-id="cd916-117">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="cd916-117">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="cd916-118">DLL</span><span class="sxs-lookup"><span data-stu-id="cd916-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="cd916-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd916-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd916-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd916-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd916-121">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="cd916-121">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





