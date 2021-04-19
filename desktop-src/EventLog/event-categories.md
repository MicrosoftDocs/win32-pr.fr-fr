---
description: Les catégories vous aident à organiser les événements afin que les observateur d’événements puissent les filtrer. Chaque source d’événement peut définir ses propres catégories numérotées et les chaînes de texte auxquelles elles sont mappées.
ms.assetid: ddba8066-b6b9-42a6-b49f-cbae8f97ef6d
title: Catégories d’événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efd84a095754bd51499edf5a21ebea0ade042d75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516935"
---
# <a name="event-categories"></a>Catégories d’événements

Les catégories vous aident à organiser les événements afin que les observateur d’événements puissent les filtrer. Chaque [source d’événement](event-sources.md) peut définir ses propres catégories numérotées et les chaînes de texte auxquelles elles sont mappées.

Les catégories doivent être numérotées consécutivement, en commençant par le chiffre 1. Les catégories elles-mêmes sont définies dans un fichier de message. Par exemple, utilisez la syntaxe suivante pour déclarer trois catégories d’événements. Dans observateur d’événements, les événements qui utilisent ces catégories auront la catégorie 1, la catégorie 2 ou la catégorie 3 affichée dans la colonne **catégorie** .

``` syntax
MessageId=0x1
SymbolicName=CATEGORY_1
Language=English
Category 1
.

MessageId=0x2
SymbolicName=CATEGORY_2
Language=English
Category 2
.

MessageId=0x3
SymbolicName=CATEGORY_3
Language=English
Category 3
.
```

Les catégories peuvent être stockées dans un fichier de message distinct ou dans un fichier qui contient des messages d’autres types. Si vous créez un seul fichier de message, assurez-vous que les catégories sont les premiers messages du fichier. Pour plus d’informations sur la création et l’utilisation de fichiers de messages, consultez [fichiers de messages](message-files.md).

Le nombre total de catégories est stocké dans la valeur **CategoryCount** pour la source de l’événement.

 

 



