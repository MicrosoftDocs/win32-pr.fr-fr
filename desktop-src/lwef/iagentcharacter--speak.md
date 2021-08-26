---
title: IAgentCharacter parler
description: IAgentCharacter parler
ms.assetid: 3c4baf83-9e69-4048-bdaf-4ead8ea8e7cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 693b40a00b34173976410391249d3fac1a7f0684e34a6e2ae82afbd8b8169ce0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014209"
---
# <a name="iagentcharacterspeak"></a>IAgentCharacter :: Speak

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT Speak(
   BSTR bszText,    // text to speak
   BSTR bszURL,     // URL of a file to speak
   long * pdwReqID  // address of a request ID
);
```

Parle du fichier texte ou audio.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*bszText*
</dt> <dd>

Texte que le caractère doit prononcer.

</dd> <dt>

<span id="bszURL"></span><span id="bszurl"></span><span id="BSZURL"></span>*bszURL*
</dt> <dd>

URL (ou spécification de fichier) d’un fichier audio à utiliser pour la sortie parlée. Il peut s’agir d’un fichier audio standard (. WAV) ou fichier audio linguistiquement amélioré (. LWV).

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Adresse d’une variable qui reçoit l’ID de demande [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) .

</dd> </dl>

Pour utiliser cette méthode avec un caractère configuré pour parler à l’aide d’un moteur TTS (Text-to-Speech); il vous suffit de fournir le paramètre *bszText* . Vous pouvez inclure des caractères de barre verticale ( \| ) dans le paramètre *bszText* pour désigner d’autres chaînes, afin que chaque fois que le serveur traite la méthode, il choisit de façon aléatoire une autre chaîne. La prise en charge de la sortie TTS est définie lorsque le caractère est compilé à l’aide de l’éditeur de caractères Microsoft Agent.

Si vous souhaitez utiliser la sortie de fichier audio pour le caractère, spécifiez l’emplacement du fichier dans le paramètre *bszURL* . Lorsque vous utilisez le protocole HTTP pour télécharger un fichier audio, utilisez la méthode [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) pour garantir la disponibilité du fichier avant d’utiliser cette méthode. Vous pouvez utiliser le paramètre *bszText* pour spécifier les mots qui s’affichent dans la bulle de texte du caractère. Si vous spécifiez un fichier audio linguistiquement amélioré (. LWV) pour le paramètre *bszURL* et ne spécifient pas de texte, le paramètre *bszText* utilise le texte stocké dans le fichier.

La méthode [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) utilise la dernière animation jouée pour déterminer l’animation parlant à lire. Par exemple, si vous faites précéder la commande **Speak** d’un [**IAgentCharacter ::P Posez**](iagentcharacter--play.md) «**GestureRight**», le serveur lira **GestureRight** , puis l’animation **GestureRight** Speaking. Si la dernière animation jouée n’a pas d’animation parlante, Microsoft Agent lit l’animation affectée à l’état de **conversation** du caractère.

Si vous appelez [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) et que le canal audio est occupé, la sortie audio du caractère n’est pas audible, mais le texte s’affiche dans la bulle. La propriété [Enabled](enabled-property.md) de l’info-bulle du mot doit également avoir la **valeur true** pour que le texte s’affiche.

La césure automatique des mots de Microsoft Agent dans la bulle de mot, arrête les mots à l’aide de caractères d’espace blanc (par exemple, espace et tabulation). Toutefois, il peut également endommager un mot pour l’ajuster à l’info-bulle. Dans les langages tels que le japonais, le chinois et le thaï, où les espaces ne sont pas utilisés pour couper des mots, insérez un espace de largeur nulle (0x200B) Unicode entre les caractères pour définir des césures lexicales.

> [!Note]  
> Définissez l’ID de langue du caractère (à l’aide de [**IAgentCharacterEx :: SetLanguageID**](iagentcharacterex--setlanguageid.md) avant d’utiliser la méthode [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) pour garantir l’affichage du texte approprié dans la bulle.

 

## <a name="see-also"></a>Voir aussi

[**IAgentCharacter ::P poser**](iagentcharacter--play.md), [**IAgentBalloon :: GetEnabled**](iagentballoon--getenabled.md), [**IAgentCharacter ::P**](iagentcharacter--prepare.md) restante


 

 