---
title: Propriété tonale
description: Propriété tonale
ms.assetid: 98b2ada3-93c6-4fa1-bf12-353eb229c30c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e346ea0fbb7ebb819d8f00b2fc6aab1ab95e72f391bddc696da18a49f0b2a09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118475409"
---
# <a name="pitch-property"></a>Propriété tonale

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description_"></span><span id="description_"></span><span id="DESCRIPTION_"></span>**Descriptive** 
</dt> <dd>

Retourne un entier long pour le paramètre de hauteur de la sortie vocale (TTS) du caractère spécifié.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent ***. Caractères («**_CharacterID_*_»). Espacement_*

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette propriété s’applique uniquement aux caractères configurés pour la sortie TTS. Si le caractère ne prend pas en charge la sortie TTS, cette propriété retourne la valeur zéro (0).

Bien que votre application ne puisse pas écrire cette valeur, vous pouvez inclure dans votre texte de sortie des balises **Pit** qui augmenteront temporairement le pas pour une énoncé particulière. Toutefois, l’utilisation de la balise **Pit** pour changer le pas de valeur ne modifie pas le paramètre **de propriété de** pas. Pour plus d’informations, consultez [balises de sortie vocale](pit-tag.md).

 

 




