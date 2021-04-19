---
title: Erreur. Item, méthode
description: La méthode Item récupère un objet ErrorItem à partir de la file d’attente des erreurs.
ms.assetid: 3aca21ff-4c6b-4c24-a85d-3d015612a496
keywords:
- méthode Item lecteur Windows Media
- méthode Item lecteur Windows Media, classe d’erreur
- Classe d’erreur lecteur Windows Media, méthode d’élément
topic_type:
- apiref
api_name:
- Error.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5545df50fce05ff5a10a5f870d1ec07648434fe9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520788"
---
# <a name="erroritem-method"></a><span data-ttu-id="e4b66-106">Erreur. Item, méthode</span><span class="sxs-lookup"><span data-stu-id="e4b66-106">Error.item method</span></span>

<span data-ttu-id="e4b66-107">La méthode **Item** récupère un objet **ErrorItem** à partir de la file d’attente des erreurs.</span><span class="sxs-lookup"><span data-stu-id="e4b66-107">The **item** method retrieves an **ErrorItem** object from the error queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4b66-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e4b66-108">Syntax</span></span>


```JScript
retVal = Error.item(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="e4b66-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e4b66-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4b66-110">*index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e4b66-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4b66-111">**Nombre** (**long**) contenant l’index de l’objet **ErrorItem** à récupérer.</span><span class="sxs-lookup"><span data-stu-id="e4b66-111">**Number** (**long**) containing the index of the **ErrorItem** object to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4b66-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e4b66-112">Return value</span></span>

<span data-ttu-id="e4b66-113">Cette méthode retourne un objet **ErrorItem** .</span><span class="sxs-lookup"><span data-stu-id="e4b66-113">This method returns an **ErrorItem** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4b66-114">Notes</span><span class="sxs-lookup"><span data-stu-id="e4b66-114">Remarks</span></span>

<span data-ttu-id="e4b66-115">Le lecteur Windows Media peut générer un certain nombre d’erreurs en réponse à une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="e4b66-115">Windows Media Player can generate a number of errors in response to an error condition.</span></span> <span data-ttu-id="e4b66-116">Cette méthode permet de récupérer une erreur spécifique dans la file d’attente à l’aide d’un numéro d’index.</span><span class="sxs-lookup"><span data-stu-id="e4b66-116">This method allows the retrieval of a specific error in the queue by using an index number.</span></span> <span data-ttu-id="e4b66-117">Les numéros d’index de la file d’attente d’erreurs commencent par zéro.</span><span class="sxs-lookup"><span data-stu-id="e4b66-117">The index numbers for the error queue begin with zero.</span></span>

<span data-ttu-id="e4b66-118">Vous devez définir des *paramètres*. **enableErrorDialogs** sur false si vous choisissez d’afficher des messages d’erreur personnalisés.</span><span class="sxs-lookup"><span data-stu-id="e4b66-118">You should set *Settings*.**enableErrorDialogs** to false if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="e4b66-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="e4b66-119">Examples</span></span>

<span data-ttu-id="e4b66-120">L’exemple JScript suivant utilise l' *erreur*. objet **Item** dans un gestionnaire d’événements pour avertir l’utilisateur de l’erreur la plus récente.</span><span class="sxs-lookup"><span data-stu-id="e4b66-120">The following JScript example uses the *Error*.**item** object in an event handler to alert the user to the most recent error.</span></span> <span data-ttu-id="e4b66-121">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="e4b66-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE="JScript"  FOR=Player EVENT=error()>

// Store the most recent error item number.
var max = Player.error.errorCount - 1 

// Store the most recent error in an error item object.
var errItem = Player.error.item(max);

// Use the error item object to store the error info.
errDesc = errItem.errorDescription;
errNum = errItem.errorCode;

// Display the error info.
alert(errNum + "\n" + errDesc);

</SCRIPT> 

```



## <a name="requirements"></a><span data-ttu-id="e4b66-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e4b66-122">Requirements</span></span>



| <span data-ttu-id="e4b66-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e4b66-123">Requirement</span></span> | <span data-ttu-id="e4b66-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4b66-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e4b66-125">Version</span><span class="sxs-lookup"><span data-stu-id="e4b66-125">Version</span></span><br/> | <span data-ttu-id="e4b66-126">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="e4b66-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="e4b66-127">DLL</span><span class="sxs-lookup"><span data-stu-id="e4b66-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="e4b66-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4b66-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4b66-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4b66-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4b66-130">**Error, objet**</span><span class="sxs-lookup"><span data-stu-id="e4b66-130">**Error Object**</span></span>](error-object.md)
</dt> <dt>

[<span data-ttu-id="e4b66-131">**Objet ErrorItem**</span><span class="sxs-lookup"><span data-stu-id="e4b66-131">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> </dl>

 

 





