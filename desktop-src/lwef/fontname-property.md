---
title: Propriété FontName (objet Commands)
description: En savoir plus sur la propriété de l’objet Commands FontName. Microsoft Agent est déconseillé à partir de Windows 7.
ms.assetid: 7de3653e-9b4d-4a31-82d5-243f10e2743b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 739fceae4e73788f408306f6af08713173c99843
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068255"
---
# <a name="fontname-property-commands-object"></a>Propriété FontName (objet Commands)

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne ou définit la police utilisée dans le menu contextuel du caractère.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agents. ***caractères («**_CharacterID_*_»). Police Commands. FontName_ *  \[  =  \]



| Partie   | Description                                      |
|--------|--------------------------------------------------|
| *Police* | Valeur de chaîne correspondant au nom de la police. |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

La propriété **FontName** définit la police utilisée pour afficher le texte dans le menu contextuel du caractère. La valeur par défaut du paramètre de police est basée sur le paramètre de police de menu pour le paramètre **LanguageID** du caractère, ou--si ce n’est pas le cas, le paramètre ID de langue par défaut de l’utilisateur.

Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.

 

 




