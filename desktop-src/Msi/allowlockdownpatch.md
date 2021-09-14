---
description: Si cette stratégie système par ordinateur n’est pas définie, seuls les administrateurs peuvent corriger les produits existants qui ont été installés à l’aide de privilèges élevés.
ms.assetid: cd07dcb0-b9b5-4186-a916-604c40f88b5f
title: AllowLockdownPatch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c85507d4f24209220ffb64411b452bbe46f3c76a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127092721"
---
# <a name="allowlockdownpatch"></a>AllowLockdownPatch

Si cette [stratégie système](system-policy.md) par ordinateur n’est pas définie, seuls les administrateurs peuvent corriger les produits existants qui ont été installés à l’aide de privilèges élevés. Si AllowLockdownPatch a la valeur « 1 », les utilisateurs non administratifs peuvent, dans certains cas, appliquer des correctifs aux produits lors de l’exécution d’une installation à l’aide de privilèges élevés. Avec la stratégie définie, le correctif peut installer des [mises à niveau mineures](minor-upgrades.md) lors de l’exécution d’une installation utilisant des privilèges élevés, le correctif ne peut pas installer les [mises à niveau majeures](major-upgrades.md). La définition de cette stratégie permet également aux utilisateurs non administratifs d’exécuter des programmes sur des privilèges LocalSystem au cours d’une installation avec élévation de privilèges.

Le paramètre par défaut est recommandé pour garantir un environnement sécurisé.

## <a name="registry-key"></a>Clé de Registre

**HKEY \_ \_** \\ **stratégies logicielles** de l’ordinateur LOCAL \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Type de données

**\_valeur DWORD reg**

## <a name="remarks"></a>Notes

N’importe quel utilisateur peut appliquer un correctif au cours d’une installation sans élévation de privilèges. La définition de cette [stratégie système](system-policy.md) par ordinateur sur « 1 » donne aux utilisateurs non administratifs la flexibilité supplémentaire pour appliquer des correctifs à n’importe quel produit au cours d’une installation avec élévation de privilèges. Si cette stratégie n’est pas définie, les utilisateurs non administratifs ne peuvent pas appliquer un correctif aux applications attribuées ou publiées.

la définition de cette stratégie permet également aux utilisateurs non administratifs d’exécuter des programmes arbitraires sur des privilèges LocalSystem s’ils disposent d’un package de correctifs Windows Installer qui installe ou lance ces programmes.

 

 



