---
title: Méthode de réflexion
description: Méthode de réflexion
ms.assetid: a188dd47-6af1-429d-af0a-69451f6b495e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c535912962a51961ae3f88f5cca412a55ecfa27506442aa78274fe697f2d7a26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975509"
---
# <a name="think-method"></a>Méthode de réflexion

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Affiche le texte spécifié pour le caractère spécifié dans une bulle de mot « pensée ».

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent ***. Caractères («**_CharacterID_*_»)._ *  \[ *Texte* de réflexion\]



| Partie   | Description                                                       |
|--------|-------------------------------------------------------------------|
| *Text* | Facultatif. Chaîne qui spécifie le résultat de la réflexion du caractère. |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

À l’instar de la méthode [**Speak**](speak-method.md) , la méthode **Song** est une demande en file d’attente qui affiche du texte dans une bulle de mot, sauf que la bulle de **pense** -bulle est différente visuellement. En outre, la bulle prend uniquement en charge la balise de contrôle de voix de signets (**\\ MRK**) et ignore toutes les autres balises de contrôle vocal. Contrairement à **Speak**, la méthode de **réflexion** ne modifie pas l’état d’animation du caractère.

Les propriétés de l’objet [**Balloon**](/windows/desktop/lwef/the-balloon-object) affectent la sortie des méthodes [**Speak**](speak-method.md) et **Song** . Par exemple, la propriété [**Enabled**](enabled-property.md) de l’objet **Balloon** doit avoir la **valeur true** pour que le texte s’affiche.

Si vous déclarez une référence d’objet et que vous la définissez sur cette méthode, elle retourne un objet de [**requête**](/windows/desktop/lwef/the-request-object) . En outre, si le fichier n’a pas été chargé, le serveur définit la propriété [**Status**](status-property.md) de l’objet de **requête** sur « failed » avec un numéro de code d’erreur approprié.

La césure automatique des mots de l’agent dans le mot-bulle arrête les mots à l’aide de caractères d’espace blanc (par exemple, espace ou tabulation). Toutefois, si ce n’est pas le cas, il peut endommager un mot pour l’ajuster à la bulle. Dans les langages tels que le japonais, le chinois et le thaï, où les espaces ne sont pas utilisés pour couper des mots, insérez un caractère d’espace de largeur nulle Unicode (0x200B) entre les caractères pour définir des césures lexicales.

> [!Note]  
> Définissez l’ID de langue du caractère avant d’utiliser la méthode [**Speak**](speak-method.md) pour garantir l’affichage du texte approprié dans la bulle.

 

 

 