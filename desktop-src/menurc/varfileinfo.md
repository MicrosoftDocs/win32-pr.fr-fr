---
title: VarFileInfo, structure
description: Représente l’Organisation des données dans une ressource de version de fichier. Elle contient des informations sur la version qui ne dépendent pas d’une langue particulière et d’une combinaison de pages de codes.
ms.assetid: 3b667778-fb08-4195-a88e-ac04baf45fee
keywords:
- Menus de la structure VarFileInfo et autres ressources
topic_type:
- apiref
api_name:
- VarFileInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 26326403abef41d131bf25acf5d5d8be7728cd0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513810"
---
# <a name="varfileinfo-structure"></a>VarFileInfo, structure

Représente l’Organisation des données dans une ressource de version de fichier. Elle contient des informations sur la version qui ne dépendent pas d’une langue particulière et d’une combinaison de pages de codes.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  WORD  wLength;
  WORD  wValueLength;
  WORD  wType;
  WCHAR szKey;
  WORD  Padding;
  Var   Children;
} VarFileInfo;
```



## <a name="members"></a>Membres

<dl> <dt>

**wLength**
</dt> <dd>

Type : **Word**

</dd> <dd>

Longueur, en octets, du bloc **VarFileInfo** entier, y compris toutes les structures indiquées par le membre **Children** .

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

Chaîne Unicode L "VarFileInfo".

</dd> <dt>

**Remplissage**
</dt> <dd>

Type : **Word**

</dd> <dd>

Autant de mots zéro que nécessaire pour aligner le membre **Children** sur une limite de 32 bits.

</dd> <dt>

**Children**
</dt> <dd>

Type : **[ **var**](var-str.md)**

</dd> <dd>

Contient généralement une liste de langues prises en charge par l’application ou la DLL.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette structure n’est pas une véritable structure de langage C, car elle contient des membres de longueur variable. Cette structure a été créée uniquement pour représenter l’Organisation des données dans une ressource de version et n’apparaît pas dans les fichiers d’en-tête fournis avec le kit de développement logiciel (SDK) Windows.

Le membre **Children** de la structure de [**Visual Studio \_ VERSIONINFO**](vs-versioninfo.md) peut contenir zéro ou une structure **VarFileInfo** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**Var**](var-str.md)
</dt> <dt>

[**VS \_ VERSIONINFO**](vs-versioninfo.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Informations sur la version](version-information.md)
</dt> </dl>

 

 





