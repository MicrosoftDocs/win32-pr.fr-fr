---
title: Déchargement IAgent
description: Déchargement IAgent
ms.assetid: 560301b3-c038-4c6e-b3f1-1203b618b67d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20e6e457e2acc33c5b34800b8378d82a50d5c4aa6a139366ca1c0d241f676f9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610139"
---
# <a name="iagentunload"></a>IAgent :: Unload

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT UnLoad(
   long * dwCharID  //character ID
);
```

Décharge les données caractères pour le caractère spécifié à partir de la collection de [**caractères**](/windows/desktop/lwef/the-characters-object) .

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

ID du caractère.

</dd> </dl>

Utilisez cette méthode lorsque vous n’avez plus besoin d’un caractère, pour libérer de la mémoire utilisée pour stocker des informations sur le caractère. Si vous accédez de nouveau au caractère, utilisez la méthode [**Load**](load-method.md) .

## <a name="see-also"></a>Voir aussi

[**IAgent :: Load**](iagent--load.md)


 

 