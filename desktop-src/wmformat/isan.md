---
title: ISAN
description: L’attribut ISAN contient le numéro audiovisuel standard international qui identifie le contenu.
ms.assetid: 2937d422-f062-4373-845e-dd200512ed0b
keywords:
- Format Windows Media ISAN
topic_type:
- apiref
api_name:
- ISAN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88dc4a850edc43178deb043143ee8f9b37140507
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404683"
---
# <a name="isan"></a>ISAN

L’attribut **ISAN** contient le numéro audiovisuel standard international qui identifie le contenu.

## <a name="global-constant"></a>Constante globale

\_wszISAN g

## <a name="data-type"></a>Type de données

**\_chaîne de type WMT \_**

## <a name="remarks"></a>Notes

ISAN est une norme internationale pour identifier les travaux audiovisuels. Pour plus d’informations sur ISAN, visitez le [site Web](https://www.isan.org/)standard.

L’objet de l’éditeur de métadonnées vérifie la chaîne ISAN lorsque vous définissez cet attribut. La mise en forme de chaîne acceptable, comme décrit dans la section 4,1 de la spécification ISAN, se compose de 16 chiffres hexadécimaux, éventuellement séparés par des espaces blancs ou des traits d’Union en segments de 4 chiffres. Le nombre mis en forme doit être suivi, également éventuellement séparé par un espace ou un trait d’Union, par un caractère de vérification valide. Le caractère de vérification peut être un chiffre décimal ou une lettre majuscule. Pour plus d’informations sur la façon de dériver le numéro de chèque, reportez-vous à l’annexe A du Guide de l’utilisateur ISAN.

La chaîne ISAN standard peut être suivie d’informations sur la version. Le cas échéant, les informations de version se composent de huit chiffres hexadécimaux suivis d’un numéro de chèque. La mise en forme de ces caractères suit les mêmes règles que la chaîne de base.

## <a name="examples"></a>Exemples

Voici trois chaînes mises en forme de façon acceptable pour un exemple de ISAN.


```
00003BAB93520000G
0000 3BAB 9352 0000 G
0000-3BAB-9352-0000-G
```



La chaîne suivante montre le format d’un ISAN avec les informations de version.


```C++
0000-3BAB-9352-0000-G-0000-0000-Q
```



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




