---
title: RESOURCEHEADER, structure
description: Contient des informations sur l’en-tête de ressource lui-même et les données spécifiques à cette ressource.
ms.assetid: e0eba7b3-a275-4ffe-9347-46361213cf48
keywords:
- Menus de la structure RESOURCEHEADER et autres ressources
topic_type:
- apiref
api_name:
- RESOURCEHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 41b436ebd6aeb5dc31f8ed773fbe7b12a1586185
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512147"
---
# <a name="resourceheader-structure"></a>RESOURCEHEADER, structure

Contient des informations sur l’en-tête de ressource lui-même et les données spécifiques à cette ressource. Cette structure n’est pas une véritable structure de langage C, car elle contient des membres de longueur variable. La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  DWORD DataSize;
  DWORD HeaderSize;
  DWORD TYPE;
  DWORD NAME;
  DWORD DataVersion;
  WORD  MemoryFlags;
  WORD  LanguageId;
  DWORD Version;
  DWORD Characteristics;
} RESOURCEHEADER;
```



## <a name="members"></a>Membres

<dl> <dt>

**DataSize**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Taille, en octets, des données qui suivent l’en-tête de ressource pour cette ressource particulière. Elle n’inclut pas le remplissage des fichiers entre cette ressource et toute ressource qui la suit dans le fichier de ressources.

</dd> <dt>

**HeaderSize**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Taille, en octets, des données d’en-tête de ressource qui suivent.

</dd> <dt>

**TYPE**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Type de ressource. Le membre de **type** peut être une valeur numérique ou une chaîne Unicode terminée par le caractère null qui spécifie le nom du type. Consultez la section Notes suivante pour obtenir une description des membres de type **nom** ou **ordinal** .

Si le membre de **type** est une valeur numérique, il peut spécifier un type de ressource standard ou défini par l’utilisateur. Si le membre est une chaîne, il s’agit d’un type de ressource défini par l’utilisateur. Pour obtenir la liste des types de ressources prédéfinis, consultez [types de ressources](/windows/desktop/menurc/resource-types).

Les valeurs inférieures à 256 sont réservées à l’utilisation du système.

</dd> <dt>

**NAME**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Nom qui identifie la ressource particulière. Le membre de **nom** , comme le membre de **type** , peut être une valeur numérique ou une chaîne Unicode terminée par le caractère null. Consultez la section Notes suivante pour obtenir une description des membres de type **nom** ou **ordinal** .

Vous n’avez pas besoin d’ajouter un remplissage pour l’alignement **DWORD** entre le **type** et les membres de **nom** , car ils contiennent des données **Word** . Toutefois, vous devrez peut-être ajouter un **mot** de remplissage après le membre **Name** pour aligner le reste de l’en-tête sur les limites **DWORD** .

</dd> <dt>

**DataVersion**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Version de données de ressource prédéfinie. Cela permet de déterminer la version des données de ressource que l’application doit utiliser.

</dd> <dt>

**MemoryFlags**
</dt> <dd>

Type : **Word**

</dd> <dd>

Ensemble d’indicateurs d’attribut qui peuvent décrire l’état de la ressource. Modificateurs dans le. Fichier de script RC assignez ces attributs à la ressource. Les identificateurs de script peuvent assigner les valeurs d’indicateur suivantes.

Les applications n’utilisent pas ces attributs. Les attributs sont autorisés dans le script à des fins de compatibilité descendante avec les scripts existants, mais ils sont ignorés. Les ressources sont chargées lorsque le module correspondant est chargé, et sont libérées quand le module est déchargé.

<dt>

<span id="MOVEABLE"></span><span id="moveable"></span>

**Moveable** (0x0010)


</dt> <dd></dd> <dt>

<span id="FIXED"></span><span id="fixed"></span>

**corrigé** (~ déplaçable)


</dt> <dd></dd> <dt>

<span id="PURE"></span><span id="pure"></span>

**Pur** (0x0020)


</dt> <dd></dd> <dt>

<span id="IMPURE"></span><span id="impure"></span>

**IMpures** (~ pure)


</dt> <dd></dd> <dt>

<span id="PRELOAD"></span><span id="preload"></span>

**Préchargement** (0x0040)


</dt> <dd></dd> <dt>

<span id="LOADONCALL"></span><span id="loadoncall"></span>

**LOADONCALL** (~ préchargement)


</dt> <dd></dd> <dt>

<span id="DISCARDABLE"></span><span id="discardable"></span>

À **Ignorer** (0x1000)


</dt> <dd></dd> </dl> </dd> <dt>

**LanguageId**
</dt> <dd>

Type : **Word**

</dd> <dd>

Langue de la ressource ou de l’ensemble de ressources. Définissez la valeur de ce membre avec l’instruction facultative de définition de ressource de [langage](./language-statement.md) . Les paramètres sont des constantes du fichier Winnt. h.

Chaque ressource contient un identificateur de langue afin que le système ou l’application puisse sélectionner une langue adaptée aux paramètres régionaux actuels du système. S’il existe plusieurs ressources du même type et du même nom qui diffèrent uniquement par la langue des chaînes dans les ressources, vous devez spécifier un **LanguageID** pour chacun d’entre eux.

</dd> <dt>

**Version**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Numéro de version défini par l’utilisateur pour les données de ressources que les outils peuvent utiliser pour lire et écrire des fichiers de ressources. Définissez cette valeur avec l’instruction facultative de définition de ressource de [version](./version-statement.md) .

</dd> <dt>

**Caractéristiques**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Spécifie des informations définies par l’utilisateur sur la ressource que les outils peuvent utiliser pour lire et écrire des fichiers de ressources. Définissez cette valeur avec les [caractéristiques](./characteristics-statement.md) facultatives de l’instruction de définition de ressource.

</dd> </dl>

## <a name="remarks"></a>Notes

Un membre de type variable est appelé « **nom** » ou « membre **ordinal** », et il est utilisé à la plupart des emplacements dans le fichier de ressources où un identificateur s’affiche. Le premier **mot** d’un membre de type **nom** ou **ordinal** indique si le membre est une valeur numérique ou une chaîne. Si le premier **mot** du membre est égal à la valeur 0xFFFF, qui est un caractère Unicode non valide, le **mot** suivant est un numéro de type. Dans le cas contraire, le membre contient une chaîne Unicode et le premier **mot** du membre est le premier caractère de la chaîne de nom. Pour plus d’informations sur les instructions de définition de ressource, consultez [instructions de définition de ressource](./resource-definition-statements.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Ressources](resources.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[Instruction de caractéristiques](./characteristics-statement.md)
</dt> <dt>

[LANGUAGE (instruction)](./language-statement.md)
</dt> <dt>

[VERSION (instruction)](./version-statement.md)
</dt> </dl>

 

