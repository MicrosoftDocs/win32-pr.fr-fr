---
title: Propriété FontCharSet
description: Propriété FontCharSet
ms.assetid: 2f23a242-d620-4766-8f59-cf158aa55969
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e4561de9af823b4213266a93b7bfa2e29588c3c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311017"
---
# <a name="fontcharset-property"></a>Propriété FontCharSet

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne ou définit le jeu de caractères pour la police affichée dans la bulle de texte du caractère spécifié.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent ***. Caractères («*** CharacterID * * * »). Valeur Balloon. FontCharSet* *  \[  =  \]



| Partie    | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *value* | Valeur entière qui spécifie le jeu de caractères utilisé par la police. Voici quelques paramètres courants pour la valeur : 0 caractères Windows standard (ANSI).<br/> 1 jeu de caractères par défaut.<br/> 2 le jeu de caractères de symbole.<br/> 128 jeu de caractères codés sur deux octets (DBCS) propre à la version japonaise de Windows.<br/> 129 jeu de caractères codés sur deux octets (DBCS) propre à la version coréenne de Windows.<br/> 134 jeu de caractères codés sur deux octets (DBCS) propre à la version de Windows en chinois simplifié.<br/> 136 jeu de caractères codés sur deux octets (DBCS) propre à la version en chinois traditionnel de Windows.<br/> 255 caractères étendus normalement affichés par les applications Microsoft MS-DOS.<br/> Pour les autres valeurs de jeu de caractères, consultez la documentation du kit de développement Platform SDK.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Notes

La valeur par défaut du jeu de caractères de la bulle de texte d’un caractère est définie dans l’éditeur de caractères Microsoft Agent. En outre, l’utilisateur peut remplacer les paramètres de jeu de caractères pour tous les caractères de la feuille de propriétés de l’agent Microsoft.

Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.

> [!Note]  
> Si vous utilisez un caractère que vous n’avez pas compilé, vérifiez les propriétés [**FontName**](fontname-property.md) et **FontCharSet** pour déterminer s’ils sont appropriés pour vos paramètres régionaux. Vous devrez peut-être définir ces valeurs avant d’utiliser la méthode [**Speak**](speak-method.md) pour garantir l’affichage du texte approprié dans la bulle.

 

## <a name="see-also"></a>Voir aussi

[**FontName, propriété**](fontname-property.md)


 

 





