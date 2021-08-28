---
description: Les actions personnalisées ICE communiquent en appelant MsiProcessMessage et en publiant un \_ message de type utilisateur INSTALLMESSAGE.
ms.assetid: 36307589-de0e-4eaf-b439-e7ba3cd96fb3
title: Instructions relatives aux messages ICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d603175dbecc12b0b9524db1a02d9ca677f61c87
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887446"
---
# <a name="ice-message-guidelines"></a>Instructions relatives aux messages ICE

Les actions personnalisées ICE communiquent en appelant [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) et en publiant un \_ message de type utilisateur INSTALLMESSAGE.

Lors de la création d’une chaîne de message pour une action personnalisée ICE, mettez en forme la chaîne comme suit.

*Nom de la glace* &lt; onglet &gt; *type de message* onglet &lt; &gt; *Description* onglet &lt; &gt; *URL ou emplacement* onglet nom de la table nom de la colonne onglet nom de la &lt; &gt;  &lt; &gt; *colonne* &lt; &gt;  &lt; &gt;  &lt; &gt;  clé primaire onglet clé primaire. . . (répétez cette opération pour autant de clés primaires que nécessaire)

Les trois premiers champs de la chaîne sont requis dans chaque message.

Le champ type de message spécifie si la glace signale un message d’erreur, d’erreur, d’avertissement ou d’information.



| Valeur | type de message                                                                                                                                                          |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Message d’échec signalant l’échec de l’action personnalisée ICE.                                                                                                       |
| 1     | Message d’erreur lors de la création de la base de données qui provoque un comportement incorrect.                                                                                             |
| 2     | Message d’avertissement création de la base de données qui provoque un comportement incorrect dans certains cas. Les avertissements peuvent également signaler des effets secondaires inattendus de la création de bases de données. |
| 3     | Message d’information.                                                                                                                                                |



 

Si l’aide n’est pas disponible, le champ URL d’aide peut être une chaîne vide.

Les messages d’erreur et d’avertissement doivent fournir le nom de la table, le nom de la colonne et les champs de clé primaire. Si l’un de ces champs est omis, tous les champs qui suivent le premier champ vide doivent être ignorés dans le message. Par exemple, un nom de table est fourni sans nom de colonne ni clé primaire, ni nom de table et un nom de colonne est fourni sans clé primaire. Toutefois, un nom de colonne et des clés primaires ne peuvent pas être utilisés sans nom de table. Plusieurs clés primaires peuvent être listées jusqu’à ce que toutes les clés primaires de cette table aient reçu des valeurs.

## <a name="examples"></a>Exemples

Premier message illustré par l' [exemple de code Ice en C++](sample-ice-in-c-.md):

« ICE01 \\ T3 \\ TLA 04/29/1998 par <insérer le nom de l’auteur ici> ».

Deuxième message publié par l’exemple de code ICE :

« ICE01 \\ T3 \\ tLast a modifié 05/06/1999 en <insérer le nom de l’auteur ici> ».

Troisième message publié par l’exemple de code ICE.

« ICE01 \\ T3 \\ tSimple Ice à illustrer le concept de glace ».

 

 



