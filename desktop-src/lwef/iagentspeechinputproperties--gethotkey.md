---
title: IAgentSpeechInputProperties GetHotKey
description: IAgentSpeechInputProperties GetHotKey
ms.assetid: b93e5b46-b8f8-4ca4-8417-7626b97d8928
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e672b26f97cfbe92bc71d0ceab165e100c3ecf92
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028475"
---
# <a name="iagentspeechinputpropertiesgethotkey"></a>IAgentSpeechInputProperties::GetHotKey

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetHotKey(
BSTR * pbszHotCharKey  // address of variable for listening key 
);                        
```

Récupère l’attribution de clavier actuelle pour la clé d’écoute de l’entrée vocale.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="pbszHotCharKey"></span><span id="pbszhotcharkey"></span><span id="PBSZHOTCHARKEY"></span>*pbszHotCharKey*
</dt> <dd>

Adresse d’un BSTR qui reçoit le paramètre de raccourci clavier actuel utilisé pour ouvrir le canal audio pour l’entrée vocale.

</dd> </dl>

Si [**GetEnabled**](iagentspeechinputproperties--getenabled.md) retourne la **valeur false**, l’interrogation de ce paramètre génère une erreur.

## <a name="see-also"></a>Voir aussi

[**IAgentSpeechInputProperties :: GetEnabled**](iagentspeechinputproperties--getenabled.md)


 

 




