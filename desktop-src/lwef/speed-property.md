---
title: Speed, propriété
description: Speed, propriété
ms.assetid: 43d0480b-d3a5-4992-a2a5-80eba37221e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24738ac17d7efac45f2aefe7e4beb5ec018915a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106543402"
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

*agent ***. Caractères («*** CharacterID * * * »). Temps**

</dd> </dl>

## <a name="remarks"></a>Notes

Cette propriété retourne le paramètre de vitesse de sortie en cours pour le caractère. Pour les caractères utilisant la sortie TTS, la propriété retourne le paramètre de sortie TTS réel pour le caractère. Si TTS n’est pas activé ou que le caractère ne prend pas en charge la sortie TTS, le paramètre reflète le paramètre utilisateur pour la vitesse de sortie.

Bien que votre application ne puisse pas écrire cette valeur, vous pouvez inclure des balises **SPD** (vitesse) dans votre texte de sortie qui accélèrent temporairement la sortie d’une énoncé particulière. Toutefois, l’utilisation de la balise **SPD** pour modifier la sortie orale du caractère n’affecte pas le paramètre de propriété **Speed** . Pour plus d’informations, consultez [balises de sortie vocale](microsoft-agent-speech-output-tags.md).

 

 




