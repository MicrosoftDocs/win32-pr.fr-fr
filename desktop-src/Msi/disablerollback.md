---
description: Si cette stratégie système est définie sur 1, le programme d’installation ne stocke pas les fichiers de restauration lors de l’installation et désactive la restauration de l’installation.
ms.assetid: 01747de6-7478-4403-ba36-8ff1abc2b70f
title: DisableRollback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7f0ce15e618880f021e04adf7d2146a97f6ed65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951329"
---
# <a name="disablerollback"></a>DisableRollback

Si cette [stratégie système](system-policy.md) est définie sur 1, le programme d’installation ne stocke pas les fichiers de restauration lors de l’installation et désactive la restauration de l’installation. Par défaut, la restauration est activée. Les administrateurs sont invités à ne pas utiliser cette stratégie, sauf si elle est absolument essentielle. Pour plus d’informations, consultez [restauration de l’installation](rollback-installation.md).

## <a name="registry-key"></a>Clé de Registre

Pour désactiver la restauration des installations par utilisateur, affectez la valeur 1 à **DisableRollback** sous la clé de Registre suivante :

**HKEY \_ \_** \\ **Stratégies logicielles** de l’utilisateur actuel \\  \\ **Microsoft** \\ **Windows** \\ **installer**

Pour désactiver la restauration des installations par ordinateur, affectez la valeur 1 à **DisableRollback** sous la clé de Registre suivante.

**HKEY \_ \_** \\ **Stratégies logicielles** de l’ordinateur local \\  \\ **Microsoft** \\ **Windows** \\ **installer**

## <a name="data-type"></a>Type de données

**\_valeur DWORD reg**

 

 



