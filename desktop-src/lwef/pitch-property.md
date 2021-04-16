---
title: Propriété tonale
description: Propriété tonale
ms.assetid: 98b2ada3-93c6-4fa1-bf12-353eb229c30c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 998ee4bcf77878062425086d67066040f5d58421
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380395"
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

*agent ***. Caractères («*** CharacterID * * * »). Donn**

</dd> </dl>

## <a name="remarks"></a>Notes

Cette propriété s’applique uniquement aux caractères configurés pour la sortie TTS. Si le caractère ne prend pas en charge la sortie TTS, cette propriété retourne la valeur zéro (0).

Bien que votre application ne puisse pas écrire cette valeur, vous pouvez inclure dans votre texte de sortie des balises **Pit** qui augmenteront temporairement le pas pour une énoncé particulière. Toutefois, l’utilisation de la balise **Pit** pour changer le pas de valeur ne modifie pas le paramètre **de propriété de** pas. Pour plus d’informations, consultez [balises de sortie vocale](pit-tag.md).

 

 




