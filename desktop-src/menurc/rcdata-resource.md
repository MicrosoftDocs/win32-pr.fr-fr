---
title: Ressource RCDATA
description: Définit une ressource de données brutes pour une application. Les ressources de données brutes permettent d’inclure des données binaires directement dans le fichier exécutable.
ms.assetid: 7535cb06-858b-4726-aaa5-43519f84d0e4
keywords:
- Menus des ressources RCDATA et autres ressources
topic_type:
- apiref
api_name:
- RCDATA
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62f813bde1195d8adcad708c40857cc11b1e7b70f696455168e174a4bf2f6cf3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847039"
---
# <a name="rcdata-resource"></a>Ressource RCDATA

Définit une ressource de données brutes pour une application. Les ressources de données brutes permettent d’inclure des données binaires directement dans le fichier exécutable.

``` syntax
nameID RCDATA  [optional-statements] {raw-data  ...}
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Nom unique ou valeur d’entier non signé 16 bits qui identifie la ressource.

</dd> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*instructions facultatives*
</dt> <dd>

Ce paramètre peut être égal à zéro ou plusieurs des instructions suivantes.



| .                                                        | Description                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Caractéristiques**](characteristics-statement.md) *DWORD*     | Informations définies par l’utilisateur sur une ressource qui peuvent être utilisées par des outils qui lisent et écrivent des fichiers de ressources. Pour plus d’informations, consultez [**caractéristiques**](characteristics-statement.md). |
| [](language-statement.md) *Langue* langue, sous- *langue* | Langue de la ressource. Pour plus d’informations, consultez [**Language**](language-statement.md).                                                                                            |
| [**Version**](version-statement.md) *DWORD*                     | Numéro de version défini par l’utilisateur pour la ressource qui peut être utilisé par les outils qui lisent et écrivent les fichiers de ressources. Pour plus d’informations, consultez [**version**](version-statement.md).              |



 

</dd> <dt>

<span id="raw-data"></span><span id="RAW-DATA"></span>*données brutes*
</dt> <dd>

Données brutes constituées d’un ou plusieurs entiers ou chaînes de caractères. Les entiers peuvent être spécifiés au format décimal, octal ou hexadécimal. pour être compatible avec les Windows 16 bits, les entiers sont stockés en tant que valeurs de **mot** . Vous pouvez stocker un entier comme valeur **DWORD** en qualifiant l’entier avec le suffixe « L ».

Les chaînes sont placées entre guillemets. RC n’ajoute pas automatiquement un caractère null de fin à une chaîne. Chaque chaîne est une séquence de caractères ANSI spécifiée, sauf si vous la qualifiez comme une chaîne de caractères larges avec le préfixe L.

Le bloc de données commence sur une limite **DWORD** et RC n’effectue aucun remplissage ou alignement des données dans le bloc de *données brutes* . Il vous incombe de garantir l’alignement correct des données dans le bloc.

</dd> </dl>

Certains attributs sont également pris en charge pour la compatibilité descendante. Pour plus d’informations, consultez [attributs de ressource communs](common-resource-attributes.md).

## <a name="examples"></a>Exemples

L’exemple suivant illustre l’utilisation de l’instruction **RCDATA** :

``` syntax
resname RCDATA
{
   "Here is an ANSI string\0",    // explicitly null-terminated 
   L"Here is a Unicode string\0", // explicitly null-terminated 
   1024,                          // integer, stored as WORD 
   7L,                            // integer, stored as DWORD 
   0x029a,                        // hex integer 
   0o733,                         // octal integer 
}
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ACCÉLÉRATEURS**](accelerators-resource.md)
</dt> <dt>

[**ATTRIBUTS**](characteristics-statement.md)
</dt> <dt>

[**SOUS**](language-statement.md)
</dt> <dt>

[**MENUS**](menu-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[**VERSION**](version-statement.md)
</dt> </dl>

 

 




