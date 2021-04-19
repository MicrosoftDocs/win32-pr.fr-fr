---
title: ClosedCaption.SAMIFileName
description: La propriété SAMIFileName spécifie ou récupère le nom du fichier contenant les informations nécessaires pour le sous-titrage.
ms.assetid: f2090500-6c9f-4d2d-9855-a9c193b00a41
keywords:
- Lecteur Windows Media ClosedCaption. SAMIFileName
topic_type:
- apiref
api_name:
- ClosedCaption.SAMIFileName
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bd748076eec80b5b7d97e7c041f454c4f9193f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523965"
---
# <a name="closedcaptionsamifilename"></a><span data-ttu-id="9a5da-104">ClosedCaption.SAMIFileName</span><span class="sxs-lookup"><span data-stu-id="9a5da-104">ClosedCaption.SAMIFileName</span></span>

<span data-ttu-id="9a5da-105">La propriété **SAMIFileName** spécifie ou récupère le nom du fichier contenant les informations nécessaires pour le sous-titrage.</span><span class="sxs-lookup"><span data-stu-id="9a5da-105">The **SAMIFileName** property specifies or retrieves the name of the file containing the information needed for closed captioning.</span></span>

``` syntax
player.closedCaption.SAMIFileName
```

## <a name="possible-values"></a><span data-ttu-id="9a5da-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="9a5da-106">Possible Values</span></span>

<span data-ttu-id="9a5da-107">Cette propriété est une **chaîne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="9a5da-107">This property is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a5da-108">Notes</span><span class="sxs-lookup"><span data-stu-id="9a5da-108">Remarks</span></span>

<span data-ttu-id="9a5da-109">Le fichier SAMI (Synchronized Accessible Media Interchange) doit utiliser une extension de nom de fichier. SMI ou. sami.</span><span class="sxs-lookup"><span data-stu-id="9a5da-109">The Synchronized Accessible Media Interchange (SAMI) file must use an .smi or .sami file name extension.</span></span>

<span data-ttu-id="9a5da-110">Si vous ne spécifiez pas de valeur pour **SAMIFileName**, cette propriété récupère une chaîne contenant le nom de fichier ou l’URL associé à l’élément multimédia en cours.</span><span class="sxs-lookup"><span data-stu-id="9a5da-110">If you don't specify a value for **SAMIFileName**, this property retrieves a string containing the file name or URL associated with the current media item.</span></span> <span data-ttu-id="9a5da-111">Cette association peut se produire lorsqu’un fichier SAMI est spécifié à l’aide du paramètre d’URL *sami* , ou automatiquement lorsque le fichier sami porte le même nom que le nom du fichier multimédia numérique (à l’exception de l’extension de nom de fichier).</span><span class="sxs-lookup"><span data-stu-id="9a5da-111">This association can occur when a SAMI file is specified using the *sami* URL parameter, or automatically when the SAMI file has the same name as the digital media file name (except for the file name extension).</span></span> <span data-ttu-id="9a5da-112">Si aucun fichier SAMI n’est associé au média actuel, cette propriété récupère une chaîne vide ("").</span><span class="sxs-lookup"><span data-stu-id="9a5da-112">If there is no SAMI file associated with the current media, this property retrieves an empty string ("").</span></span>

