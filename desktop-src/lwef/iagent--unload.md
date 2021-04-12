---
title: Déchargement IAgent
description: Déchargement IAgent
ms.assetid: 560301b3-c038-4c6e-b3f1-1203b618b67d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc30d6c4c06c1d292a26a2f503477dcca651dd18
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315048"
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


 

 