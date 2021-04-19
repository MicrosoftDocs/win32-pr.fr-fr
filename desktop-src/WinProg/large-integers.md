---
title: Entiers volumineux
description: Les grandes fonctions et structures entières offraient à l’origine une prise en charge des valeurs 64 bits sur Windows 32 bits.
ms.assetid: db4ffbd5-d9e4-4c95-83cc-6f0691c080d2
keywords:
- entiers volumineux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ab6276ff6879ce5b72f198e3ccbd247f456e70
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106513545"
---
# <a name="large-integers"></a>Entiers volumineux

Les grandes fonctions et structures entières offraient à l’origine une prise en charge des valeurs 64 bits sur Windows 32 bits. Désormais, votre compilateur C peut prendre en charge les entiers 64 bits en mode natif. Par exemple, Microsoft Visual C++ prend en charge le type d’entier de taille [**\_ \_ Int64**](/windows/desktop/Midl/--int64) . Pour plus d’informations, consultez la documentation fournie avec votre compilateur C.

Pour plus d’informations sur les entiers 64 bits sous Windows 64 bits, consultez [nouveaux types de données](/windows/desktop/WinProg64/the-new-data-types).

## <a name="large-integer-operations"></a>Opérations sur les entiers volumineux

Les applications peuvent multiplier des entiers 32 bits signés ou non signés, générant des résultats 64 bits, à l’aide des fonctions [**Int32x32To64**](/windows/desktop/api/Winnt/nf-winnt-int32x32to64) et [**UInt32x32To64**](/windows/desktop/api/Winnt/nf-winnt-uint32x32to64) . Les applications peuvent décaler les bits des valeurs 64 bits vers la gauche ou vers la droite à l’aide des fonctions [**Int64ShllMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shllmod32), [**Int64ShraMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shramod32)et [**Int64ShrlMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shrlmod32) . Ces fonctions fournissent des décalages logiques et arithmétiques.

Les applications peuvent également multiplier et diviser des valeurs 32 bits en une seule opération à l’aide de la fonction [**MulDiv**](/windows/desktop/api/Winbase/nf-winbase-muldiv) . Bien que le résultat de l’opération soit une valeur 32 bits, la fonction stocke le résultat intermédiaire sous la forme d’une valeur 64 bits, de sorte que les informations ne sont pas perdues lorsque de grandes valeurs 32 bits sont multipliées et divisées.

## <a name="large-integer-reference"></a>Référence d’entier long

-   [Fonctions entières de type long](large-integer-functions.md)
-   [Structures d’entiers longs](large-integer-structures.md)

 

 