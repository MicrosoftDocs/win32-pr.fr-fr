---
title: IAgentCharacterEx GetTTSModeID
description: IAgentCharacterEx GetTTSModeID
ms.assetid: e7b3c576-dc3c-40de-8d09-8e7f4b79250b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62a77e78755345c0993ed5723080b0b3f4b8297a
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104030881"
---
# <a name="iagentcharacterexgetttsmodeid"></a>IAgentCharacterEx::GetTTSModeID

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetTTSModeID(
   BSTR * pbszModeID  // address of TTS engine ID
);
```

Récupère l’ID de mode du jeu de moteurs TTS pour le caractère.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="pbszModeID"></span><span id="pbszmodeid"></span><span id="PBSZMODEID"></span>*pbszModeID*
</dt> <dd>

Adresse d’un BSTR qui reçoit le paramètre de l’ID de mode du moteur TTS pour le caractère.

</dd> </dl>

Ce paramètre renvoie l’ID de mode de moteur TTS (conversion de texte par synthèse vocale) pour la sortie parlée d’un caractère. L’ID de mode d’un moteur TTS est une représentation sous forme de chaîne du GUID (mis en forme à l’aide d’accolades et de tirets) défini par le fournisseur vocal qui identifie de façon unique le moteur. Pour plus d’informations, consultez la [documentation du kit de développement logiciel (SDK) Microsoft Speech](https://msdn.microsoft.com/library/ee705648.aspx). L’interrogation de cette propriété chargera le moteur associé s’il n’est pas déjà chargé.

Si vous ne définissez pas un ID de mode de moteur TTS pour le caractère, le serveur tente de renvoyer un moteur qui correspond (à l’aide des interfaces de l’API Microsoft Speech) au paramètre TTS compilé du caractère et au paramètre de langue actuel du caractère. Si elles sont différentes, le paramètre de langue du caractère remplace le paramètre de mode créé. Si vous n’avez pas défini le paramètre de langue du caractère, la langue du caractère est l’ID de langue par défaut de l’utilisateur, et le serveur tente la correspondance en fonction de cet ID de langue.

Cette fonction n’échoue pas si [**IAgentAudioObjectProperties :: GetEnabled**](https://www.bing.com/search?q=**IAgentAudioObjectProperties::GetEnabled**) retourne **false**.

Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.

La configuration requise du moteur de reconnaissance vocale de Microsoft Agent est basée sur l’API Microsoft Speech. Les moteurs prenant en charge les spécifications SAPI de Microsoft Agent peuvent être installés et utilisés avec l’agent.

## <a name="see-also"></a>Voir aussi

[**IAgentCharacterEx::SetTTSModeID**](iagentcharacterex--setttsmodeid.md)


 

 




