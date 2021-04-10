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
# <a name="using-null-terminated-strings"></a><span data-ttu-id="ba4cb-103">Utilisation de chaînes terminées par un caractère null</span><span class="sxs-lookup"><span data-stu-id="ba4cb-103">Using Null-terminated Strings</span></span>

<span data-ttu-id="ba4cb-104">Vos applications Unicode doivent toujours effectuer un cast de zéro en TCHAR quand vous utilisez des chaînes terminées par le caractère null.</span><span class="sxs-lookup"><span data-stu-id="ba4cb-104">Your Unicode applications should always cast zero to TCHAR when using null-terminated strings.</span></span> <span data-ttu-id="ba4cb-105">Le code 0x0000 est l’indicateur de fin de chaîne Unicode pour une chaîne terminée par le caractère null.</span><span class="sxs-lookup"><span data-stu-id="ba4cb-105">The code 0x0000 is the Unicode string terminator for a null-terminated string.</span></span> <span data-ttu-id="ba4cb-106">Un seul octet NULL n’est pas suffisant pour ce code, car de nombreux caractères Unicode contiennent des octets de valeur NULL comme octets de poids fort ou de poids faible.</span><span class="sxs-lookup"><span data-stu-id="ba4cb-106">A single null byte is not sufficient for this code, because many Unicode characters contain null bytes as either the high or the low byte.</span></span> <span data-ttu-id="ba4cb-107">Par exemple, la lettre A, pour laquelle le code de caractère est 0x0041.</span><span class="sxs-lookup"><span data-stu-id="ba4cb-107">An example is the letter A, for which the character code is 0x0041.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba4cb-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ba4cb-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba4cb-109">Utilisation de caractères spéciaux en Unicode</span><span class="sxs-lookup"><span data-stu-id="ba4cb-109">Using Special Characters in Unicode</span></span>](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



