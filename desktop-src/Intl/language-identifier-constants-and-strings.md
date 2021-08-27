---
description: Chaque identificateur de langue se compose d’un identificateur de langue primaire indiquant la langue et un identificateur de sous-langue indiquant le pays ou la région.
ms.assetid: 8a6373e0-46c2-4b1b-bc67-543f426ef15a
title: Constantes et chaînes de l’identificateur de langue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67321097d93c5f4224a86a66528f98dacce18312003062665ccc30c1377de70f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948746"
---
# <a name="language-identifier-constants-and-strings"></a>Constantes et chaînes de l’identificateur de langue

> [!IMPORTANT]
> Les constantes d’identificateur de langue sont déconseillées et leur utilisation est déconseillée. L’utilisation de noms de paramètres régionaux au lieu des identificateurs de paramètres régionaux est toujours préférable.

Pour obtenir une description des identificateurs de langue, consultez [identificateur de langue](language-identifiers.md) .

Un identificateur principal ou de sous-langue peut être défini par l’utilisateur ou prédéfini. pour obtenir les identificateurs de langue principale prédéfinis avec leurs identificateurs de sous-langue valides, consultez [[MS-LCID] : informations de référence sur les identificateurs de Code (LCID) Windows language](/openspecs/windows_protocols/ms-lcid/70feba9f-294e-491e-b6eb-56532684c37f).

> [!Note]  
> S’il n’existe aucun identificateur de sous-langue à utiliser avec un identificateur de langue primaire, votre application doit utiliser la **\_ valeur par défaut de sublang**. Il doit utiliser la sous-langue **\_ neutre** pour les ressources qui sont identiques pour toutes les sous-langues d’une langue primaire.

Un identificateur de langue principale défini par l’utilisateur a une valeur comprise dans la plage 0x0200 à 0x03ff. Toutes les autres valeurs sont réservées à l’utilisation du système d’exploitation.

Un identificateur de sous-langue défini par l’utilisateur a une valeur comprise dans la plage 0x20 à 0x3F. Toutes les autres valeurs sont réservées à l’utilisation du système d’exploitation.
