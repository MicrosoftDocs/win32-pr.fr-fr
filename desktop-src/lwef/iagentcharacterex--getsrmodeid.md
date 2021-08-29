---
title: IAgentCharacterEx GetSRModeID
description: IAgentCharacterEx GetSRModeID
ms.assetid: 28049680-8245-49f3-9ecd-13c7605f10ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d43e09722aef8f39f802c6a4be037a2002cab564be535554b2450668faed90d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114759"
---
# <a name="iagentcharacterexgetsrmodeid"></a>IAgentCharacterEx::GetSRModeID

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetSRModeID(
   BSTR * pbszModeID  // address of speech recognition engine ID
);
```

Récupère l’ID de mode du moteur de reconnaissance vocale défini pour le caractère.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="pbszModeID"></span><span id="pbszmodeid"></span><span id="PBSZMODEID"></span>*pbszModeID*
</dt> <dd>

Adresse d’un BSTR qui reçoit le paramètre de l’ID de mode du moteur de reconnaissance vocale pour le caractère.

</dd> </dl>

Ce paramètre retourne le jeu de moteurs pour l’entrée vocale d’un caractère. L’ID de mode d’un moteur de reconnaissance vocale est une représentation sous forme de chaîne du GUID (mis en forme à l’aide d’accolades et de tirets) par le fournisseur de reconnaissance vocale qui identifie le moteur de manière unique. Pour plus d’informations, consultez la [documentation du kit de développement logiciel (SDK) Microsoft Speech](https://msdn.microsoft.com/library/ee705648.aspx).

Si vous ne définissez pas un ID de mode de moteur de reconnaissance vocale pour le caractère, le serveur retourne un moteur qui correspond au paramètre de langue du caractère (à l’aide des interfaces de l’API Microsoft Speech). Si aucun moteur de reconnaissance vocale correspondant n’est disponible pour le caractère, le serveur retourne une chaîne null (vide).

Lorsque l’entrée vocale est activée (dans la fenêtre Options de caractères avancés), l’interrogation ou la définition de cette propriété chargera le moteur associé (s’il n’est pas déjà chargé) et démarrera les services de reconnaissance vocale. Autrement dit, la clé d’écoute est disponible et l’info-bulle d’écoute est affichable. (La clé d’écoute et l’info-bulle d’écoute sont activées uniquement si elles sont également activées dans les options de caractères avancés.) Toutefois, si vous interrogez la propriété alors que la reconnaissance vocale est désactivée, le serveur ne démarre pas les services vocaux et retourne une chaîne null (chaîne vide).

Cette fonction retourne uniquement le paramètre de l’utilisation du caractère par l’application cliente ; le paramètre ne reflète pas les autres clients du caractère ou d’autres caractères de votre application cliente.

Cette fonction n’échoue pas si [**IAgentSpeechInputProperties :: GetEnabled**](iagentspeechinputproperties--getenabled.md) retourne **false**.

La configuration requise du moteur de reconnaissance vocale de Microsoft Agent est basée sur l’API Microsoft Speech. Les moteurs prenant en charge les spécifications SAPI de Microsoft Agent peuvent être installés et utilisés avec l’agent.

## <a name="see-also"></a>Voir aussi

[**IAgentCharacterEx::SetSRModeID**](iagentcharacterex--setsrmodeid.md)


 

 




