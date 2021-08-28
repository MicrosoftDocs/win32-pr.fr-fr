---
description: ICONFilePath
MS-HAID: WWAN\_profile\_v4.element\_ICONFilePath
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ICONFilePath
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50f902fe348322df2b29853aeafa65ec1cf68b71
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479915"
---
# <a name="span-idwwan_profile_v4element_iconfilepathspaniconfilepath"></a><span id="WWAN_profile_v4.element_ICONFilePath"></span>ICONFilePath

Chemin d’accès au fichier d’icône pour la connexion. L’interface utilisateur de la connexion au système d’exploitation affiche l’icône lorsqu’une connexion est établie à l’aide de ce profil.

Pour plus d’informations sur l’utilisation de cet élément, consultez la documentation v1 pour [**ICONFilePath**](./schema-iconfilepath-mbnprofile-element.md).

## <a name="element-hierarchy"></a>Hiérarchie d’éléments

[<MBNProfileExt>](element-mbnprofileext.md)  
**<ICONFilePath>**

## <a name="syntax"></a>Syntax

``` syntax
<ICONFilePath>

  iconFileType

</ICONFilePath>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributs et éléments

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs

Aucun.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Éléments enfants

Aucun.

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Éléments parents


| Élément parent | Description | 
|----------------|-------------|
| <a href="element-mbnprofileext.md">MBNProfileExt</a> | <p>L’élément <strong>MBNProfileExt</strong> est une extension de l’élément MBNProfile précédent. Il identifie un profil haut débit mobile avec un ensemble d’options plus riche que l’élément MBNProfile.</p><p>Un profil peut contenir plusieurs éléments MbnProfileExt, décrivant des paramètres de profil pour un ensemble particulier de conditions de fonctionnement. Utilisez l’élément enfant <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> pour spécifier les conditions de fonctionnement qui font d’un profil particulier le profil actif.</p> | 


 

## <a name="requirements"></a>Configuration requise


| | | <p>Espace de noms</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 
