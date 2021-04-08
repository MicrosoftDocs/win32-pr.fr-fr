---
title: Désinscription IAgent
description: Désinscription IAgent
ms.assetid: d81cde72-f9ff-45aa-9dbf-faea9a478c3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 796e033ac823ee7c79fe5312fab2c57dec36e694
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842281"
---
# <a name="iagentunregister"></a>IAgent :: Unregister

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT Unregister(
   long dwSinkID  //notification sink ID
);
```

Décharge les données caractères pour le caractère spécifié à partir de la collection de [**caractères**](/windows/desktop/lwef/the-characters-object) .

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="dwSinkID"></span><span id="dwsinkid"></span><span id="DWSINKID"></span>*dwSinkID*
</dt> <dd>

ID du récepteur de notifications.

</dd> </dl>

Utilisez cette méthode lorsque vous n’avez plus besoin des services Microsoft Agent, tels que le moment où votre application s’arrête.

## <a name="see-also"></a>Voir aussi

[**IAgent :: Register**](iagent--register.md)


 

 