<span data-ttu-id="9a5da-113">Une fois que vous avez spécifié une valeur pour **SAMIFileName**, cette valeur persiste jusqu’à ce que vous spécifiiez une nouvelle valeur (ou jusqu’à ce qu’un nouvel élément multimédia soit ouvert à l’aide du paramètre URL *sami* ).</span><span class="sxs-lookup"><span data-stu-id="9a5da-113">Once you specify a value for **SAMIFileName**, that value persists until you specify a new value (or until a new media item is opened using the *sami* URL parameter).</span></span> <span data-ttu-id="9a5da-114">Par conséquent, vous devez spécifier une nouvelle valeur pour cette propriété avant de lire chaque nouvel élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="9a5da-114">Therefore, you must specify a new value for this property before you play each new media item.</span></span> <span data-ttu-id="9a5da-115">De cette façon, la nouvelle valeur de **SAMIFileName** prend effet lors de l’ouverture de l’élément multimédia suivant (ou de *Player*.\*\*\*\* la méthode Close est appelée).</span><span class="sxs-lookup"><span data-stu-id="9a5da-115">That way, the new value for **SAMIFileName** will take effect when the next media item is opened (or when *Player*.**close** is called).</span></span> <span data-ttu-id="9a5da-116">La spécification d’une nouvelle valeur pour **SAMIFileName** n’a aucun effet sur le média actuel.</span><span class="sxs-lookup"><span data-stu-id="9a5da-116">Specifying a new value for **SAMIFileName** has no effect for the current media.</span></span>

<span data-ttu-id="9a5da-117">Pour que le lecteur Windows Media retourne à l’aide du fichier SAMI associé à un élément multimédia particulier, spécifiez une valeur pour **SAMIFileName** égale à une chaîne vide ("") avant de lire l’élément multimédia suivant.</span><span class="sxs-lookup"><span data-stu-id="9a5da-117">To cause Windows Media Player to return to using the SAMI file associated with a particular media item, specify a value for **SAMIFileName** equal to an empty string ("") before you play the next media item.</span></span>

<span data-ttu-id="9a5da-118">**Lecteur Windows Media 10 Mobile :** Cette propriété est en lecture seule et retourne toujours une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="9a5da-118">**Windows Media Player 10 Mobile:** This property is read only, and always returns an empty string.</span></span>

## <a name="examples"></a><span data-ttu-id="9a5da-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="9a5da-119">Examples</span></span>

<span data-ttu-id="9a5da-120">Les trois exemples JScript suivants utilisent *ClosedCaption*. **SAMIFileName** pour spécifier le nom d’un fichier texte de légende fermé.</span><span class="sxs-lookup"><span data-stu-id="9a5da-120">The following three JScript examples use *ClosedCaption*.**SAMIFileName** to specify the name of a closed caption text file.</span></span> <span data-ttu-id="9a5da-121">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="9a5da-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Display the closed captions from a website.
Player.closedCaption.SAMIFileName="https://www.proseware.com/ccsample.smi";

// Display the closed captions from a local network.
// You must add an escape sequence of a backslash for every original backslash.
Player.closedCaption.SAMIFileName="\\\\yourservername\\Public\\ccsample.smi";

// Display the closed captions from a file on a local drive.
// Be sure to add the appropriate escape sequences.
Player.closedCaption.SAMIFileName="C:\\WMSDK\\WMPSDK9\\samples\\media\\ccsample.smi";

```



## <a name="requirements"></a><span data-ttu-id="9a5da-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9a5da-122">Requirements</span></span>



| <span data-ttu-id="9a5da-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9a5da-123">Requirement</span></span> | <span data-ttu-id="9a5da-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a5da-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9a5da-125">Version</span><span class="sxs-lookup"><span data-stu-id="9a5da-125">Version</span></span><br/> | <span data-ttu-id="9a5da-126">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="9a5da-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="9a5da-127">DLL</span><span class="sxs-lookup"><span data-stu-id="9a5da-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="9a5da-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a5da-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a5da-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a5da-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a5da-130">**Ajout de sous-titres à des médias numériques**</span><span class="sxs-lookup"><span data-stu-id="9a5da-130">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="9a5da-131">**Objet ClosedCaption**</span><span class="sxs-lookup"><span data-stu-id="9a5da-131">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> <dt>

[<span data-ttu-id="9a5da-132">**Player. Close**</span><span class="sxs-lookup"><span data-stu-id="9a5da-132">**Player.close**</span></span>](player-close.md)
</dt> </dl>

 

 





