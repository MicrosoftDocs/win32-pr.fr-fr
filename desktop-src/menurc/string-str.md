---
title: Structure de chaîne
description: Représente l’Organisation des données dans une ressource de version de fichier. Elle contient une chaîne qui décrit un aspect spécifique d’un fichier, par exemple, la version d’un fichier, ses mentions de droits d’auteur ou ses marques.
ms.assetid: fcc5ac68-4aec-4a3b-aa92-96fc50cc4ca2
keywords:
- Menus de structure de chaîne et autres ressources
topic_type:
- apiref
api_name:
- String
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a6db2c10e981ae059a46e84e7abfc4d6dfc372fc3c75c76cfc20fd8a8f42735d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776729"
---
# <a name="string-structure"></a>Structure de chaîne

Représente l’Organisation des données dans une ressource de version de fichier. Elle contient une chaîne qui décrit un aspect spécifique d’un fichier, par exemple, la version d’un fichier, ses mentions de droits d’auteur ou ses marques.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  WORD  wLength;
  WORD  wValueLength;
  WORD  wType;
  WCHAR szKey;
  WORD  Padding;
  WORD  Value;
} String;
```



## <a name="members"></a>Membres

<dl> <dt>

**wLength**
</dt> <dd>

Type : **Word**

</dd> <dd>

Longueur, en octets, de cette structure de **chaîne** .

</dd> <dt>

**wValueLength**
</dt> <dd>

Type : **Word**

</dd> <dd>

Taille, en termes, du membre de **valeur** .

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

Chaîne Unicode arbitraire. Le membre **szKey** peut être une ou plusieurs des valeurs suivantes. Ces valeurs sont uniquement des indications.

<dt>

<span id="Comments"></span><span id="comments"></span><span id="COMMENTS"></span>

<span id="Comments"></span><span id="comments"></span><span id="COMMENTS"></span>**Inclus**


</dt> <dd>

Le membre de **valeur** contient toutes les informations supplémentaires qui doivent être affichées à des fins de diagnostic. Cette chaîne peut être une longueur arbitraire.

</dd> <dt>

<span id="CompanyName"></span><span id="companyname"></span><span id="COMPANYNAME"></span>

<span id="CompanyName"></span><span id="companyname"></span><span id="COMPANYNAME"></span>**Prennent**


</dt> <dd>

Le membre de **valeur** identifie la société qui a produit le fichier. Par exemple, « Microsoft Corporation » ou « Standard Microsystems Corporation, Inc. »

</dd> <dt>

<span id="FileDescription"></span><span id="filedescription"></span><span id="FILEDESCRIPTION"></span>

<span id="FileDescription"></span><span id="filedescription"></span><span id="FILEDESCRIPTION"></span>**FileDescription**


</dt> <dd>

Le membre de **valeur** décrit le fichier de façon à ce qu’il puisse être présenté aux utilisateurs. Cette chaîne peut être présentée dans une zone de liste lorsque l’utilisateur choisit les fichiers à installer. par exemple, « pilote de clavier pour les claviers de style AT » ou « Microsoft Word pour Windows ».

</dd> <dt>

<span id="FileVersion"></span><span id="fileversion"></span><span id="FILEVERSION"></span>

<span id="FileVersion"></span><span id="fileversion"></span><span id="FILEVERSION"></span>**FileVersion**


</dt> <dd>

Le membre de **valeur** identifie la version de ce fichier. Par exemple, la **valeur** peut être « 3.00 a » ou « 5,00. RC2 ».

</dd> <dt>

<span id="InternalName"></span><span id="internalname"></span><span id="INTERNALNAME"></span>

<span id="InternalName"></span><span id="internalname"></span><span id="INTERNALNAME"></span>**InternalName**


</dt> <dd>

Le membre de **valeur** identifie le nom interne du fichier, s’il en existe un. par exemple, cette chaîne peut contenir le nom de module pour une DLL, un nom de périphérique virtuel pour un Windows appareil virtuel ou un nom de périphérique pour un pilote de périphérique MS-DOS.

</dd> <dt>

<span id="LegalCopyright"></span><span id="legalcopyright"></span><span id="LEGALCOPYRIGHT"></span>

<span id="LegalCopyright"></span><span id="legalcopyright"></span><span id="LEGALCOPYRIGHT"></span>**LegalCopyright**


</dt> <dd>

Le membre **value** décrit toutes les mentions de droits d’auteur, marques déposées et marques déposées qui s’appliquent au fichier. Cela doit inclure le texte intégral de la totalité des mentions, symboles légaux, dates de copyright, numéros de marques, etc. En anglais, cette chaîne doit être au format « Copyright Microsoft Corp. 1990 1994 ».

</dd> <dt>

<span id="LegalTrademarks"></span><span id="legaltrademarks"></span><span id="LEGALTRADEMARKS"></span>

<span id="LegalTrademarks"></span><span id="legaltrademarks"></span><span id="LEGALTRADEMARKS"></span>**LegalTrademarks**


</dt> <dd>

Le membre **value** décrit toutes les marques et les marques déposées qui s’appliquent au fichier. Cela doit inclure le texte intégral de la totalité des mentions, symboles légaux, numéros de marques, etc. En français, cette chaîne doit avoir le format « Windows est une marque de Microsoft Corporation ».

</dd> <dt>

<span id="OriginalFilename"></span><span id="originalfilename"></span><span id="ORIGINALFILENAME"></span>

<span id="OriginalFilename"></span><span id="originalfilename"></span><span id="ORIGINALFILENAME"></span>**OriginalFilename**


</dt> <dd>

Le membre de **valeur** identifie le nom d’origine du fichier, à l’exclusion du chemin d’accès. Cela permet à une application de déterminer si un fichier a été renommé par un utilisateur. Ce nom peut ne pas être au format MS-DOS 8,3 Si le fichier est spécifique à un système de fichiers non FAT.

</dd> <dt>

<span id="PrivateBuild"></span><span id="privatebuild"></span><span id="PRIVATEBUILD"></span>

<span id="PrivateBuild"></span><span id="privatebuild"></span><span id="PRIVATEBUILD"></span>**PrivateBuild**


</dt> <dd>

Le membre de **valeur** décrit par qui, où et pourquoi cette version privée du fichier a été générée. Cette chaîne doit être présente uniquement si l’indicateur **vs \_ FF \_ PRIVATEBUILD** est défini dans le membre **dwFileFlags** de la structure [**vs \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) . Par exemple, la **valeur** peut être « générée par Oscar sur \\ OSCAR2 ».

</dd> <dt>

<span id="ProductName"></span><span id="productname"></span><span id="PRODUCTNAME"></span>

<span id="ProductName"></span><span id="productname"></span><span id="PRODUCTNAME"></span>**ProductName**


</dt> <dd>

Le membre de **valeur** identifie le nom du produit avec lequel ce fichier est distribué. Par exemple, cette chaîne peut être « Microsoft Windows ».

</dd> <dt>

<span id="ProductVersion"></span><span id="productversion"></span><span id="PRODUCTVERSION"></span>

<span id="ProductVersion"></span><span id="productversion"></span><span id="PRODUCTVERSION"></span>**ProductVersion**


</dt> <dd>

Le membre de **valeur** identifie la version du produit avec lequel ce fichier est distribué. Par exemple, la **valeur** peut être « 3.00 a » ou « 5,00. RC2 ».

</dd> <dt>

<span id="SpecialBuild"></span><span id="specialbuild"></span><span id="SPECIALBUILD"></span>

<span id="SpecialBuild"></span><span id="specialbuild"></span><span id="SPECIALBUILD"></span>**SpecialBuild**


</dt> <dd>

Le membre **value** décrit la différence entre cette version du fichier et la version normale. Cette entrée doit être présente uniquement si l’indicateur **vs \_ FF \_ SPECIALBUILD** est défini dans le membre **dwFileFlags** de la structure [**vs \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) . Par exemple, la **valeur** peut être « build privée pour les problèmes de souris de résolution Olivetti sur les ordinateurs M250 et M250E ».

</dd> </dl> </dd> <dt>

**Remplissage**
</dt> <dd>

Type : **Word**

</dd> <dd>

Autant de mots zéro que nécessaire pour aligner le membre **value** sur une limite de 32 bits.

</dd> <dt>

**Valeur**
</dt> <dd>

Type : **Word**

</dd> <dd>

Chaîne se terminant par zéro. Pour plus d’informations, consultez la description du membre **szKey** .

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette structure n’est pas une véritable structure de langage C, car elle contient des membres de longueur variable. cette structure a été créée uniquement pour représenter l’organisation des données dans une ressource de version et n’apparaît pas dans les fichiers d’en-tête fournis avec le kit de développement logiciel (SDK) Windows.

Une structure de **chaîne** peut avoir la valeur **szKey** , par exemple, « CompanyName » et la **valeur** « Microsoft Corporation ». Une autre structure de **chaîne** avec la même valeur **szKey** peut contenir la **valeur** « Microsoft GmbH ». Cela peut se produire si la deuxième structure de **chaîne** était associée à une structure [**STRINGTABLE**](stringtable.md) dont la valeur **SzKey** est 040704b0 c’est-à-dire, allemande/Unicode.

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

[**VS \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)
</dt> <dt>

[**StringFileInfo**](stringfileinfo.md)
</dt> <dt>

[**VS \_ VERSIONINFO**](vs-versioninfo.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Informations sur la version](version-information.md)
</dt> </dl>

 

 





