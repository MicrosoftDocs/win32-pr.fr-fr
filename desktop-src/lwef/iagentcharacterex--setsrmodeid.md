---
title: IAgentCharacterEx SetSRModeID
description: IAgentCharacterEx SetSRModeID
ms.assetid: 8f9072ec-1f64-4f5c-972d-cd6799ce028c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 390d7e0126fe5ef62273cf6d7d23ada25c26bbdb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127221012"
---
# <a name="iagentcharacterexsetsrmodeid"></a>IAgentCharacterEx::SetSRModeID

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT SetSRModeID(
   BSTR bszModeID  // speech recognition engine ID
);
```

Définit l’ID de mode du moteur de reconnaissance vocale défini pour le caractère.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

bszModeID

Paramètre de l’ID de mode du moteur de reconnaissance vocale pour le caractère.

Ce paramètre définit le moteur pour l’entrée vocale d’un caractère. L’ID de mode d’un moteur de reconnaissance vocale est le GUID défini par le fournisseur de reconnaissance vocale qui identifie de façon unique le mode du moteur (mis en forme à l’aide d’accolades et de tirets). Pour plus d’informations, consultez la [documentation du kit de développement logiciel (SDK) Microsoft Speech](https://msdn.microsoft.com/library/ee705648.aspx).

Si vous spécifiez un ID de mode qui ne correspond pas au paramètre de langue du caractère, si l’utilisateur a désactivé la reconnaissance vocale (dans la feuille de propriétés de l’agent Microsoft) ou si le moteur n’est pas installé, cet appel échoue. Si vous ne définissez pas un ID de mode de moteur de reconnaissance vocale pour le caractère, le serveur définit celui qui correspond au paramètre de langue du caractère (à l’aide des interfaces de l’API Microsoft Speech).

Lorsque l’entrée vocale est activée dans la feuille de propriétés de l’agent (options de caractères avancés), la définition de cette propriété chargera le moteur associé (s’il n’est pas déjà chargé) et démarrez les services vocaux. Autrement dit, la clé d’écoute est disponible et l’info-bulle d’écoute est affichable. (La clé d’écoute et l’info-bulle d’écoute sont activées uniquement si elles sont également activées dans les options de caractères avancés.) Toutefois, si vous interrogez la propriété alors que la reconnaissance vocale est désactivée, le serveur ne démarre pas les services vocaux.

Cette propriété s’applique uniquement au client du caractère ; le paramètre ne reflète pas le paramètre pour d’autres clients du caractère ou d’autres caractères du client.

La configuration requise du moteur de reconnaissance vocale de Microsoft Agent est basée sur l’API Microsoft Speech. Les moteurs prenant en charge les spécifications SAPI de Microsoft Agent peuvent être installés et utilisés avec l’agent.

## <a name="see-also"></a>Voir aussi

[**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md)


 

 




