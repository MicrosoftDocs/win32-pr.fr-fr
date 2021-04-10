---
description: Vos applications Unicode doivent toujours effectuer un cast de zéro en TCHAR quand vous utilisez des chaînes terminées par le caractère null.
ms.assetid: 43bbf0ab-9b69-4f7d-acda-d0f8b6caf4b5
title: Utilisation de chaînes terminées par un caractère null
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce12079fa3d0c5a88af369a347f1cd655136ee09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210935"
---
# <a name="using-null-terminated-strings"></a>Utilisation de chaînes terminées par un caractère null

Vos applications Unicode doivent toujours effectuer un cast de zéro en TCHAR quand vous utilisez des chaînes terminées par le caractère null. Le code 0x0000 est l’indicateur de fin de chaîne Unicode pour une chaîne terminée par le caractère null. Un seul octet NULL n’est pas suffisant pour ce code, car de nombreux caractères Unicode contiennent des octets de valeur NULL comme octets de poids fort ou de poids faible. Par exemple, la lettre A, pour laquelle le code de caractère est 0x0041.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de caractères spéciaux en Unicode](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



