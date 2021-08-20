---
description: Si cette stratégie système par utilisateur est définie sur &\# 0034 ; 1&\# 0034 ;, les utilisateurs et les administrateurs exécutant une installation de maintenance d’un produit ne peuvent pas utiliser la boîte de dialogue Parcourir pour parcourir les sources de média, telles que les CD-ROM, pour les sources d’autres produits installables.
ms.assetid: 275a6d43-ecf8-4146-82eb-3b42b25b9a80
title: DisableMedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2337a1698865b0b977e179021f6490e2fa651a8c4baa3a56e808d037926ad39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118143245"
---
# <a name="disablemedia"></a>DisableMedia

Si cette [stratégie système](system-policy.md) par utilisateur est définie sur « 1 », les utilisateurs et les administrateurs exécutant une installation de maintenance d’un produit ne peuvent pas utiliser la boîte de dialogue Parcourir pour parcourir les sources de média, telles que les CD-ROM, pour les sources d’autres produits installables. La recherche d’autres produits est empêchée, que l’installation soit effectuée avec des privilèges élevés. Il est toujours possible pour l’utilisateur de réinstaller le produit à partir d’un support si celui-ci possède une source de média correctement libellée.

## <a name="registry-key"></a>Clé de Registre

**HKEY \_ \_** \\ **stratégies logicielles** de l’utilisateur actuel programme d' \\  \\  \\  \\ **installation** de Microsoft Windows

## <a name="data-type"></a>Type de données

**\_valeur DWORD reg**

## <a name="remarks"></a>Remarques

Notez que la propriété [**DISABLEMEDIA**](-disablemedia.md) a un effet différent de la stratégie DISABLEMEDIA. La définition de la stratégie système DisableMedia désactive uniquement la navigation vers les sources multimédias. La définition de la propriété **DISABLEMEDIA** empêche le programme d’installation d’inscrire toute source multimédia, telle qu’un CD-ROM, comme source valide pour le produit. Toutefois, si la navigation est activée, un utilisateur peut toujours accéder à une source multimédia.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Résilience source](source-resiliency.md)
</dt> </dl>

 

 



