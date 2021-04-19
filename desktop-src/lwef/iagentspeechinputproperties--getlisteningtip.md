---
title: IAgentSpeechInputProperties GetListeningTip
description: IAgentSpeechInputProperties GetListeningTip
ms.assetid: b0488a54-03f8-43ce-935c-dd49c6ed5dbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91218fb7935edb68458d540a8f35fe5402b317ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106545727"
---
# <a name="iagentspeechinputpropertiesgetlisteningtip"></a><span data-ttu-id="49c61-103">IAgentSpeechInputProperties::GetListeningTip</span><span class="sxs-lookup"><span data-stu-id="49c61-103">IAgentSpeechInputProperties::GetListeningTip</span></span>

<span data-ttu-id="49c61-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="49c61-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetListeningTip(
long * pbListeningTip  // address of variable for listening tip flag
);                       
```

<span data-ttu-id="49c61-105">Récupère une valeur indiquant si l’info-bulle d’écoute est activée pour l’affichage.</span><span class="sxs-lookup"><span data-stu-id="49c61-105">Retrieves a value indicating whether the Listening Tip is enabled for display.</span></span>

-   <span data-ttu-id="49c61-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="49c61-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="49c61-107"><span id="pbListeningTip"></span><span id="pblisteningtip"></span><span id="PBLISTENINGTIP"></span>*pbListeningTip*</span><span class="sxs-lookup"><span data-stu-id="49c61-107"><span id="pbListeningTip"></span><span id="pblisteningtip"></span><span id="PBLISTENINGTIP"></span>*pbListeningTip*</span></span>
</dt> <dd>

<span data-ttu-id="49c61-108">Adresse d’une variable qui reçoit la **valeur true** si l’info-bulle d’écoute est activée pour l’affichage, ou **false** si l’info-bulle d’écoute est désactivée.</span><span class="sxs-lookup"><span data-stu-id="49c61-108">Address of a variable that receives **True** if the Listening Tip is enabled for display, or **False** if the Listening Tip is disabled.</span></span>

</dd> </dl>

<span data-ttu-id="49c61-109">Si [**GetEnabled**](iagentspeechinputproperties--getenabled.md) retourne la **valeur false**, l’interrogation de toute autre propriété d’entrée vocale retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="49c61-109">If [**GetEnabled**](iagentspeechinputproperties--getenabled.md) returns **False**, querying any other speech input properties returns an error.</span></span>

## <a name="see-also"></a><span data-ttu-id="49c61-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49c61-110">See Also</span></span>

[<span data-ttu-id="49c61-111">**IAgentSpeechInputProperties :: GetEnabled**</span><span class="sxs-lookup"><span data-stu-id="49c61-111">**IAgentSpeechInputProperties::GetEnabled**</span></span>](iagentspeechinputproperties--getenabled.md)


 

 




