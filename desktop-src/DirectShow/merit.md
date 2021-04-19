---
description: Les valeurs mérite définissent l’ordre dans lequel le gestionnaire de graphes de filtre tente d’ajouter des filtres lors de la génération du graphique.
ms.assetid: 9e026675-e0a9-4c82-9b57-ab0e7d9592ea
title: Mérite (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 947a13d78f58c12c236ec31f0eeee1dc6d44f1d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535222"
---
# <a name="merit"></a>Mérite

Les valeurs mérite définissent l’ordre dans lequel le gestionnaire de graphes de filtre tente d’ajouter des filtres lors de la génération du graphique.

<dl> <span id="MERIT_PREFERRED"></span><span id="merit_preferred"></span>**Mérite \_ Préféré** (0x800000) mérite <span id="MERIT_NORMAL"></span> <span id="merit_normal"></span> **\_ normal** (0x600000) <span id="MERIT_UNLIKELY"></span> <span id="merit_unlikely"></span> **mérite \_ improbable** (0x400000) mériter <span id="MERIT_DO_NOT_USE"></span> <span id="merit_do_not_use"></span> **\_ n' \_ \_ utiliser pas** (0x200000) le compresseur de <span id="MERIT_SW_COMPRESSOR"></span> <span id="merit_sw_compressor"></span> **\_ SW \_** () <span id="MERIT_HW_COMPRESSOR"></span> <span id="merit_hw_compressor"></span> **\_ \_** mérite le compresseur de matériel (0x100050)
</dl>

## <a name="remarks"></a>Notes

Chaque filtre est inscrit avec une valeur mérite. Lorsque le gestionnaire de graphique de filtre crée un graphique, il énumère tous les filtres inscrits avec le type de média correct. Il les essaie ensuite dans l’ordre de leur mérite, du plus élevé au plus bas. (Il utilise des critères supplémentaires pour choisir entre les filtres avec des mérites identiques.) Il ne tente jamais de filtrer avec une valeur mérite inférieure ou égale à la valeur **mérite \_ do \_ not \_ use**.

Un filtre qui ne doit jamais être pris en compte pour une lecture ordinaire doit avoir un mérite de **mérite \_ n' \_ \_ utilise pas au** maximum. Les filtres peuvent être enregistrés avec des valeurs intermédiaires non définies par cette énumération, telles que **mérite \_ normal** + 1.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes et GUID](constants-and-guids.md)
</dt> <dt>

[Instructions pour l’enregistrement des filtres](guidelines-for-registering-filters.md)
</dt> <dt>

[Connexion intelligente](intelligent-connect.md)
</dt> </dl>

 

 




