---
title: StringTable, structure
description: Représente l’Organisation des données dans une ressource de version de fichier. Elle contient des informations de mise en forme de la langue et de la page de codes pour les chaînes spécifiées par le membre Children. Une page de codes est un jeu de caractères ordonné.
ms.assetid: e8e9d654-b515-434c-ac38-79d333a8d7cb
keywords:
- Menus de la structure StringTable et autres ressources
topic_type:
- apiref
api_name:
- StringTable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 01ad7a2436c4b32f0f2fa09ab801339903ed55f35be80bbfc43c4542da4e4ce5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119720659"
---
# <a name="stringtable-structure"></a>StringTable, structure

Représente l’Organisation des données dans une ressource de version de fichier. Elle contient des informations de mise en forme de la langue et de la page de codes pour les chaînes spécifiées par le membre **Children** . Une page de codes est un jeu de caractères ordonné.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  WORD   wLength;
  WORD   wValueLength;
  WORD   wType;
  WCHAR  szKey;
  WORD   Padding;
  String Children;
} StringTable;
```



## <a name="members"></a>Membres

<dl> <dt>

**wLength**
</dt> <dd>

Type : **Word**

</dd> <dd>

Longueur, en octets, de cette structure **STRINGTABLE** , y compris toutes les structures indiquées par le membre **Children** .

</dd> <dt>

**wValueLength**
</dt> <dd>

Type : **Word**

</dd> <dd>

Ce membre est toujours égal à zéro.

</dd> <dt>

**wType**
</dt> <dd>

Type : **Word**

</dd> <dd>

Type de données de la ressource de version. Ce membre est 1 si la ressource de version contient des données texte et 0 si la ressource de version contient des données binaires.

</dd> <dt>

**szKey**
</dt> <dd>

Type : **WCHAR**

</dd> <dd>

Nombre hexadécimal à 8 chiffres stocké sous la forme d’une chaîne Unicode. Les quatre chiffres les plus significatifs représentent l’identificateur de langue. Les quatre chiffres les moins significatifs représentent la page de codes pour laquelle les données sont mises en forme. Chaque identificateur de langue Microsoft standard contient deux parties : les 10 bits de poids faible spécifient la langue principale et les 6 bits de poids fort spécifient la sous-langue. Pour obtenir une table des identificateurs valides, consultez.

</dd> <dt>

**Remplissage**
</dt> <dd>

Type : **Word**

</dd> <dd>

Autant de mots zéro que nécessaire pour aligner le membre **Children** sur une limite de 32 bits.

</dd> <dt>

**Children**
</dt> <dd>

Type : **[ **chaîne**](string-str.md)**

</dd> <dd>

Tableau d’une ou de plusieurs structures de [**chaîne**](string-str.md) .

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette structure n’est pas une véritable structure de langage C, car elle contient des membres de longueur variable. cette structure a été créée uniquement pour représenter l’organisation des données dans une ressource de version et n’apparaît pas dans les fichiers d’en-tête fournis avec le kit de développement logiciel (SDK) Windows.

Le membre **Children** de la structure [**StringFileInfo**](stringfileinfo.md) contient au moins une structure **STRINGTABLE** .

Définissez la partie page de codes du membre **szKey** sur la valeur hexadécimale 0x04b0 pour indiquer la page de codes Unicode, ou sur la valeur hexadécimale de la page de codes appropriée pour le composant de langage. Une fois que vous avez choisi la valeur de la page de codes, vous devez continuer à utiliser la même valeur dans les révisions ultérieures du fichier.

Un fichier exécutable ou une DLL qui prend en charge plusieurs langages doit avoir une ressource de version pour chaque langue, plutôt qu’une ressource de version unique qui contient des chaînes dans plusieurs langues. Toutefois, si vous utilisez la structure [**var**](var-str.md) pour répertorier les langues prises en charge par votre application, le nombre de structures **STRINGTABLE** dans la ressource de version est directement lié au nombre de paires d’identificateurs de langue ou de page de code dans le membre **value** de la structure **var** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**String**](string-str.md)
</dt> <dt>

[**StringFileInfo**](stringfileinfo.md)
</dt> <dt>

[**Var**](var-str.md)
</dt> <dt>

[**VarFileInfo**](varfileinfo.md)
</dt> <dt>

[**VS \_ VERSIONINFO**](vs-versioninfo.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Informations sur la version](version-information.md)
</dt> </dl>

 

 





