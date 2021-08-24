---
title: Propriété style
description: Propriété style
ms.assetid: f01d7d51-8a16-4265-b9b7-93b64f4984e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37196aead474c5364c7a94780686707b74bab0f4c4831381cf4c40e47e350e17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119715879"
---
# <a name="style-property"></a>Propriété style

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne ou définit le style de sortie de la bulle de texte du caractère.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agents. ***caractères («**_CharacterID_*_»). Style Balloon. style_ *  \[  =  \]



| Partie    | Description                                                                                                                                                                                                                                                                       |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Style* | Entier qui représente le style de sortie de l’info-bulle. Le paramètre de style est un champ de bits dont les bits correspondent à : Balloon-on (bit 0), taille-to-Text (bit 1), masquage automatique (bit 2), rythme automatique (bit 3), nombre de caractères par ligne (bits 16-23) et nombre de lignes (bits 24-31). |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

Lorsque le bit de style Balloon est défini sur 1, la bulle de mot apparaît lorsqu’une méthode [**Speak**](https://www.bing.com/search?q=**Speak**) ou [**Song**](think-method.md) est utilisée, sauf si l’utilisateur remplace ce paramètre dans la feuille de propriétés de l’agent Microsoft. Si la valeur est 0, une bulle n’apparaît pas.

Lorsque le bit de style taille-texte a la valeur 1, le mot bulle redimensionne automatiquement la hauteur de l’info-bulle sur la taille actuelle du texte de l’instruction [**Speak**](https://www.bing.com/search?q=**Speak**) ou [**Song**](think-method.md) . Lorsqu’elle est définie sur 0, la hauteur de l’info-bulle est basée sur le paramètre de propriété [**numberoflines**](numberoflines-property.md) . Si ce bit de style est défini sur 1 et que vous tentez de définir la propriété **numberoflines** , l’agent génère une erreur.

Lorsque le bit de style à masquage automatique est défini sur 1, la bulle de mot est automatiquement masquée quand la sortie orale est terminée. Lorsqu’elle est définie sur 0, la bulle reste affichée jusqu’au prochain appel [**Speak**](https://www.bing.com/search?q=**Speak**) ou [**Song**](think-method.md) , que le caractère est masqué ou que l’utilisateur clique sur le caractère ou le fait glisser.

Lorsque le bit de style de rythme automatique est défini sur 1, la bulle de mot ajuste la sortie en fonction du taux de sortie actuel, par exemple, un mot à la fois. Lorsque la sortie dépasse la taille de la bulle, le texte précédent est automatiquement défilé. Si la valeur est 0, tout le texte inclus dans une instruction [**Speak**](https://www.bing.com/search?q=**Speak**) ou [**Song**](think-method.md) s’affiche à la fois.

Pour récupérer uniquement la valeur des quatre bits inférieurs, **et** la valeur retournée par le **style** avec 255. Pour définir une valeur de bit, **ou** la valeur retournée avec la valeur des bits que vous souhaitez définir. Pour désactiver un bit, **et** la valeur retournée avec un complément du bit :


```
   Const BalloonOn = 1

   ' Turn the word balloon off
   Genie.Balloon.Style = Genie.Balloon.Style And (Not BalloonOn)
   Genie.Speak "No balloon"

   ' Turn the word balloon on
   Genie.Balloon.Style = Genie.Balloon.Style Or BalloonOn
   Genie.Speak "Balloon"
```



La propriété **style** retourne également le nombre de caractères par ligne dans l’octet inférieur du mot supérieur et le nombre de lignes dans l’octet de poids fort du mot supérieur. Bien que cette opération puisse être plus facile à lire à l’aide des propriétés [**CharsPerLine**](charsperline-property.md) et [**numberoflines**](numberoflines-property.md), la propriété **style** vous permet également de définir ces valeurs.

Par exemple, pour modifier le nombre de lignes, effacez les bits 24 à 31 avec une opération **and** logique avant de définir la nouvelle valeur en tant que produit de la nouvelle valeur Times 2 ^ 24, ajouté à la valeur existante de la propriété **style** .


```
   ' Set the number of lines to 4
   Genie.Balloon.Style = (Genie.Balloon.Style <b>AND</b> &amp;H00FFFFFF) + (4*(2^24))
```



Pour définir le nombre de caractères par ligne, effacez les bits de 16 à 23 avec une opération **and** logique avant de définir la nouvelle valeur en tant que produit de la nouvelle valeur Times 2 ^ 16, ajouté à la valeur existante de la propriété style.


```
   ' Set the number of characters per line to 16
   Genie.Balloon.Style = (Genie.Balloon.Style AND &amp;HFF00FFFF) + (16*(2^16))
```



La propriété **style** peut être définie même si l’utilisateur a désactivé l’affichage des bulles à l’aide de la feuille de propriétés Microsoft Agent. Toutefois, les valeurs du nombre de lignes doivent être comprises entre 1 et 128 et le nombre de caractères par ligne doit être compris entre 8 et 255. Si vous fournissez une valeur non valide pour la propriété **style** , agent génère une erreur.

Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.

Les valeurs par défaut de ces bits de style sont basées sur leurs paramètres lorsque le caractère est compilé avec l’éditeur de caractères Microsoft Agent.

 

 




