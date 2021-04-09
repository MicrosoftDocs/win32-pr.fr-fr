---
title: Structure VS_VERSIONINFO
description: Représente l’Organisation des données dans une ressource de version de fichier. Il s’agit de la structure racine qui contient toutes les autres structures d’informations de version de fichier.
ms.assetid: 7864510f-1894-4f17-bf7b-fd5bc1ba4aae
keywords:
- VS_VERSIONINFO des menus de structure et d’autres ressources
topic_type:
- apiref
api_name:
- VS_VERSIONINFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e2758d5553e192357296868e2dbb62f7a6733ded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106162"
---
# <a name="vs_versioninfo-structure"></a>Structure de VS \_ VERSIONINFO

Représente l’Organisation des données dans une ressource de version de fichier. Il s’agit de la structure racine qui contient toutes les autres structures d’informations de version de fichier.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  WORD             wLength;
  WORD             wValueLength;
  WORD             wType;
  WCHAR            szKey;
  WORD             Padding1;
  VS_FIXEDFILEINFO Value;
  WORD             Padding2;
  WORD             Children;
} VS_VERSIONINFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**wLength**
</dt> <dd>

Type : **Word**

</dd> <dd>

Longueur, en octets, de la structure **vs \_ VERSIONINFO** . Cette longueur n’inclut aucun remplissage qui aligne les données de ressource de version suivantes sur une limite de 32 bits.

</dd> <dt>

**wValueLength**
</dt> <dd>

Type : **Word**

</dd> <dd>

Longueur, en octets, du membre de **valeur** . Cette valeur est égale à zéro si aucun membre de **valeur** n’est associé à la structure de la version actuelle.

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

Chaîne Unicode L "info VS \_ version \_ ".

</dd> <dt>

**Padding1**
</dt> <dd>

Type : **Word**

</dd> <dd>

Contient autant de mots zéro que nécessaire pour aligner le membre **value** sur une limite de 32 bits.

</dd> <dt>

**Valeur**
</dt> <dd>

Type : **[ **vs \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)**

</dd> <dd>

Données arbitraires associées à cette structure **Visual Studio \_ VERSIONINFO** . Le membre **wValueLength** spécifie la longueur de ce membre ; Si **wValueLength** est égal à zéro, ce membre n’existe pas.

</dd> <dt>

**Padding2**
</dt> <dd>

Type : **Word**

</dd> <dd>

Autant de mots zéro que nécessaire pour aligner le membre **Children** sur une limite de 32 bits. Ces octets ne sont pas inclus dans **wValueLength**. Ce membre est facultatif.

</dd> <dt>

**Children**
</dt> <dd>

Type : **Word**

</dd> <dd>

Tableau de zéro ou une structure [**StringFileInfo**](stringfileinfo.md) , et zéro ou une structure [**VarFileInfo**](varfileinfo.md) qui sont des enfants de la structure **vs \_ VERSIONINFO** actuelle.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette structure n’est pas une véritable structure de langage C, car elle contient des membres de longueur variable. Cette structure a été créée uniquement pour représenter l’Organisation des données dans une ressource de version et n’apparaît pas dans les fichiers d’en-tête fournis avec le kit de développement logiciel (SDK) Windows.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**StringFileInfo**](stringfileinfo.md)
</dt> <dt>

[**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea)
</dt> <dt>

[**VarFileInfo**](varfileinfo.md)
</dt> <dt>

[**VS \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Informations sur la version](version-information.md)
</dt> </dl>

 

 





