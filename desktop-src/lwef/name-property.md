---
title: Propriété Name (objet Characters)
description: Propriété Name
ms.assetid: vs|msagent|~\pacontrol_2bxm.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6e7b4a8872952cce0ae68445ec22a5599891674
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104464055"
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

 

 




