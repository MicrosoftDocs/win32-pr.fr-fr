---
title: Var, structure
description: Représente l’Organisation des données dans une ressource de version de fichier. Il contient généralement une liste de paires de langue et d’identificateur de page de codes que la version de l’application ou de la DLL prend en charge.
ms.assetid: edd2f2e5-100c-49c2-841f-f75e2909460a
keywords:
- Menus de structure var et autres ressources
topic_type:
- apiref
api_name:
- Var
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 48537009b56d2b37f4508871049463a65a12965c31658e932716832955503f42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119599579"
---
# <a name="var-structure"></a>Var, structure

Représente l’Organisation des données dans une ressource de version de fichier. Il contient généralement une liste de paires de langue et d’identificateur de page de codes que la version de l’application ou de la DLL prend en charge.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  WORD  wLength;
  WORD  wValueLength;
  WORD  wType;
  WCHAR szKey;
  WORD  Padding;
  DWORD Value;
} Var;
```



## <a name="members"></a>Membres

<dl> <dt>

**wLength**
</dt> <dd>

Type : **Word**

</dd> <dd>

Longueur, en octets, de la structure **var** .

</dd> <dt>

**wValueLength**
</dt> <dd>

Type : **Word**

</dd> <dd>

Longueur, en octets, du membre de **valeur** .

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

Chaîne Unicode L « translation ».

</dd> <dt>

**Remplissage**
</dt> <dd>

Type : **Word**

</dd> <dd>

Autant de mots zéro que nécessaire pour aligner le membre **value** sur une limite de 32 bits.

</dd> <dt>

**Valeur**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Tableau d’une ou de plusieurs valeurs qui sont des paires d’identificateurs de page de codes et de langage. Pour plus d’informations, consultez la section Notes suivante.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette structure n’est pas une véritable structure de langage C, car elle contient des membres de longueur variable. cette structure a été créée uniquement pour représenter l’organisation des données dans une ressource de version et n’apparaît pas dans les fichiers d’en-tête fournis avec le kit de développement logiciel (SDK) Windows.

Si vous utilisez la structure **var** pour répertorier les langues prises en charge par votre application ou dll au lieu d’utiliser plusieurs ressources de version, utilisez le membre **value** pour contenir un tableau de valeurs **DWORD** indiquant les combinaisons de langue et de page de codes prises en charge par ce fichier. Le mot de poids faible de chaque **DWORD** doit contenir un identificateur de langue Microsoft, et le mot de poids fort doit contenir le numéro de page de codes IBM. Le mot de poids fort ou de poids faible peut être égal à zéro, ce qui indique que le fichier est indépendant de la langue ou de la page de codes. Si la structure **var** est omise, le fichier est interprété comme une langue et une page de codes indépendantes.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**VarFileInfo**](varfileinfo.md)
</dt> <dt>

[**StringFileInfo**](stringfileinfo.md)
</dt> <dt>

[**StringTable**](stringtable.md)
</dt> <dt>

[**VS \_ VERSIONINFO**](vs-versioninfo.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Informations sur la version](version-information.md)
</dt> </dl>

 

 





