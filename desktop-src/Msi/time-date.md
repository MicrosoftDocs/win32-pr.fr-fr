---
description: Le type de données date/heure correspond à l’heure et à la date stockées individuellement, en utilisant des entiers non signés comme champs de bits, compressés comme suit.
ms.assetid: 02c6076e-7f81-489c-9997-1435dec81852
title: Heure/date
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c3c5cccc2f1211918b52008f0d81a7e4693dfd14766696b77cd184d75f4309d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810739"
---
# <a name="timedate"></a>Heure/date

Le type de données date/heure correspond à l’heure et à la date stockées individuellement, en utilisant des entiers non signés comme champs de bits, compressés comme suit.

## <a name="time"></a>Heure

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



 

 

 



