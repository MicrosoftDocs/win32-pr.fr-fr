---
title: Speed, propriété
description: Speed, propriété
ms.assetid: 43d0480b-d3a5-4992-a2a5-80eba37221e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaca342dde91965ab381f95671a39c4ba9fdcae040835f09867b3fabf5899a6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118745951"
---
# <a name="speed-property"></a>Speed, propriété

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne un entier long qui spécifie la vitesse actuelle de la sortie vocale du caractère.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent ***. Caractères («**_CharacterID_*_»). Vitesse_*

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette propriété retourne le paramètre de vitesse de sortie en cours pour le caractère. Pour les caractères utilisant la sortie TTS, la propriété retourne le paramètre de sortie TTS réel pour le caractère. Si TTS n’est pas activé ou que le caractère ne prend pas en charge la sortie TTS, le paramètre reflète le paramètre utilisateur pour la vitesse de sortie.

Bien que votre application ne puisse pas écrire cette valeur, vous pouvez inclure des balises **SPD** (vitesse) dans votre texte de sortie qui accélèrent temporairement la sortie d’une énoncé particulière. Toutefois, l’utilisation de la balise **SPD** pour modifier la sortie orale du caractère n’affecte pas le paramètre de propriété **Speed** . Pour plus d’informations, consultez [balises de sortie vocale](microsoft-agent-speech-output-tags.md).

 

 




