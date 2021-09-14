---
description: Si cette stratégie système par ordinateur est définie sur 1, aucun package sur le système n’obtient la fonctionnalité de composant partagé activée par l’attribut msidbComponentAttributesShared dans la table des composants.
ms.assetid: 28181f8c-8c03-4962-a142-c35d0dd88940
title: DisableSharedComponent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c7a1d4c2bae3f499722890e06502c7a289e6921
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091494"
---
# <a name="disablesharedcomponent"></a>DisableSharedComponent

Si cette [stratégie système](system-policy.md) par ordinateur est définie sur 1, aucun package sur le système n’obtient la fonctionnalité de composant partagé activée par l’attribut **msidbComponentAttributesShared** dans la [table des composants](component-table.md). La valeur par défaut est 0, ce qui active la fonctionnalité de composant partagé pour les composants marqués avec **msidbComponentAttributesShared** dans tous les packages.

**[Windows Installer 4,0 et versions antérieures](not-supported-in-windows-installer-4-0.md):** Non pris en charge. cette fonction est disponible à partir de Windows Installer 4,5.

## <a name="registry-key"></a>Clé de Registre

**HKEY \_ \_** \\ **stratégies logicielles** de l’ordinateur LOCAL \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Type de données

**\_valeur DWORD reg**

 

 



