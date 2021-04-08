---
title: StringFileInfo, structure
description: Représente l’Organisation des données dans une ressource de version de fichier. Elle contient des informations de version qui peuvent être affichées pour une langue et une page de codes particulières.
ms.assetid: dda38fee-e8ea-4e58-b5ee-72e4cdb08f42
keywords:
- Menus de la structure StringFileInfo et autres ressources
topic_type:
- apiref
api_name:
- StringFileInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f252077a5536194e635281d4b4178a457f7a82cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941801"
---
# <a name="stringfileinfo-structure"></a>StringFileInfo, structure

Représente l’Organisation des données dans une ressource de version de fichier. Elle contient des informations de version qui peuvent être affichées pour une langue et une page de codes particulières.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  WORD        wLength;
  WORD        wValueLength;
  WORD        wType;
  WCHAR       szKey;
  WORD        Padding;
  StringTable Children;
} StringFileInfo;
```



## <a name="members"></a>Membres

<dl> <dt>

**wLength**
</dt> <dd>

Type : **Word**

</dd> <dd>

Longueur, en octets, du bloc **StringFileInfo** entier, y compris toutes les structures indiquées par le membre **Children** .

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

Chaîne Unicode L "StringFileInfo".

</dd> <dt>

**Remplissage**
</dt> <dd>

Type : **Word**

</dd> <dd>

Autant de mots zéro que nécessaire pour aligner le membre **Children** sur une limite de 32 bits.

</dd> <dt>

**Children**
</dt> <dd>

Type : **[ **STRINGTABLE**](stringtable.md)**

</dd> <dd>

Tableau d’une ou de plusieurs structures [**STRINGTABLE**](stringtable.md) . Chaque membre **szKey** de la structure **STRINGTABLE** indique la langue et la page de codes appropriées pour l’affichage du texte dans cette structure **STRINGTABLE** .

</dd> </dl>

## <a name="remarks"></a>Notes

Cette structure n’est pas une véritable structure de langage C, car elle contient des membres de longueur variable. Cette structure a été créée uniquement pour représenter l’Organisation des données dans une ressource de version et n’apparaît pas dans les fichiers d’en-tête fournis avec le kit de développement logiciel (SDK) Windows.

Le membre **Children** de la structure de [**Visual Studio \_ VERSIONINFO**](vs-versioninfo.md) peut contenir zéro ou plusieurs structures **StringFileInfo** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**StringTable**](stringtable.md)
</dt> <dt>

[**String**](string-str.md)
</dt> <dt>

[**VS \_ VERSIONINFO**](vs-versioninfo.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Informations sur la version](version-information.md)
</dt> </dl>

 

 





