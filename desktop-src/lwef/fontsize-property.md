---
title: FontSize, propriété (objet Commands)
description: En savoir plus sur la propriété de l’objet FontSize Commands. Microsoft Agent est déconseillé à partir de Windows 7.
ms.assetid: a1113a3a-5da8-4077-8565-168963c503d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5cee9d4852a68792fe1270ebd9c91e51f567adc546433d7142de68392e9f8dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118751432"
---
# <a name="fontsize-property-commands-object"></a>FontSize, propriété (objet Commands)

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne ou définit la taille de police utilisée dans le menu contextuel du caractère.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agents. ***caractères («**_CharacterID_*_»). Points de commande. FontSize_ *  \[  =  \]



| Partie     | Description                                              |
|----------|----------------------------------------------------------|
| *Moments* | Valeur entière de type long spécifiant la taille de police en points. |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

La propriété **FontSize** définit la taille en points de la police utilisée pour afficher le texte dans le menu contextuel du caractère. La valeur par défaut du paramètre de police est basée sur le paramètre de police de menu du paramètre **LanguageID** du caractère ou, si cela n’est pas défini, le paramètre de langue par défaut de l’utilisateur.

Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.

 

 




