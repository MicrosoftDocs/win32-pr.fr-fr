---
title: IAgentCommandsEx GetDefaultID
description: IAgentCommandsEx GetDefaultID
ms.assetid: 14079ae0-ad2c-4f38-9371-9914f8402e49
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e4dabfb1c957031b353303775921a352bf40d984ac5de1ee9c933f79a5e02cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105225"
---
# <a name="iagentcommandsexgetdefaultid"></a>IAgentCommandsEx::GetDefaultID

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetDefaultID(
   long * pdwID  // address of default command's ID
);
```

Récupère l’ID de la commande par défaut dans une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="pdwID"></span><span id="pdwid"></span><span id="PDWID"></span>*pdwID*
</dt> <dd>

Adresse d’une variable qui reçoit l’ID de la [**commande**](/windows/desktop/lwef/the-command-object) définie comme valeur par défaut.

</dd> </dl>

Cette propriété retourne l’objet de [**commande**](/windows/desktop/lwef/the-command-object) par défaut actuel dans votre collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) . La commande par défaut est en gras dans le menu contextuel du caractère. Toutefois, la définition de la commande par défaut ne modifie pas les événements de gestion des commandes ou de double-clic.

Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.

## <a name="see-also"></a>Voir aussi

[**IAgentCommandsEx::SetDefaultID**](iagentcommandsex--setdefaultid.md)


 

 