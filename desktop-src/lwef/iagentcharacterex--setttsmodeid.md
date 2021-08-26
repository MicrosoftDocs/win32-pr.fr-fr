---
title: IAgentCharacterEx SetTTSModeID
description: IAgentCharacterEx SetTTSModeID
ms.assetid: 66ed792a-1693-45dc-b9a8-eebe772c5af9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a24195fd177abbde3c6423f966df67ba0faeaf315038d7f8cb0b4ca136f16c3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114719"
---
# <a name="iagentcharacterexsetttsmodeid"></a>IAgentCharacterEx::SetTTSModeID

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT SetTTSModeID(
   BSTR bszModeID  // TTS engine ID
);
```

Définit l’ID de mode du jeu de moteurs TTS pour le caractère.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="bszModeID"></span><span id="bszmodeid"></span><span id="BSZMODEID"></span>*bszModeID*
</dt> <dd>

Paramètre d’ID de mode du moteur TTS pour le caractère.

> [!Note]  
> **IAgentCharacterEx : SetTTSModeID** peut échouer si Speech.dll n’est pas installé et que le moteur que vous spécifiez ne correspond pas au paramètre de mode TTS compilé du caractère.

 

</dd> </dl>

Ce paramètre détermine le mode de moteur par défaut pour la sortie TTS orale d’un caractère. L’ID de mode pour un moteur TTS (conversion de texte par synthèse vocale) est le GUID défini par le fournisseur de reconnaissance vocale qui identifie de façon unique le mode du moteur (mis en forme à l’aide d’accolades et de tirets). Pour plus d’informations, consultez la [documentation du kit de développement logiciel (SDK) Microsoft Speech](https://msdn.microsoft.com/library/ee705648.aspx).

Si vous définissez un ID de mode TTS, il remplace la tentative de serveur pour qu’il corresponde à un moteur de reconnaissance vocale en fonction de l’ID de mode TTS compilé du caractère, de l’ID de langue système actuel et de l’ID de langue actuel du caractère. Toutefois, si vous tentez de définir un ID de mode lorsque l’utilisateur a désactivé la sortie vocale dans la feuille de propriétés de l’agent Microsoft ou que le moteur associé n’est pas installé, cet appel échoue.

Si vous ne définissez pas un ID de mode de moteur TTS pour le caractère, le serveur définit un moteur qui correspond au paramètre de langue du caractère (à l’aide des interfaces de l’API Microsoft Speech). La définition de cette propriété chargera le moteur associé s’il n’est pas déjà chargé.

Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.

La configuration requise du moteur de reconnaissance vocale de Microsoft Agent est basée sur l’API Microsoft Speech. Les moteurs prenant en charge les spécifications SAPI de Microsoft Agent peuvent être installés et utilisés avec l’agent.

## <a name="see-also"></a>Voir aussi

[**IAgentCharacterEx:GetTTSModeID**](iagentcharacterex--getttsmodeid.md)


 

 




