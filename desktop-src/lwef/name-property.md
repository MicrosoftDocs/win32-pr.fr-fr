---
title: Propriété Name (objet Characters)
description: En savoir plus sur la propriété Name de l’objet Characters. Microsoft Agent est déconseillé à partir de Windows 7.
ms.assetid: vs|msagent|~\pacontrol_2bxm.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7365550d5d4d4071cf4292e505f16e7047628cf1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118210"
---
# <a name="name-property-characters-object"></a>Propriété Name (objet Characters)

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne ou définit une chaîne qui spécifie le nom par défaut du caractère spécifié.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent ***. Caractères («**_CharacterID_*_»)._ *  \[  =  *Chaîne* de nom\]



| Partie     | Description                                                                             |
|----------|-----------------------------------------------------------------------------------------|
| *string* | Valeur de chaîne correspondant au nom du caractère (dans le paramètre de langue actuel). |



 

</dd> </dl>

## <a name="remarks"></a>Notes

Le **nom** d’un caractère peut dépendre du paramètre [**LanguageID**](languageid-property.md) du caractère. Le nom d’un caractère dans une langue peut être différent ou utiliser des caractères différents de ceux d’un autre langage. Le **nom** par défaut du caractère pour une langue spécifique est défini lorsque le caractère est compilé à l’aide de l’éditeur de caractères Microsoft Agent.

Évitez de renommer un caractère, surtout quand vous l’utilisez dans un scénario où d’autres applications clientes peuvent utiliser le même caractère. En outre, l’agent utilise le **nom** du caractère pour créer automatiquement des commandes de masquage et d’indication du caractère.

 

 




