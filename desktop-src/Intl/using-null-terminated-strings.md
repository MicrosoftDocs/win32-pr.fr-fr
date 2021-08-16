---
description: Vos applications Unicode doivent toujours effectuer un cast de zéro en TCHAR quand vous utilisez des chaînes terminées par le caractère null.
ms.assetid: 43bbf0ab-9b69-4f7d-acda-d0f8b6caf4b5
title: Utilisation de chaînes terminées par un caractère null
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d0a5f27048bde2af75eca28626a562473ceffcc66f3f2f23509beca4fba06ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631779"
---
# <a name="using-null-terminated-strings"></a>Utilisation de chaînes terminées par un caractère null

Vos applications Unicode doivent toujours effectuer un cast de zéro en TCHAR quand vous utilisez des chaînes terminées par le caractère null. Le code 0x0000 est l’indicateur de fin de chaîne Unicode pour une chaîne terminée par le caractère null. Un seul octet NULL n’est pas suffisant pour ce code, car de nombreux caractères Unicode contiennent des octets de valeur NULL comme octets de poids fort ou de poids faible. Par exemple, la lettre A, pour laquelle le code de caractère est 0x0041.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de caractères spéciaux en Unicode](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



