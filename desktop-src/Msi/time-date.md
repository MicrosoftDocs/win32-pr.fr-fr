---
description: Le type de données date/heure correspond à l’heure et à la date stockées individuellement, en utilisant des entiers non signés comme champs de bits, compressés comme suit.
ms.assetid: 02c6076e-7f81-489c-9997-1435dec81852
title: Heure/date
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b973143c2043419e4a54348917aa5d38fa97ff67
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119633"
---
# <a name="timedate"></a>Heure/date

Le type de données date/heure correspond à l’heure et à la date stockées individuellement, en utilisant des entiers non signés comme champs de bits, compressés comme suit.

## <a name="time"></a>Temps

L’heure est encodée dans un entier non signé de 2 octets avec les champs de bits suivants.



| Contenu           | Bits        | Plage de valeurs |
|--------------------|-------------|-------------|
| heures              | 0 1 2 3 4   | 0–23        |
| minutes            | 5 6 7 8 9 A | 0–59        |
| intervalles de 2 secondes | B C D E F   | 0 – 29        |



 

## <a name="date"></a>Date

La date est encodée dans un entier non signé de 2 octets avec les champs de bits suivants.



| Contenu | Bits          | Plage de valeurs              |
|----------|---------------|--------------------------|
| year     | 0 1 2 3 4 5 6 | 0 – 119 (par rapport à 1980) |
| month    | 7 8 9 A       | 1–12                     |
| day      | B C D E F     | 1–31                     |



 

 

 



