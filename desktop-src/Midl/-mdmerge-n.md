---
title: commutateur/n
description: Le commutateur/n spécifie la profondeur de composition pour la composition des fichiers de métadonnées.
ms.assetid: 7A1F8A9E-B3CC-4BB2-BF50-5662D4560280
keywords:
- /n Switch MIDL
topic_type:
- apiref
api_name:
- /n
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3e9575995d80a4c61b5e91be7c5cfc1c802abed892af8cfa653f62c66e602b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430969"
---
# <a name="n-switch"></a>commutateur/n

Le commutateur **/n** spécifie la profondeur de composition pour la composition des fichiers de métadonnées.

``` syntax
mdmerge /n namespace_depth
```

## <a name="switch-options"></a>Options de commutateur

<dl> <dt>

*profondeur de l’espace de noms \_* 
</dt> <dd>

Spécifie la profondeur de l’espace de noms à composer en un seul fichier de métadonnées.

</dd> </dl>

## <a name="remarks"></a>Remarques

Voici les formats de valeurs possibles que vous pouvez spécifier avec le commutateur **/n** .



| Format de valeur                   | Description                                                                     |
|--------------------------------|---------------------------------------------------------------------------------|
| > Int32 0                   | Compose tous les types à la profondeur d’espace de noms spécifiée dans le commutateur.               |
| -1                             | Composez tous les types dans un fichier IDL par espace de noms.                              |
| <namespace>: Int32 > 0 | Compose tous les types avec l’espace de noms correspondant à la profondeur spécifiée dans le commutateur. |
| <namespace>:-1           | Compose tous les types avec l’espace de noms correspondant dans un fichier par espace de noms.          |



 

Le tableau suivant présente les résultats de différentes combinaisons du commutateur **/n** qui fonctionnent sur ces espaces de noms.

-   Windows. Foundation. Collections. interface iiterable
-   Windows. L'. DirectUI. Controls. Button
-   Windows. L'. DirectUI. Controls. ListView
-   Windows. L'. Immersif. application. point. Target
-   Windows. Web. Syndication. RSS



| Commutateurs                         | Résultats                                                                                                                                                                                                                                                       | Explication                                                                                                                                                                                                                                                                                                                        |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **/n :-1**  / **n :1**               | Windows.winmd                                                                                                                                                                                                                                                | Le dernier commutateur/n remplace tous les commutateurs-n précédents.                                                                                                                                                                                                                                                                           |
| **/n :-1/n : Windows. INTERFACE UTILISATEUR : 2**         | <dl> <dt>Windows. Foundation. winmd</dt> <dt>Windows. UI. winmd</dt> <dt>Windows. Web. Syndication. winmd</dt> </dl> | <dl> <dt>**Windows. Foundation** est toujours composé à – n :2.</dt> <dt>**Windows.** Les types d’interface utilisateur sont regroupés.</dt> <dt>**Windows. Web. Syndication** est composé dans n :-1.</dt> </dl>       |
| **/n : 1/n : Windows. L'. DirectUI : 3** | <dl> <dt>Windows. Foundation. winmd</dt> <dt>Windows. L'. DirectUI. winmd</dt> <dt>Windows. winmd</dt> </dl>       | <dl> <dt>**Windows. Foundation** est toujours composé à – n :2.</dt> <dt>**Windows. L'. DirectUI** est composé au niveau 3.</dt> <dt>Tous les autres types sont composés au niveau 1.</dt> </dl> |



 

Voici les règles de gestion de plusieurs instances du commutateur **/n** .

-   L’instance la plus spécifique est prioritaire. Par exemple, si vous spécifiez **– n :A.B.C : 4 – n :A.B : 5**, MDMERGE résout un. b. c. D au niveau 4, car a. b. c est plus spécifique que A.B. A. B. E. F se résout à Depth 5, car il correspond à A. B mais pas à A.B.C.
-   La dernière instance est en vigueur. Par exemple, si vous spécifiez **– n :5 – n :2**, les types sont composés au niveau 2.
-   Ces deux règles s’appliquent. Si vous spécifiez – n :A.B.C : 4 – n :A.B.C : 1, l’espace de noms A. B. C est composé au niveau 1.

## <a name="examples"></a>Exemples

**mdmerge.exe-Metadata \_ dir $ ( \_ chemin des métadonnées du SDK \_ )-i $ ( \_ chemin des métadonnées du kit de développement logiciel (SDK \_ ) interne \_ )-o $ (obj \_ Path) \\ $O \\ SystemMetadata-v-n :-1-n : Windows. Base : 2**

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|--------------------------------|
| Client<br/> | Windows 8<br/>           |
| Serveur<br/> | Windows Server 2012<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> </dl>

 

 





