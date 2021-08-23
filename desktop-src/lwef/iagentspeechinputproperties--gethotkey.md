---
title: IAgentSpeechInputProperties GetHotKey
description: IAgentSpeechInputProperties GetHotKey
ms.assetid: b93e5b46-b8f8-4ca4-8417-7626b97d8928
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a66e4f3fe070a944ecd9800a6712e8ae4db8d333913e5cfe85c027565cf1cf77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609379"
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


 

 




