---
description: Indicateurs cohérents et terminés
ms.assetid: a641fa95-5587-4362-9869-e5c27c6dd2ce
title: Indicateurs cohérents et terminés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 568b0c614c745f46d8bbcc816b65f501e02de1e0455f0b64216662ec52308213
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954359"
---
# <a name="consistent-and-done-flags"></a>Indicateurs cohérents et terminés

COM+ crée toujours un objet de contexte avant d’activer un objet transactionnel. L’objet Context contient des informations relatives aux objets, telles que son créateur et son identificateur de transaction. Chaque objet de contexte contient également un *indicateur de cohérence* et un *indicateur Done*. Ensemble, ces indicateurs déterminent l’état de l’objet transactionnel.

L’indicateur de cohérence indique que l’objet transactionnel est cohérent ou incohérent. Les détails spécifiques de la cohérence de l’état d’un objet sont définis par le programmeur. Quand un appel de méthode affecte à cet indicateur la valeur true, l’objet est cohérent. False indique que l’objet est incohérent. COM+ affecte la valeur true à l’indicateur lorsqu’il crée une instance d’objet. Un objet cohérent est prêt à poursuivre la transaction. Lorsqu’un objet reste actif, les appels de méthode suivants peuvent basculer à plusieurs reprises l’indicateur de cohérence de true à false et vice versa.

L’indicateur Done détermine la durée d’une transaction. Lorsqu’un appel de méthode est retourné, COM+ inspecte l’indicateur Done. Si la méthode affecte à cet indicateur la valeur true, COM+ désactive l’objet et note l’indicateur de cohérence. Lorsque l’indicateur Done a la valeur false, COM+ ne désactive pas l’objet et ne note pas l’indicateur consistent. COM+ affecte la valeur false à l’indicateur Done lorsqu’il crée une instance d’objet.

L’indicateur consistent convertit un vote pour valider ou abandonner la transaction dans laquelle il s’exécute, et l’indicateur Done finalise le vote. COM+ inspecte l’indicateur de cohérence lorsque l’indicateur Done a la valeur true lors du retour d’un appel de méthode ou lorsque l’objet est désactivé. Bien que l’indicateur de cohérence d’un objet puisse changer à plusieurs reprises au sein de chaque appel de méthode, seule la dernière modification compte.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion des transactions automatiques dans COM+](managing-automatic-transactions-in-com-.md)
</dt> <dt>

[Définition des indicateurs cohérents et terminés](setting-the-consistent-and-done-flags.md)
</dt> </dl>

 

 



