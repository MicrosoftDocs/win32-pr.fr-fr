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
# <a name="iagentspeechinputpropertiesgetlisteningtip"></a>IAgentSpeechInputProperties::GetListeningTip

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetListeningTip(
long * pbListeningTip  // address of variable for listening tip flag
);                       
```

Récupère une valeur indiquant si l’info-bulle d’écoute est activée pour l’affichage.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="pbListeningTip"></span><span id="pblisteningtip"></span><span id="PBLISTENINGTIP"></span>*pbListeningTip*
</dt> <dd>

Adresse d’une variable qui reçoit la **valeur true** si l’info-bulle d’écoute est activée pour l’affichage, ou **false** si l’info-bulle d’écoute est désactivée.

</dd> </dl>

Si [**GetEnabled**](iagentspeechinputproperties--getenabled.md) retourne la **valeur false**, l’interrogation de toute autre propriété d’entrée vocale retourne une erreur.

## <a name="see-also"></a>Voir aussi

[**IAgentSpeechInputProperties :: GetEnabled**](iagentspeechinputproperties--getenabled.md)


 

 




