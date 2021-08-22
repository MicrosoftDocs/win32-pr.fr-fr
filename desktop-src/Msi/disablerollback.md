---
description: Si cette stratégie système est définie sur 1, le programme d’installation ne stocke pas les fichiers de restauration lors de l’installation et désactive la restauration de l’installation.
ms.assetid: 01747de6-7478-4403-ba36-8ff1abc2b70f
title: DisableRollback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5da8380ce5dc7ea0b711d5766a554d6dce970bc81587a75164e61f3694c6a5ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947313"
---
# <a name="disablerollback"></a>DisableRollback

Si cette [stratégie système](system-policy.md) est définie sur 1, le programme d’installation ne stocke pas les fichiers de restauration lors de l’installation et désactive la restauration de l’installation. Par défaut, la restauration est activée. Les administrateurs sont invités à ne pas utiliser cette stratégie, sauf si elle est absolument essentielle. Pour plus d’informations, consultez [restauration de l’installation](rollback-installation.md).

## <a name="registry-key"></a>Clé de Registre

Pour désactiver la restauration des installations par utilisateur, affectez la valeur 1 à **DisableRollback** sous la clé de Registre suivante :

**HKEY \_ \_** \\ **stratégies logicielles** de l’utilisateur actuel programme d' \\  \\  \\  \\ **installation** de Microsoft Windows

Pour désactiver la restauration des installations par ordinateur, affectez la valeur 1 à **DisableRollback** sous la clé de Registre suivante.

**HKEY \_ \_** \\ **stratégies logicielles** de l’ordinateur LOCAL \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Type de données

**\_valeur DWORD reg**

 

 



